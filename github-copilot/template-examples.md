# Template Examples

Real examples you can adapt for your project.

---

## README.md Template

```markdown
# Project Name

Brief one-line description of what your project does.

## Problem It Solves

2-3 sentences explaining why someone would use this. What pain point does it address?

## Features

- Feature 1: Brief description
- Feature 2: Brief description
- Feature 3: Brief description

## Installation

### For npm
\`\`\`bash
npm install project-name
\`\`\`

### For pip
\`\`\`bash
pip install project-name
\`\`\`

### From source
\`\`\`bash
git clone https://github.com/username/project-name.git
cd project-name
npm install  # or pip install -e .
\`\`\`

## Quick Start

Here's a working example that shows the main use case:

\`\`\`javascript
const lib = require('project-name');

// Basic example
const result = lib.doSomething('input');
console.log(result);  // Output: expected result
\`\`\`

Or Python:

\`\`\`python
from project_name import do_something

result = do_something('input')
print(result)  # Output: expected result
\`\`\`

## More Examples

### Example 1: With options
\`\`\`javascript
const result = lib.doSomething('input', {
  option1: true,
  option2: 'value'
});
\`\`\`

### Example 2: Error handling
\`\`\`javascript
try {
  const result = lib.doSomething('input');
} catch (error) {
  console.error('Something went wrong:', error.message);
}
\`\`\`

## API Reference

### \`functionName(arg1, options)\`

**Parameters**:
- \`arg1\` (string): Description of first argument
- \`options\` (object, optional):
  - \`option1\` (boolean): What this does. Default: false
  - \`option2\` (string): What this does. Default: 'default'

**Returns**: Description of return value

**Example**:
\`\`\`javascript
const result = functionName('arg', { option1: true });
\`\`\`

## Configuration

If your project needs configuration:

\`\`\`bash
# Create a config file
cp .config.example.js .config.js

# Edit for your setup
vim .config.js
\`\`\`

## Running Tests

\`\`\`bash
npm test
# or
pytest tests/
\`\`\`

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to contribute.

## Security

If you discover a security vulnerability, see [SECURITY.md](SECURITY.md).

## License

MIT - see [LICENSE](LICENSE)

## Acknowledgments

- Thanks to [Project X](https://example.com) for inspiration
- Built with [Library Y](https://example.com)

---

## More Help

- **Documentation**: [Full docs here](link)
- **Issues**: [Ask a question](link)
- **Discussions**: [Chat with us](link)
```

---

## CONTRIBUTING.md Template

```markdown
# Contributing

Thanks for wanting to contribute! Here's how to help.

## Getting Started

### Fork and Clone

1. Fork the repository on GitHub
2. Clone your fork locally:
\`\`\`bash
git clone https://github.com/YOUR-USERNAME/project-name.git
cd project-name
\`\`\`

### Set Up Development Environment

\`\`\`bash
# Install dependencies
npm install
# or
pip install -e ".[dev]"

# Create a branch for your work
git checkout -b feature/your-feature-name
\`\`\`

### Run Tests

\`\`\`bash
npm test
# or
pytest
\`\`\`

## Making Changes

### Code Style

We follow [style guide here]:
- Use 2 spaces for indentation (not tabs)
- Use \`const\` instead of \`var\` (JavaScript)
- Write comments for complex logic
- Keep functions small and focused

**Lint your code**:
\`\`\`bash
npm run lint
# or
flake8 src/
\`\`\`

### Commit Messages

Write clear commit messages:
\`\`\`
fix: resolve issue with parser
- Explain what was broken
- Explain how you fixed it

feature: add support for new format
- Explain why this is useful
- Explain how to use it
\`\`\`

Bad commit messages:
- ❌ "fix stuff"
- ❌ "updates"
- ❌ "asdfgh"

Good commit messages:
- ✅ "fix: handle null values in parser"
- ✅ "docs: clarify setup instructions"
- ✅ "refactor: simplify error handling"

### Before Submitting

- [ ] Tests pass: \`npm test\`
- [ ] Linter passes: \`npm run lint\`
- [ ] New tests added for new functionality
- [ ] Documentation updated (README, code comments)
- [ ] Commit message is clear

## Submitting a Pull Request

1. **Push to your fork**:
\`\`\`bash
git push origin feature/your-feature-name
\`\`\`

2. **Open a Pull Request** on GitHub with:
   - Clear title: "Fix: Issue description" or "Feature: New feature"
   - Description of what changed and why
   - Reference any related issues: "Closes #123"

3. **Wait for review**:
   - We typically respond within 48 hours
   - Be open to feedback
   - Update your PR if requested

4. **Merge**:
   - Once approved, your PR will be merged
   - You'll be credited in the changelog

## What We Care About

- **Working code**: Tests pass, no breaking changes
- **Clear communication**: Commit messages and PR descriptions explain the why
- **Documentation**: If you change behavior, update docs/comments
- **Tests**: New features come with tests
- **Respect for existing code**: Understand the design before changing architecture

## What We Don't Care About

- Perfectly polished code on first try (we iterate)
- Exact code style (we have linters for that)
- Asking questions (please ask!)

## Questions?

- **How do I...?** Ask in [GitHub Discussions](link)
- **Found a bug?** [Open an issue](link)
- **Security issue?** See [SECURITY.md](SECURITY.md)

## Code of Conduct

See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for community standards.

---

Thanks for contributing! 🙏
```

---

## CODE_OF_CONDUCT.md Template

Based on Contributor Covenant. See [contributor-covenant.org](https://www.contributor-covenant.org/) for the full version and more details.

```markdown
# Code of Conduct

## Our Pledge

We are committed to providing a welcoming and inspiring community for all. We pledge that everyone participating in this project and its community will be treated with respect and dignity.

## Our Standards

Examples of behavior that contributes to creating a positive environment include:

- Using welcoming and inclusive language
- Being respectful of differing opinions, viewpoints, and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

Examples of unacceptable behavior include:

- Harassment or intimidation of any kind
- Discrimination based on gender, gender identity, sexual orientation, disability, age, race, ethnicity, religion, or similar personal characteristics
- Deliberate intimidation, threats, or violent language
- Unwelcome sexual attention or advances
- Trolling, insulting/derogatory comments, and personal or political attacks

## Enforcement

Community members who violate this code of conduct may be temporarily or permanently removed from the community at the discretion of project maintainers.

## Reporting

If you experience or witness unacceptable behavior, please report it to [contact@example.com](mailto:contact@example.com).

All reports will be handled confidentially. We will review and investigate all complaints fairly.

## Attribution

This Code of Conduct is adapted from the Contributor Covenant, version 2.0, available at [https://www.contributor-covenant.org/version/2/0/code_of_conduct/](https://www.contributor-covenant.org/version/2/0/code_of_conduct/)
```

---

## SECURITY.md Template

```markdown
# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please report it responsibly to us rather than using the public issue tracker.

**Email**: [security@example.com](mailto:security@example.com)

Please include:
- Description of the vulnerability
- Steps to reproduce it
- Potential impact
- Any suggested fixes (if you have them)

## What to Expect

- We will acknowledge your report within 48 hours
- We will work with you to understand and fix the issue
- We ask that you do not publicly disclose the vulnerability until we've released a fix
- We will credit you in the security advisory (unless you prefer otherwise)

## Security Practices

- Keep your installation up to date
- Report suspicious activity immediately
- Don't share API keys or credentials in public repositories
- Use .env files for local development (never commit them)

## Supported Versions

We provide security updates for:

| Version | Support Status |
|---------|----------------|
| 2.x     | ✅ Actively supported |
| 1.x     | ⚠️ Security fixes only |
| 0.x     | ❌ No longer supported |

Older versions may have known vulnerabilities. Please upgrade.

## Security Checklist

Before deploying to production:

- [ ] Use the latest stable version
- [ ] Review dependencies for known vulnerabilities: \`npm audit\`
- [ ] Don't commit secrets or API keys
- [ ] Use environment variables for configuration
- [ ] Enable security features in your deployment

## Questions?

Email [security@example.com](mailto:security@example.com) with security-related questions.
```

---

## Tips for Adapting Templates

1. **Replace placeholders**:
   - `[contact@example.com]` → your actual email
   - `project-name` → your project name
   - `YOUR-USERNAME` → your GitHub username
   - `Full docs here` → link to your docs

2. **Keep it honest**:
   - If you only check PRs on weekends, say so
   - If you're a solo maintainer, say "best effort"
   - Don't promise 24/7 support you can't deliver

3. **Match your project**:
   - CLI tool? Show CLI examples
   - Library? Show import/require
   - Web app? Link to live demo
   - Research? Explain the methodology

4. **Be welcoming**:
   - CONTRIBUTING should encourage first-timers
   - CODE_OF_CONDUCT should be about safety, not punishment
   - README should excite people about what you built

5. **Keep it brief**:
   - README: 500-1000 lines max (move details to /docs/)
   - CONTRIBUTING: 200-300 lines
   - CODE_OF_CONDUCT: 100-150 lines (use Contributor Covenant template)
   - SECURITY: 50-100 lines (keep it simple)

---

## Real Examples in the Wild

If you want to see how real projects do this:

**Good READMEs**:
- [React](https://github.com/facebook/react)
- [Node.js](https://github.com/nodejs/node)
- [Vue.js](https://github.com/vuejs/vue)

**Good CONTRIBUTING**:
- [Rails](https://github.com/rails/rails/blob/main/CONTRIBUTING.md)
- [Kubernetes](https://github.com/kubernetes/kubernetes/blob/master/CONTRIBUTING.md)

**Good CODE_OF_CONDUCT**:
- Any project using [Contributor Covenant](https://www.contributor-covenant.org/adopters)

Copy their structure, customize for your project.
