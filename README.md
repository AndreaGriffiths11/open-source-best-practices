# Open Source Best Practices

**Use this if:** You're launching a project publicly, hardening an existing public repo, or preparing a private project for open source. Works standalone or with AI agents (GitHub Copilot, Claude, etc.) that recognize skill formats.

I built this skill because I've seen too many projects launch publicly without thinking through what comes next. Whether you're open-sourcing something for the first time or hardening an existing repo, this framework keeps you from discovering critical gaps after your first contributors show up.

Built on what actually breaks projects: missing security cleanup, unclear governance, burned-out maintainers, and documentation that assumes too much knowledge. We fix those things first.

## What's Inside

You get 8 phases that build on each other, starting with security and ending with sustainability. Each phase has concrete checklists and reference guides you can actually use, not generic best practices that sound nice but don't help.

**The phases:**

Phase 1 is security—clean your git history and remove secrets before anything else. Use [Git History Cleaner](https://andreagriffiths11.github.io/git-history-cleaner/) to scan for and remove API keys, credentials, .env files, and sensitive data. 

Phase 2 covers legal and ownership. Choose your license, verify you own the code, and define what the project is actually for.

Phase 3 is community foundations. Code of conduct and governance. You're setting expectations for how decisions get made.

Phase 4 is documentation and onboarding. README, CONTRIBUTING, issue templates. Help people help themselves.

Phase 5 is setup and infrastructure. CI/CD, verified setup instructions. Make it easy to contribute.

Phase 6 defines maintainer expectations. Roles, SLAs, how to say no. This prevents burnout.

Phase 7 is security and vulnerability reporting. A process for handling incidents responsibly.

Phase 8 is funding and sustainability. GitHub Sponsors, transparency. Optional, but worth thinking about early.

## Installation

To add this skill to your project, run:

```bash
npx skills add https://github.com/AndreaGriffiths11/open-source-best-practices --skill open-source-best-practices
```

This command installs the open-source-best-practices skill, making it available to AI agents like GitHub Copilot that can guide you through the framework.

## How to Use This

**Start here:** Read the full framework in [SKILL.md](SKILL.md). It has all 8 phases with checklists and explains why each one matters.

If you're launching a new project, start with Phase 1 and work through in order. If you already have a public repo, work through them anyway—you can retrofit this framework even if you're already public.

Each phase has a detailed reference guide. Want to pick a license? There's a decision tree. Need to set up GitHub Sponsors? There's a template. Writing a security policy? Copy what's here and adapt it.

You don't have to do all of it at once.

### With AI Agents

If you're using GitHub Copilot, Claude, or another AI agent that recognizes skills, you can ask:
- "Use the open-source-best-practices skill to help me clean my git history"
- "Guide me through Phase 2 (Legal & Ownership) for my project"
- "What files do I need before going public?"

See [github-copilot/AGENTS.md](github-copilot/AGENTS.md) for the agent workflow and how it guides you through each phase. 

## Essential Tool: Git History Cleaner

Before you start the phases, you need [Git History Cleaner](https://andreagriffiths11.github.io/git-history-cleaner/). This tool scans your entire git history for secrets, credentials, API keys, .env files, large binaries, and sensitive data—things you didn't realize were committed years ago.

It safely removes them and rewrites your history so the data is truly gone, not just hidden. This is non-negotiable before going public. Use it first, in Phase 1.

## Key Idea

Your project is healthy when new people can set up locally in 30 minutes, contributors know how to submit PRs without asking, you respond to issues within your stated SLA, your roadmap is visible, security issues have a private reporting process, and you can actually sustain maintenance.

Everything else flows from that.

## Reference Guides Included

- **file-checklist.md** — what files you actually need
- **license-selection.md** — how to pick one that fits
- **security-practices.md** — git history cleaning and secret removal
- **governance.md** — how decisions actually get made
- **maintainer-expectations.md** — roles, SLAs, and protecting yourself
- **sponsors-setup.md** — GitHub Sponsors tiers and strategy
- **template-examples.md** — copy-paste text you can use

## Common Questions

**Do I have to do all 8 phases?** Phases 1-7 before you go public. Phase 8 is optional but recommended.

**Can I skip ahead?** No. Always start with Phase 1. The rest build on it.

**What if I'm already public?** Do it anyway. You can add governance and documentation to an existing repo.

**How long does this take?** Depends on complexity. A week for simple projects, a month for complex ones.

---

## License

This skill is licensed under the **Creative Commons Attribution 4.0 International (CC-BY-4.0) License**. You're free to share and adapt this material for any purpose, including commercially, as long as you provide appropriate attribution. See the [LICENSE](LICENSE) file for details.

## Next Steps

Ready to move forward? 

1. Read [SKILL.md](SKILL.md) for the complete framework
2. Start with Phase 1: Git history cleanup using [Git History Cleaner](https://andreagriffiths11.github.io/git-history-cleaner/)
3. Work through each phase in order

**Want to help?** See [CONTRIBUTING.md](CONTRIBUTING.md) for how to contribute improvements, suggest changes, or add new content.

**Community standards:** Review our [Code of Conduct](CODE_OF_CONDUCT.md) to understand expectations for respectful, inclusive interactions.

Questions or ideas? Open an issue on [GitHub](https://github.com/AndreaGriffiths11/open-source-best-practices) or find me on [X](https://x.com/acolombiadev).

