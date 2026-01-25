# Contributing to Open Source Best Practices

Thanks for considering contributing to this project! This guide explains how to help.

## What We Welcome

We're looking for contributions in these areas:

### Documentation Improvements
- Clearer explanations in the 8 phases
- New examples or case studies
- Better templates for specific project types
- Corrections or updates to reference guides
- Translations (in progress)

### New Reference Guides
- Specific guidance for frameworks or languages
- Community-contributed best practices
- Real-world templates from successful projects
- FAQ additions based on common questions

### Real-World Examples
- Case studies of successful open source launches
- Before/after examples of projects that used this framework
- Templates tailored to specific project types (CLI tools, libraries, frameworks, etc.)

### Bug Reports & Improvements
- Typos, broken links, or clarity issues
- Missing checklists or guidance
- Outdated tool recommendations
- Accessibility improvements

### Tool Integration
- Better integration with [Git History Cleaner](https://andreagriffiths11.github.io/git-history-cleaner/)
- New security scanning tools
- AI agent improvements and feedback

## What We Don't Accept

- Content that promotes closed-source or proprietary practices
- Advertising or sponsored content
- Legal advice (we're not lawyers—guidelines point to lawyers)
- Unsubstantiated claims about licensing or governance
- Content that conflicts with the core mission of sustainable open source

## How to Contribute

### For Small Changes (Typos, Links, Minor Clarifications)

1. **Fork the repository** on GitHub
2. **Create a branch:**
   ```bash
   git checkout -b fix/your-description
   git checkout -b docs/your-description
   ```
3. **Make your changes** in the relevant file
4. **Test your changes:**
   - If adding links, verify they work
   - If editing phase descriptions, ensure clarity
   - If changing templates, ensure they're copy-paste ready
5. **Commit with a clear message:**
   ```bash
   git commit -m "docs: fix typo in Phase 2 section"
   git commit -m "docs: clarify licensing decision tree"
   ```
6. **Push your branch:**
   ```bash
   git push origin fix/your-description
   ```
7. **Open a Pull Request** with:
   - Clear description of what changed and why
   - Reference to any related issues

### For Larger Changes (New Guides, Major Rewrites, New Sections)

1. **Open an issue first** to discuss the change
   - Describe what you want to add and why
   - Explain how it fits into the framework
   - Wait for feedback before starting work

2. **Create a draft PR** if the issue is approved
   - Work on your changes in a branch
   - Open the PR as a draft to get early feedback
   - Iterate based on reviewer comments

3. **Finalize and submit**
   - Once approved, mark as ready for review
   - Address remaining feedback
   - The PR will be merged

## Writing Style

Keep these principles in mind:

- **Practical over theoretical** - Show concrete steps, not abstract concepts
- **Short sentences** - Easier to scan and understand
- **Active voice** - "You need to" not "It should be"
- **Examples always** - Templates, checklists, real scenarios
- **Link to tools** - Reference [Git History Cleaner](https://andreagriffiths11.github.io/git-history-cleaner/) and other resources when relevant
- **Honest about trade-offs** - No "this is always the right answer"
- **Assume no prior knowledge** - Explain terms, don't assume people know our jargon

### Formatting

- Use markdown consistently
- Use `code` for technical terms, file names, commands
- Use **bold** for emphasis, not bold-italic
- Use lists for steps or options
- Use tables for comparisons
- Link relevant sections within the project

### Templates

If you're adding a template (LICENSE, CONTRIBUTING, CODE_OF_CONDUCT, etc.):
- Make sure it's copy-paste ready
- Include [brackets] for placeholders
- Add a note about what needs to be customized
- Example:
  ```markdown
  # Code of Conduct
  
  Thank you for contributing to [PROJECT NAME].
  
  This project has adopted the Contributor Covenant Code of Conduct.
  See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for full text.
  
  To report violations, email: [CONTACT EMAIL]
  ```

## Review Process

The maintainers will review your PR within 1-2 weeks. We look for:

1. **Clarity** - Is the guidance clear and actionable?
2. **Accuracy** - Is the information correct?
3. **Completeness** - Does it fit into the framework? Are there gaps?
4. **Practical value** - Will this help someone launching open source?
5. **Tone** - Does it match the project's voice (honest, practical, supportive)?
6. **Links** - Do all links work? Are they to stable resources?

We may ask you to:
- Clarify language or add examples
- Adjust tone or structure
- Add links to related sections
- Expand or condense content
- Update based on community feedback

## Commit Message Format

Use clear, descriptive commit messages:

```
docs: add licensing decision tree for non-profit projects
security: update Git History Cleaner examples
phase-2: clarify ownership verification checklist
templates: add CONTRIBUTING template for CLI tools
fix: correct broken link in governance guide
```

Prefixes:
- `docs:` - Documentation changes
- `phase-1` to `phase-8:` - Changes to specific phases
- `security:` - Security-related updates
- `templates:` - Template additions or changes
- `fix:` - Typos, broken links, corrections
- `refactor:` - Restructuring content without changing meaning

## Attribution

When you contribute, you:
- Agree your contribution is licensed under CC-BY-4.0 (same as this project)
- Grant permission to include your name in the project's contributor list
- Understand that your content may be adapted or improved by others

We'll acknowledge significant contributions in:
- The `CONTRIBUTORS.md` file
- Release notes
- README (for major contributions)

## Questions or Ideas?

- **Unclear guidance?** Open an issue asking for clarification
- **New idea?** Start a discussion or issue describing what you want to add
- **Tool integration?** Let us know how we can better support your workflow
- **Feedback?** Tell us what's missing or what could be better

## Code of Conduct

This project has adopted the [Contributor Covenant](https://www.contributor-covenant.org/version/2/1/code_of_conduct/). All contributors are expected to be respectful and professional.

Unacceptable behavior includes:
- Harassment, discrimination, or hostile language
- Dismissing others' ideas without engaging seriously
- Spamming or advertising
- Violating others' privacy or intellectual property


## Local Development

### Prerequisites
- Git
- A markdown editor (VS Code, Obsidian, etc.)
- [Git History Cleaner](https://andreagriffiths11.github.io/git-history-cleaner/) (for testing Phase 1 examples)

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AndreaGriffiths11/open-source-best-practices.git
   cd open-source-best-practices
   ```

2. **Create a branch:**
   ```bash
   git checkout -b feature/your-branch-name
   ```

3. **Make your changes:**
   - Edit `.md` files in the root and `github-copilot/` folders
   - Test links and formatting locally
   - Verify examples are accurate

4. **Test your changes:**
   - Open markdown files in your editor
   - Click links to verify they work
   - Read through for clarity and flow
   - Ask a friend to review if you can

5. **Push and open a PR:**
   ```bash
   git add .
   git commit -m "your clear commit message"
   git push origin feature/your-branch-name
   ```

### Verifying Links

For PRs that add or change links:
- Verify external links are not behind paywalls
- Ensure links to GitHub files point to `main` branch
- Test that relative links work (e.g., `[Phase 2](github-copilot/governance.md)`)

## Testing Changes

For content changes, test by:
1. **Reading aloud** - Does it flow naturally?
2. **Following instructions** - Can you actually do what it says?
3. **Checking examples** - Are code examples realistic and correct?
4. **Verifying links** - Do they go where you'd expect?

## Improvement Ideas Without Code

Even if you don't write content, we welcome:
- Comments on open issues sharing your experience
- Feedback on what's confusing
- Real-world examples of the framework in action
- Stories about how open source maintainers struggle
- Suggestions for new section topics

## Rights and Recognition

By contributing to this project, you agree that:
- Your contribution will be licensed under CC-BY-4.0
- We may use your contribution in derived works
- Your name will be attributed where appropriate
- You're not providing legal or professional advice (we're not lawyers)

## Questions?

Open an issue or reach out:
- **GitHub Issues:** [open-source-best-practices/issues](https://github.com/AndreaGriffiths11/open-source-best-practices/issues)
- **GitHub Discussions:** [open-source-best-practices/discussions](https://github.com/AndreaGriffiths11/open-source-best-practices/discussions)
- **X:** [@acolombiadev](https://x.com/acolombiadev)

---

Thanks for helping build sustainable open source! 🚀
