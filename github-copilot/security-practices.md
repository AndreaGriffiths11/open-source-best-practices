# Security: Cleaning Git History Before Public Release

Your git history becomes public when you make the repo public. **Secrets committed and then deleted are still visible in the history.** Anyone can clone your repo and dig through commits to find them.

Before publishing, you must clean your git history.

---

## What to Look For

### Critical - Remove Immediately

**Credentials & Secrets**:
- API keys, tokens, auth tokens
- Passwords (database, SSH, etc.)
- Private keys (.pem, .key files)
- AWS access keys, Firebase keys
- OAuth tokens, JWT secrets
- Database connection strings
- .env files with real values

**Internal/Sensitive Info**:
- Private URLs, internal hostnames
- Internal IP addresses
- Employee emails (personal)
- Proprietary algorithm/research
- Internal project names/codenames
- Real customer data, PII

**Problematic Files**:
- Large binaries (videos, archives, databases)
- Compiled dependencies (node_modules committed by mistake)
- Build artifacts
- Lock files with private registries

### How to Scan for These

**Quick manual check**:
```bash
# Search for common secret patterns
git log -p | grep -i "password\|secret\|api[_-]?key\|token\|credential"

# Find API key patterns
git log --all -S "sk_" --oneline  # Stripe keys
git log --all -S "AKIA" --oneline  # AWS keys

# Find large files already in history
git rev-list --all --objects | \
  awk '{print $1}' | git cat-file --batch-check | \
  grep blob | sort -k3 -n | tail -20
```

**Better approach**: Use a tool. See "How to Clean It" below.

---

## How to Clean It

### Option 1: Git History Cleaner (Recommended)

[Git History Cleaner](https://github.com/AndreaGriffiths11/git-history-cleaner) is specifically designed for this. It safely removes secrets, sensitive data, large files, and entire commits from your entire git history.

**Why use it**:
- Rewrites history so sensitive data is truly gone (not just hidden)
- Handles complex patterns (API keys, file types, commit ranges)
- Much safer than manual git filter-branch
- User-friendly; generates scripts you can review before running

**What it removes**:
- Specific secrets or patterns (e.g., "sk_live_")
- Entire files (e.g., ".env", "config.json")
- Commits containing specific data
- Large files above a threshold

**Basic workflow**:

```bash
# Install
npm install -g git-history-cleaner
# or
git clone https://github.com/AndreaGriffiths11/git-history-cleaner
cd git-history-cleaner
npm install

# Find and remove
git-history-cleaner scan                    # Scan for secrets
git-history-cleaner remove --pattern "sk_"  # Remove by pattern
git-history-cleaner remove --file ".env"    # Remove by filename
git-history-cleaner remove --size 100mb     # Remove large files

# Force-push the cleaned history
git push origin --force --all
git push origin --force --tags
```

See the [Git History Cleaner docs](https://github.com/AndreaGriffiths11/git-history-cleaner) for detailed examples.

---

### Option 2: Manual Approach (If Preferred)

**Using git filter-repo** (safer than old git filter-branch):

```bash
# Install
pip install git-filter-repo

# Remove specific file from all history
git filter-repo --path .env --invert-paths

# Remove large files
git filter-repo --larger-than 50M --invert-paths

# After cleanup
git push origin --force --all
git push origin --force --tags
```

**Using git filter-branch** (last resort, harder to undo):

```bash
# Remove a specific file
git filter-branch --tree-filter 'rm -f .env' HEAD

# This is more complex and error-prone. Use Git History Cleaner instead.
```

---

## After Cleaning

### Force-Push
```bash
# CAUTION: This rewrites history. Make sure everyone on the team knows.
git push origin --force --all
git push origin --force --tags
```

**Tell your team**: If anyone has cloned this repo, they need to re-clone after the force-push.

### Tell Collaborators
Let everyone who's cloned the repo know to:
```bash
git pull --rebase origin main
# or just re-clone
```

### Verify the Clean
```bash
# Confirm the secrets are gone
git log --all -S "secret_value" --oneline  # Should return nothing

# Verify file is gone from history
git log --all --full-history -- ".env" --oneline  # Should return nothing
```

---

## Best Practices Going Forward

### Prevent Future Commits

**Use .gitignore properly**:
```gitignore
# Environment variables
.env
.env.local
.env.*.local

# OS files
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/

# Dependencies
node_modules/
__pycache__/
vendor/

# Secrets and keys
*.key
*.pem
*.p12
config.secrets.json
```

**Use a secrets manager locally**:
```bash
# Good: Store secrets in .env.local (excluded by .gitignore)
echo "DATABASE_PASSWORD=xyz123" >> .env.local

# Bad: Store in code or config files
# Don't do this:
const password = "xyz123";  // ❌
```

**Use pre-commit hooks** to catch secrets before they're committed:

```bash
# Install pre-commit framework
pip install pre-commit

# Create .pre-commit-config.yaml in repo root
repos:
  - repo: https://github.com/Yelp/detect-secrets
    rev: v1.4.0
    hooks:
      - id: detect-secrets
        args: ['--baseline', '.secrets.baseline']
```

Then secrets are scanned before every commit:
```bash
git commit ...
# Pre-commit runs and warns if secrets detected
# Commit is blocked
```

### For Secrets in CI/CD

**GitHub Actions** (or similar):
```yaml
jobs:
  build:
    env:
      DATABASE_PASSWORD: ${{ secrets.DATABASE_PASSWORD }}
      API_KEY: ${{ secrets.API_KEY }}
```

Secrets are injected at runtime, never committed.

### Educate Your Team

- Never commit `.env` files with real values
- Use `.env.example` with placeholders instead
- Always create `.env.local` for local overrides (in .gitignore)
- Use CI/CD secrets for production credentials
- Review PR diffs carefully before approving

---

## Checklist Before Going Public

- [ ] Scan git history for secrets (use Git History Cleaner)
- [ ] Remove all .env files with real values
- [ ] Remove any API keys, tokens, or credentials
- [ ] Remove large binaries/build artifacts
- [ ] Remove any sensitive internal references
- [ ] Verify with: `git log --all -S "secret" --oneline` (should return nothing)
- [ ] Force-push: `git push origin --force --all`
- [ ] Add proper .gitignore for future protection
- [ ] Add pre-commit hooks to catch secrets
- [ ] Tell your team about the history rewrite
- [ ] Make repo public

---

## If You Discover Secrets After Public Release

1. **Treat it as a real security incident**
2. **Immediately rotate** the compromised credentials (password, API key, token, etc.)
3. **Clean your history** using Git History Cleaner
4. **Force-push**: `git push origin --force --all`
5. **Notify users** if PII was exposed (privacy law requirement in many jurisdictions)
6. **Set up alerts** for that credential in services (e.g., GitHub Dependabot alerts)

The key is rotating the actual credential. Cleaning the history prevents future access, but the credential is still compromised until you change it in the actual system.

---

## Remember

- **Git history is permanent**. Deletion only hides, it doesn't remove.
- **Use Git History Cleaner** to safely and completely rewrite history.
- **Clean before public**. It's way easier than doing it after.
- **Prevent future problems** with .gitignore, .env.local, and pre-commit hooks.
- **Educate your team**. Secrets get committed by accident.

The public repo is not the place for secrets.
