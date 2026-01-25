# Maintainer Expectations & Communication

This guide helps you set realistic expectations and communicate effectively with your community.

---

## Defining Your Maintainer Role

First, be clear about what you're committing to. Open source burnout is real.

### Maintainer Responsibilities

What maintainers typically do:

1. **Triage issues**
   - Read issue, understand the problem
   - Label and categorize
   - Ask clarifying questions
   - Link related issues

2. **Review PRs**
   - Check code quality
   - Ensure tests pass
   - Verify no breaking changes
   - Suggest improvements
   - Approve and merge

3. **Respond to community**
   - Answer questions in issues/discussions
   - Provide support (with limits)
   - Guide new contributors
   - Report bugs

4. **Manage releases**
   - Merge PRs into release branch
   - Update CHANGELOG
   - Publish to npm/PyPI/etc
   - Announce new version

5. **Maintain roadmap**
   - Keep backlog current
   - Prioritize issues
   - Communicate plans

6. **Decision-making**
   - Participate in governance
   - Approve/reject proposals
   - Make trade-off decisions

### What Maintainers DON'T Do

Be clear about boundaries:

❌ Provide free consulting for how to use the library in your project  
❌ Debug user's code (they can ask, but it's not your job)  
❌ Answer every question (link to docs instead)  
❌ Respond 24/7 (set SLAs)  
❌ Implement every feature request (say no often)  
❌ Fix every bug others report (triage and let community help)  
❌ Support legacy versions forever (set support windows)  

---

## Response Time SLAs (Service Level Agreements)

Set realistic expectations. Be honest about availability.

### What to Document

Add to README or CONTRIBUTING:

```markdown
## Support & Response Times

We're a [volunteer/part-time/full-time] project. Here are our typical 
response times. These are targets, not guarantees.

### Issues
- **New issue**: We aim to triage within 1 week
- **Bug report**: We try to confirm/investigate within 2 weeks
- **Question**: Refer to docs; if truly stuck, answer within 1-2 weeks

### Pull Requests
- **From maintainers**: Review within 3 days
- **From contributors**: Review within 1-2 weeks
- **Approved**: Merge within 1 week

### Security Reports
- **Acknowledgment**: Within 24 hours
- **Initial response**: Within 48 hours
- **Fix**: Depends on severity (critical: ASAP, others: 1-2 weeks)

### Release Cadence
- **Bug fixes**: Published as needed (within days of fix)
- **Minor releases**: [Weekly / Monthly / As-needed]
- **Major releases**: [4x per year / Annually / As-needed]

### Exceptions
- During holidays, major life events, or high-activity periods, 
  responses may be slower. We'll communicate if delays are expected.

We're all volunteers. Patience and understanding appreciated!
```

### Setting SLAs by Project Maturity

**Early stage** (< 1 year old, small user base):
- Issues: Best effort, could be weeks
- PRs: Review within 2-3 weeks
- Release cadence: Irregular, when ready

**Established** (1-3 years, moderate users):
- Issues: Triage within 1 week
- PRs: Review within 1-2 weeks
- Release cadence: Monthly or quarterly

**Mature** (3+ years, large users):
- Issues: Triage within 3-5 days
- PRs: Review within 3-5 days
- Release cadence: Monthly or bi-weekly

**Corporate-backed**:
- Issues: Within 24 hours
- PRs: Within 1-2 days
- Release cadence: Weekly or more

---

## Public Communication Preference

Document how you want community to communicate.

### Prefer Public Channels

```markdown
## How We Communicate

We prefer **public communication** because:

1. **Others learn from it**: Issues and discussions are searchable
2. **Multiple people can help**: Not dependent on one maintainer
3. **Decisions are transparent**: Community understands reasoning
4. **Reduces maintenance burden**: Don't answer same question 10x

### Where to Go

**For bug reports**: [GitHub Issues](link) - Describe problem, steps to reproduce, environment

**For feature proposals**: [GitHub Issues](link) or [Discussions](link) - Explain the need and proposed solution

**For questions**: [Discussions](link) or [Stack Overflow](link) with `[project-name]` tag

**For chat/realtime**: [Discord](link) (but decisions go in issues, not chat)

**For security issues**: Email security@example.com (NOT public issues)

### Avoid Direct Messages

Please don't DM maintainers with:
- Support questions (use Issues/Discussions)
- Feature requests (use Issues)
- Bug reports (use Issues)
- General chat (use Discord/Slack)

**Why?**:
- We might miss it
- Others can't learn from the answer
- We prefer to batch communications

If you DM, we'll politely ask you to open an issue.

### Response to "Just DM me"

If someone suggests just DM-ing a maintainer:

```markdown
We keep communication public because:
- Others with same question benefit
- We don't lose discussions in DMs
- Maintainers can focus and batch responses
- No single person becomes bottleneck

Thanks for using [project]!
```
```

### Encouraging Discussion Issues

Use GitHub Discussions for non-bug topics:

```markdown
## Ideas & Discussion

Before proposing a feature, let's discuss in [Discussions](link)!

**Good discussion topics**:
- "How should we handle X?" - Get community input
- "Has anyone tried Y?" - Learn from others
- "What do you all think about Z?" - Gauge interest

**Then** if there's agreement, someone opens an issue with formal proposal.

This prevents us from closing issues when we say "no" after someone 
invested effort in a PR.

Thanks for discussing first!
```

---

## How to Say No (In Practice)

The hardest part of maintaining. Here's how to do it well.

### The Three-Part Framework

**1. Thank them**
- Appreciate the effort
- Acknowledge the idea
- Show you read their proposal

**2. Explain why**
- Specific reason(s)
- Not vague ("not right now")
- Reference scope/vision/constraints

**3. Suggest alternative**
- Link to similar project
- Offer different approach
- Offer to help in modified way

### Real Examples

**Example 1: Out of Scope**

```markdown
Thanks so much for taking the time to propose this feature, @alice!

I appreciate the detailed write-up. However, this falls outside our 
project's scope. We focus on [core mission]. Adding [requested feature] 
would expand us into [new area], which:

1. Adds maintenance burden we can't sustain
2. Distracts from our core mission
3. Isn't a good fit for our audience

**Good alternatives for your use case:**
- Project X (specifically designed for this)
- Project Y (handles this with a plugin)
- You could build this as a separate plugin!

Thanks for understanding. Closing this issue, but we'd love to hear 
if those alternatives work for you!
```

**Example 2: Already Proposed**

```markdown
Great idea, @bob! We've discussed this before in #123. 

The conclusion was:
- Pros: [list]
- Cons: [list]
- Decision: Prioritizing other work

We're not reopening this right now. If you have new information, 
please comment on #123 with a fresh perspective!

Thanks.
```

**Example 3: Implementation Concerns**

```markdown
I like the idea, @carol, but I have concerns about the implementation:

1. This would require breaking changes to [API]
2. It adds complexity that might not pay off
3. There's a simpler approach: [alternative]

**Proposed compromise:**
Instead of [big change], what about [smaller change]? It addresses 
80% of the use case with less complexity.

Thoughts?
```

**Example 4: Maintenance Burden**

```markdown
This is a great suggestion, @david, but I'm concerned about 
long-term maintenance.

Our project is maintained by volunteers. We're barely keeping up 
with existing features. Adding [feature] would require:

- Ongoing support for edge cases
- Regular updates as X changes
- Triaging related bugs

**What I can offer:**
- Merge a well-tested implementation (you maintain initial code)
- Help review PRs on this feature
- Not add it as a core feature

If you want to champion this, a plugin/extension approach might work 
better. See [plugin guide]. Then you're in control!

Closing this, but let me know if you want to pursue as plugin.
```

**Example 5: Blocking a PR**

```markdown
Thanks for the effort on this PR, @eve! I appreciate the work.

However, I'm going to block this merge because:

1. [Specific technical concern]
2. [Breaking change impact]
3. [Maintenance concern]

**Before we can merge, we need:**
- Discussion in #XYZ about approach
- Consensus from maintainers
- Different implementation strategy

I know this is disappointing. Let's discuss in issue #XYZ about 
how to move forward. Open to alternatives!
```

### Tone Checklist

When rejecting a proposal:

- [ ] Did I thank them for the effort?
- [ ] Did I explain my reasoning clearly?
- [ ] Did I suggest alternatives?
- [ ] Did I offer a path forward (if any)?
- [ ] Did I keep it warm, not cold?
- [ ] Did I explain my constraints (time, scope, maintenance)?
- [ ] Did I close the issue respectfully?

---

## Managing Burnout & Setting Boundaries

You can't maintain if you burn out.

### Red Flags

You might be burning out if:

- ✋ You dread opening GitHub notifications
- ✋ You respond to issues outside working hours
- ✋ You feel responsible for every user's problem
- ✋ You argue with every rejected feature
- ✋ You haven't had a break in months
- ✋ You're the only decision-maker and it's exhausting

### Boundaries to Set

```markdown
## Taking Care of Ourselves

Maintaining open source is a gift to the community, not an obligation. 
To keep [project] sustainable, we need to take care of ourselves.

**Maintainers have the right to:**
- Take breaks (weeks off without responding)
- Say no to out-of-scope requests
- Close "WONTFIX" issues without argument
- Set their own availability
- Delegate tasks to other maintainers
- Simplify maintenance burden

**This means:**
- Don't expect 24/7 support
- Help in community Slack for free, not one-on-one consulting
- We won't respond to every message
- Some issues will close without implementation
- We reserve the right to step back if needed

We appreciate your understanding. We're all volunteers and we care 
for this project on our own terms.
```

### Taking Time Off

```markdown
## [Maintainer] is Taking Time Off

@alice will be off-grid from [dates]. 

During this time:
- No response to emails or messages (going offline)
- Issues/PRs will be triaged by other maintainers
- No emergencies unless critical security issue
- See security@example.com for urgent security matters

Back [date]. Thanks for understanding!
```

---

## Community Management Best Practices

### Responding to Issues

**Good issue response**:
```markdown
Thanks for reporting this, @frank!

I see the problem. It's in [module] where we [explanation].

To confirm: Does it happen [in situation X]?

If so, I have a fix in mind. Someone from the team (including 
community!) can submit a PR.

Thanks for using [project]!
```

**Closing without implementation**:
```markdown
Thanks for the report, @grace! I appreciate the detail.

However, this is a low-priority issue for us and we don't have 
bandwidth to fix it right now. 

**What would help:**
- A PR from the community
- Workaround: [alternative approach]
- Upvote on this issue if you want to help prioritize

Closing for now, but we'd welcome a PR!
```

### Welcoming First Contributors

```markdown
Great first contribution, @henry! Welcome! 

A couple of suggestions for next time:
1. [Feedback on code]
2. [Feedback on tests]

But overall, excellent work. Keep it up! 👏

See [CONTRIBUTING.md] for our process. Excited to see more from you.
```

### Handling Complaints/Anger

```markdown
I understand your frustration, @iris.

You're right that [problem]. We made a trade-off when we 
[decision] because [reasoning].

It wasn't perfect, and we're open to [alternative approach].

Can we discuss how to move forward in [issue/#123]?

Thanks for your patience.
```

---

## Documentation Updates

Keep these docs current:

**README**:
- [ ] Response SLA section updated
- [ ] Support channels documented
- [ ] Links to CONTRIBUTING, CODE_OF_CONDUCT clear

**CONTRIBUTING**:
- [ ] Setup instructions current
- [ ] Review expectations clear
- [ ] Link to style guide accurate

**GOVERNANCE**:
- [ ] Decision-making process documented
- [ ] Maintainer list current
- [ ] Vision/scope up-to-date

**MAINTAINERS.md**:
- [ ] Team list current
- [ ] Contact info accurate
- [ ] Responsibilities clear

**ROADMAP**:
- [ ] Next 3-6 months realistic
- [ ] Public backlog visible
- [ ] Community input welcome

---

## When You Need Help

If maintenance is becoming unsustainable:

**Options**:
1. **Add maintainers** - Share responsibility
2. **Request donations** - Fund time (GitHub Sponsors)
3. **Move to organization** - Community ownership
4. **Go dormant** - Pause development, accept PRs only
5. **Hand off** - Give project to someone more available
6. **Archive** - Close project responsibly

**Handing off**:
```markdown
## [Project] Maintenance Change

I'm stepping back as primary maintainer due to [reason].

[New maintainer] is taking over. They bring [relevant experience] 
and will be excellent stewards of this project.

Thanks to everyone who contributed and used [project]. It's been 
meaningful to maintain.

See [new maintainer] for future support.

- [Previous maintainer]
```

---

## Checklist for Your Team

- [ ] SLAs documented (response time, release cadence)
- [ ] Communication preferences documented
- [ ] How to say no decided (as team)
- [ ] Boundaries around consulting work set
- [ ] Maintainer time commitment realistic
- [ ] Backup maintainers (bus factor reduced)
- [ ] Burnout prevention discussed
- [ ] Time off process documented
- [ ] Community knows expectations

This is hard work, but sustainable open source starts with realistic expectations.
