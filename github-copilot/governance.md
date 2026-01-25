# Governance Framework

This guide helps you document how decisions are made in your project and how to handle disagreements, scope disputes, and rejections kindly.

---

## Governance Model

Document your governance model in **GOVERNANCE.md** or in README under a "How This Project Works" section.

### Simple Governance (Most Projects)

For small/medium projects with 1-3 maintainers:

```markdown
# Governance

## Decision-Making

**Small decisions** (documentation, minor bug fixes, small improvements):
- Any maintainer can approve and merge

**Feature proposals**:
- Open an issue to discuss
- Maintainers review and comment
- If consensus: proceed to PR
- If disagreement: we discuss until consensus or maintainer makes final call

**Breaking changes**:
- Must be discussed in an issue first
- Requires RFC (Request for Comments) document
- Needs agreement from all active maintainers
- Announced in release notes and changelog

**Governance changes** (to this document):
- Requires discussion and all maintainer agreement

## Who Decides

- @alice: Project lead, final decision authority
- @bob: Core contributor, PR reviews
- @carol: Community liaison, issue triage

## How to Propose

1. Open an issue describing your idea
2. Discuss with maintainers
3. If accepted: submit PR
4. Maintainer reviews and provides feedback
5. You iterate and merge

## Appeals

If you disagree with a decision:
1. Comment respectfully in the issue
2. Ask for clarification
3. If still unresolved: email maintainers@example.com

We'll discuss and explain our reasoning.
```

### Formal Governance (Large Projects)

For projects with large communities or multiple organizations:

```markdown
# Governance

## Project Structure

**Steering Committee** (3-5 people):
- Sets strategic direction
- Approves major features and breaking changes
- Manages maintainer onboarding/offboarding
- Meets monthly

**Maintainers** (5+ people):
- Review PRs
- Triage issues
- Implement decisions from steering committee
- Manage their area (docs, performance, security, etc.)

**Contributors**:
- Submit PRs
- Propose ideas
- Participate in discussions

## Decision Process

**Lazy consensus**: If no disagreement for 72 hours, a proposal is approved.

**Voting**: If consensus can't be reached:
- Steering committee votes (majority wins)
- Documented in meeting notes

**Blocking**: Any maintainer can block a decision with justification.
If blocked, discussion required.

## Conflict Resolution

1. **Discussion**: Talk in issues/meetings
2. **Mediation**: Ask neutral steering committee member to facilitate
3. **Vote**: If still stuck, steering committee votes
4. **Escalation**: For serious conflicts, external mediator (if funded)

## Changing Governance

Changes to governance require steering committee vote + 2/3 majority.
```

---

## Vision & Scope Documentation

Write a clear VISION.md or add to README to help you say "no" kindly.

### What to Include

```markdown
# Vision & Scope

## Problem We're Solving

[Specific problem] for [specific users].

Example:
"Managing CSS across large scale applications without naming conflicts."

## Who We're For

- React/Vue developers building large applications
- Teams with multiple independent feature teams
- Projects with >10k lines of CSS

## What We Do

1. Provide CSS-in-JS with automatic namespacing
2. Enable component scoping without build tools
3. Support dynamic styling based on runtime state
4. Maintain small bundle size (< 10kb gzipped)

## What We Explicitly Don't Do

1. **Server-side rendering optimization**: Use [Project X] for that
2. **Animation library**: Combine with [Project Y]
3. **CSS framework (Bootstrap-style)**: Use [Project Z] instead
4. **Preprocessor features (Sass/Less)**: Use those directly
5. **Browser fallbacks for IE11**: We support modern browsers only

## Decision Framework

We say "no" to features that:
- Expand scope without clear benefit to existing users
- Add significant maintenance burden
- Conflict with our core use case (simplicity + component scoping)
- Require ongoing support we can't sustain

## Example Scenarios

### "Add Tailwind integration"
We appreciate the interest, but that's out of scope. Our scope is CSS-in-JS 
with component scoping. Tailwind is a utility-first framework, which is a 
different paradigm. Consider using Tailwind directly or combining both.

### "Support SSR optimization"
That's a great need, but it's beyond our scope. We focus on runtime CSS 
management. For SSR, check out [Project X].

### "Add animation support"
We keep animations out of scope to stay focused. Combine us with [Animation 
Library Y] for animation support.
```

---

## How to Say No (Kindly)

This is one of the hardest parts of maintaining open source. Here's a framework.

### The "No" Template

```markdown
Thanks for proposing this, @username! I appreciate the thoughtful suggestion.

Here's why we're not moving forward with this:

1. **Scope**: This falls outside our core mission to [state mission]. 
   We try to stay focused so we can maintain quality.

2. **Maintenance burden**: This would add ongoing support cost without 
   clear benefit to existing users.

3. **Alternative**: For your use case, consider [Project X] which 
   specifically handles [that feature].

This doesn't mean your idea is bad—it's just not the right fit for us. 
We hope you understand, and we'd love to hear if [Alternative] works for you!

Closing this issue, but always happy to discuss further.
```

### Real Examples

**Example 1: Out of Scope**

```markdown
Thanks for the proposal to add real-time collaboration features!

We appreciate the enthusiasm, but real-time sync is outside our scope. 
We're focused on being a single-user, offline-first editor. Real-time 
collaboration adds complexity and infrastructure we can't maintain.

For real-time features, check out:
- [Project A] - Purpose-built for collaborative editing
- [Project B] - Great for real-time data sync

These would work great alongside our editor!

Thanks for understanding.
```

**Example 2: Maintenance Burden**

```markdown
I love this idea, but I'm concerned about the maintenance cost.

Our project is maintained by volunteers with limited time. Adding 
[feature] would require ongoing support for edge cases we can't 
anticipate. Right now, we barely keep up with core maintenance.

If you'd like to champion this: you could maintain a plugin/extension. 
Many users do this and publish separately! See [Plugin Guide].

Thanks for understanding our constraints.
```

**Example 3: Breaking Change**

```markdown
Great catch on this inefficiency! However, fixing it would break 
existing code for users relying on current behavior.

We keep breaking changes rare because they're expensive for our users.

Options:
1. Deprecate: We add a warning in v2, remove in v3
2. New API: We add a new method alongside the old one
3. Configuration: We add an opt-in flag for new behavior

Which appeals to you? Let's discuss in the issue.
```

### Tone Guidelines

**Do**:
- Be specific about why you're saying no
- Acknowledge the effort in the proposal
- Suggest alternatives
- Stay professional and warm
- Explain your constraints (maintainer time, scope, etc.)
- Give them a path forward

**Don't**:
- Say "We don't want this" without explanation
- Be dismissive of the idea
- Make them feel bad
- Disappear without responding
- Argue if they push back; explain your thinking once, then close kindly

---

## Communication Preferences

Document how your community should communicate:

```markdown
# How We Communicate

## Public First

- **Issues & Discussions**: Use these for all public discussions
- **Record decisions**: Document why decisions were made
- **Searchable**: Future users can learn from your discussions

## Where to Go

- **Bug reports**: [GitHub Issues](link)
- **Feature proposals**: [GitHub Issues](link) or [Discussions](link)
- **Questions**: [GitHub Discussions](link) or [Stack Overflow](link)
- **Real-time chat**: [Discord](link) (but decisions go in issues)
- **Security issues**: Email security@example.com (not public)

## Avoid Direct Messages

We prefer discussions in public channels because:
1. Others can learn from the conversation
2. Decisions are documented
3. Multiple people can help (not just one maintainer)
4. Reduces bus factor (project not dependent on one person)

If you DM a maintainer, they might ask you to open an issue instead.

## Response Times

See SLAs section in main skill.
```

---

## Maintainer Onboarding/Offboarding

Document how people become (and stop being) maintainers:

```markdown
# Becoming a Maintainer

## Criteria

You're a good fit if you:
- Have been active for 3+ months
- Submitted 10+ quality PRs
- Demonstrated good judgment in discussions
- Understand the project vision and constraints
- Can commit to ongoing maintenance (even if just a few hours/month)

## How It Works

1. **Invitation**: Current maintainers invite you privately
2. **Discussion**: We talk about expectations and time commitment
3. **Onboarding**: We add you to MAINTAINERS.md and assign relevant areas
4. **Support**: Existing maintainers help you learn review process

## What Maintainers Do

1. **Code review**: PR reviews, suggest changes, approve merges
2. **Issue triage**: Label issues, respond to questions, prioritize
3. **Releases**: Help publish new versions
4. **Communication**: Represent project in community
5. **Decision-making**: Participate in governance

Time commitment: 2-5 hours/week (varies by season)

---

# Maintainer Offboarding

When a maintainer needs to step back:

1. **Discussion**: Talk with steering committee
2. **Transition**: Handoff responsibilities to other maintainers
3. **Credit**: Always thank them publicly, mention their work
4. **Optionally**: Keep them as "emeritus" (honorary role)

No shame in stepping back. Open source maintainence is hard.
```

---

## Handling Contentious Issues

For when there's real disagreement:

```markdown
## When We Disagree

Sometimes maintainers disagree about the right direction.

**Process**:
1. Open a GitHub Discussions thread labeled "RFC" (Request for Comments)
2. Explain your position with reasoning
3. Others comment with perspective
4. We discuss for 1-2 weeks
5. Steering committee votes if consensus isn't reached
6. Decision documented and implemented

**Example**:

Issue: Should we add TypeScript support?

Pros:
- Type safety
- Better IDE support
- Attracts more developers

Cons:
- Increases complexity
- Harder for beginners
- More maintenance burden

Decision: We'll add TypeScript definitions (not rewrite in TS).
This gives type benefits without rewriting.
```

---

## Transparency & Documentation

Keep governance transparent:

**Document**:
- [ ] Decision made → note in issue
- [ ] Controversial decisions → blog post or RFC
- [ ] Maintainer changes → announce in release notes
- [ ] Governance changes → update GOVERNANCE.md
- [ ] Goals & roadmap → visible in README or ROADMAP.md

**Links from README**:
```markdown
## Project Governance

- [GOVERNANCE.md](GOVERNANCE.md) - How we make decisions
- [VISION.md](VISION.md) - What we do and don't do
- [MAINTAINERS.md](MAINTAINERS.md) - Current maintainers
- [Roadmap](ROADMAP.md) - Where we're going
```

---

## Red Flags (What to Avoid)

❌ **All decisions made by one person** - Single point of failure

❌ **No documentation of decisions** - Community doesn't understand why

❌ **Rejecting ideas without explanation** - Contributors feel unwelcome

❌ **Inconsistent governance** - Some ideas accepted, same type rejected differently

❌ **Private discussions of public decisions** - Lack of transparency

❌ **No vision/scope** - Every feature request becomes an argument

❌ **No SLAs** - Maintainers burn out responding to every message

✅ **Clear governance** - Everyone knows how decisions happen

✅ **Documented vision** - People understand scope

✅ **Kind rejections** - Explained and alternatives offered

✅ **Public decisions** - Searchable, transparent, learnable

✅ **Realistic SLAs** - Sustainable pace

✅ **Multiple maintainers** - No bus factor

---

## Templates to Copy

### GOVERNANCE.md

```markdown
# Governance

See this document for how decisions are made in this project.

## Decision Types

| Decision | Who Decides | Process | Timeline |
|----------|-----------|---------|----------|
| Bug fix | Any maintainer | Approve & merge | Same day |
| Feature | Steering committee | Discuss in issue → Vote if needed | 1-2 weeks |
| Breaking change | Steering committee | RFC + Vote | 2-4 weeks |
| Governance change | Steering committee | Discussion + Vote | 2-4 weeks |

## Current Maintainers

- @alice - Project lead, final decision
- @bob - Core contributor
- @carol - Community liaison

## How to Propose

1. Open an issue
2. Describe idea + reasoning
3. Discuss with maintainers
4. If approved: submit PR
5. Review → Merge

## Questions?

Ask in our [Discussions](link).
```

### MAINTAINERS.md

```markdown
# Maintainers

## Current Team

| Name | Role | Focus Area | Contact |
|------|------|-----------|---------|
| Alice | Lead | Architecture | alice@example.com |
| Bob | Reviewer | Performance | bob@example.com |
| Carol | Liaison | Community | carol@example.com |

## Responsibilities

- Review and merge PRs
- Triage and respond to issues
- Participate in governance decisions
- Represent project in community
- Publish releases

## Time Commitment

2-5 hours/week on average. Varies by season and urgency.

## How to Become a Maintainer

See GOVERNANCE.md
```
