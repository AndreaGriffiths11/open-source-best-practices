# GitHub Sponsors Setup & Sustainability

Guide for setting up GitHub Sponsors and building sustainable funding for your open source project.

---

## Why GitHub Sponsors?

GitHub Sponsors connects your work to funding:

- **Sustainable maintenance**: Fund one day/week of dedicated work
- **Support infrastructure**: Pay for servers, CI/CD, tools
- **Full-time work**: Some projects fund entire teams
- **No platform fees**: GitHub doesn't take a cut
- **Integrated**: Sponsorship links right in your repo

Most successful projects use Sponsors + OpenCollective + other sources.

---

## Setting Up GitHub Sponsors

### Step 1: Enable Sponsors on Your Profile

1. Go to GitHub Settings > Sponsors
2. Click "Set up Sponsors"
3. Choose a funding method:
   - **Stripe**: Direct bank deposits (0% fee)
   - **PayPal**: Adds ~3% fee
4. Set up business info (bank account or Stripe Connect)
5. Complete verification (takes 1-5 days)

### Step 2: Define Your Sponsorship Profile

**Bio / About**:
```
[Your Name]

I maintain [Project Name], an open source [what it does].

With your support, I can:
- Dedicate more time to maintenance
- Fix bugs faster
- Build new features
- Keep infrastructure running

Thank you for supporting open source!
```

**Why Sponsorship Matters**:
```
Maintaining [Project] takes ~10 hours/week across:

- Code reviews and PR merges
- Issue triage and support
- Security updates and patches
- Performance improvements
- Documentation and examples
- Infrastructure (servers, CI/CD)

Right now this is all volunteer. With sponsorship, I can:
- Dedicate 1 day/week to maintenance (current: after hours)
- Reduce response times (current: 1-2 weeks)
- Implement community-requested features faster
- Keep infrastructure funded

Every $$ goes directly to maintaining [Project].
```

### Step 3: Define Sponsorship Tiers

Keep tiers simple. Most projects have 3-5 tiers.

**Template**:

```
$5/month: Supporter
- Your name/username in README
- Credit in monthly newsletter
- Feel-good sponsorship

$25/month: Contributor
- ↑ Supporter benefits
- Priority issue triage (48-hour response)
- Early access to RFC discussions
- Monthly updates via email

$100/month: Sponsor
- ↑ Contributor benefits
- Monthly 30-minute office hours (group, no consultation)
- Early access to releases (2 days before public)
- Sponsor badge in docs
- Feature prioritization (vote on next features)

$500/month: Enterprise
- ↑ Sponsor benefits
- Dedicated Slack channel (shared with other enterprise sponsors)
- Quarterly strategy calls
- Custom features (if aligned with vision)
- Logo in README and website

Custom amount:
- Contact for custom arrangement
```

### Tier Best Practices

**What Works**:
- ✅ Clear benefits at each level
- ✅ Benefits scale with price
- ✅ Concrete deliverables ("monthly updates", "priority triage")
- ✅ Group benefits ("office hours with others", not 1-on-1 consulting)
- ✅ Recognition (names/logos, not secret benefits)
- ✅ Custom tier for enterprise

**What Doesn't Work**:
- ❌ Vague benefits ("more features", "faster support")
- ❌ Too many tiers (7+ is overwhelming)
- ❌ Expensive benefits (office hours at $10/month is unsustainable)
- ❌ One-on-1 consulting (not scalable)
- ❌ Feature guarantees (what if it's hard?)
- ❌ No clear difference between tiers

### Example: Well-Designed Tiers

```
$3/month: Coffee ☕
- Sponsor badge in README
- Credit in release notes

$10/month: Lunch 🍔
- ↑ Coffee benefits
- Sponsor list in docs
- Ad-free access to community Slack

$50/month: Vacation 🏖️
- ↑ Lunch benefits
- Monthly email with progress updates
- Vote on next quarter's priorities
- Early access to releases

$200/month: Professional 💼
- ↑ Vacation benefits
- Logo in README (if 3+ months)
- Quarterly sync call with maintainers
- Custom feature consultation (within scope)

Custom: Let's talk!
- Contact us for your needs
```

---

## Adding Sponsorship Links to Your Project

### README Sponsor Section

```markdown
## Supporting This Project

[Project Name] is maintained by volunteers. If it's valuable to you, 
please consider sponsoring to fund ongoing maintenance.

[![Sponsor @alice on GitHub Sponsors](https://img.shields.io/github/sponsors/alice?style=social)](https://github.com/sponsors/alice)

Your support enables:
- Faster bug fixes and security updates
- New features and improvements
- Dedicated maintenance time
- Infrastructure costs

[Become a Sponsor](https://github.com/sponsors/alice)
```

### Repo Sidebar

GitHub lets you add a funding link in repo settings:

1. Go to repo Settings > "Funding links"
2. Add: `github: alice`
3. Optionally add: `custom: https://opencollective.com/project`
4. Shows as "Sponsor" button in repo sidebar

### Profile README

If you maintain multiple projects:

```markdown
# Hi, I'm [Name]

I maintain several open source projects including [Project A], [Project B], and [Project C].

If you use my projects, consider sponsoring to support continued development:

[![Sponsor me on GitHub](https://img.shields.io/github/sponsors/alice?style=social)](https://github.com/sponsors/alice)

[Become a Sponsor](https://github.com/sponsors/alice) | [All Projects](...)
```

### CONTRIBUTING or SPONSORS.md

```markdown
## Support This Project

This project is maintained by volunteers. If it's valuable to you:

[Become a Sponsor](https://github.com/sponsors/alice)

### What Your Sponsorship Enables

- **$500/month needed** to fund 1 day/week maintenance
- **$1500/month** would fund 3 days/week (close to full-time)
- **$5000/month** would fund full-time maintenance + infrastructure

Current status: [X sponsors, $Y/month, funding Z%]

See [GitHub Sponsors](https://github.com/sponsors/alice) for details.
```

---

## Transparency: How You Use Funds

Be honest about what sponsorship pays for.

### Monthly Update to Sponsors

Send via email or GitHub Sponsors update feature:

```markdown
## [Project] Sponsorship Update - [Month]

Hi sponsors! 👋

Thanks for supporting [Project]. Here's what your contributions funded this month:

### Work Done ($X hours)
- PR reviews: X hours (reviewed Y PRs)
- Issue triage: X hours (closed/prioritized Z issues)
- Bug fixes: X hours (fixed W bugs)
- Documentation: X hours (wrote/updated X pages)
- Security updates: X hours (patched Y vulnerabilities)

### Infrastructure
- Server costs: $X
- CI/CD: $X (GitHub Actions free, but used $X credit)
- Tools: $X (monitoring, testing, etc.)

### What's Next
Working on [Feature A] and [Feature B] based on sponsor feedback.

### Sponsors This Month
Welcome [New Sponsor 1] and [New Sponsor 2]!

Thank you all for supporting open source! 🙌

[Maintainer Name]
```

### Sponsorship Goals

Make goals visible and specific:

```markdown
## Sponsorship Goals

### 🎯 Current: $Y/month ($500 goal for 1 day/week)

**$500/month**: I can dedicate 1 day/week (8 hours) to [Project]
- Faster bug fixes (48-hour turnaround)
- Monthly feature releases
- Prompt security updates

**$1000/month**: 2 days/week
- Weekly releases
- Proactive security audits
- Better documentation
- Community mentoring

**$2000/month**: 4 days/week (nearly full-time)
- Daily releases (if needed)
- Professional-grade infrastructure
- Dedicated community manager
- Potential to hire additional maintainer

Help us reach [next goal]! [Sponsor](link)
```

### Annual Transparency Report

Share yearly what you did with funds:

```markdown
# 2024 Sponsorship Report

## Income
- GitHub Sponsors: $12,000
- OpenCollective: $3,000
- Patreon: $1,500
- **Total: $16,500**

## Expenses

### Maintainer Time: $10,000
- My time: $10/hour × 1000 hours (undermarket rate)
- ~1 day/week maintenance

### Infrastructure: $4,000
- Server: $2,000
- CI/CD: $1,000
- Tools & services: $1,000

### Total Spent: $14,000
**Surplus: $2,500** (building rainy day fund)

## Impact

This year we:
- Merged 150 PRs (50% from community)
- Fixed 200 bugs
- Added 5 major features
- Served 500,000+ installations
- Maintained 99.9% uptime

## Future Plans

2025 goals:
- Hire part-time reviewer ($8k/year)
- Improve documentation ($2k/year)
- Maintain emergency fund ($2k/year)

Thanks to [number] sponsors who made this possible! 🙏
```

---

## Communication with Sponsors

### Monthly/Quarterly Email

Set up scheduled emails to sponsors:

```markdown
[Month] [Project] Update

Hi [Sponsor Name] 👋

Thank you for sponsoring [Project]!

### This Month
- Fixed [X] bugs
- Merged [Y] PRs
- Released [version]

### Looking Ahead
Working on [features].

### Recognition
Welcome new sponsors: [names]

Thanks for your support!
- [Maintainer]
```

### Thank You Notes

For larger sponsors ($100+), send personal notes:

```markdown
Hi [Sponsor Name],

I wanted to personally thank you for sponsoring [Project]. 

Your support directly funded:
- [Specific feature/fix]
- [Time I spent on maintenance]
- [Infrastructure cost]

This means a lot to me and the community. I'm committed to making 
[Project] the best it can be.

If you have requests or feedback, I'd love to hear it.

Thanks again!
- [Maintainer Name]
```

### Sponsor-Only Content (Optional)

Some projects offer sponsor-exclusive updates:

```markdown
## Sponsor Update: October (Sponsor-only email)

Hi [Sponsor Name],

Thanks for your ongoing support. Here's what else is happening:

### Unreleased Features
- [Feature A] - launching next week
- [Feature B] - in progress

### Security Issues Fixed
- [Security issue] - patched in next release

### Roadmap Preview
Q1 2025 we're focusing on [X], [Y], [Z]

### Special Thanks
Huge thanks to [Company X] sponsor for funding [Feature]. 🙏
```

---

## Multiple Funding Sources

Don't rely on GitHub Sponsors alone:

### Recommended Mix

```
GitHub Sponsors:        40% (direct)
OpenCollective:         30% (no platform fee option)
Patreon:               20% (recurring)
One-time donations:    10% (via stripe)
```

### Linking Multiple Sponsors

In repo sidebar (FUNDING.yml):

```yaml
github: [username]
patreon: [patreon-name]
opencollective: [project-name]
custom: https://donate.example.com
```

In README:

```markdown
## Support

- [GitHub Sponsors](https://github.com/sponsors/alice) - Monthly support
- [OpenCollective](https://opencollective.com/project) - Company matching
- [Patreon](https://patreon.com/alice) - Monthly pledges
- [One-time donation](https://donate.stripe.com) - Help with specific feature
```

---

## Sponsorship Tiers Template (Copy & Paste)

Use this as starting point:

```markdown
# GitHub Sponsors

I maintain [Project], an open source [description].

## How Your Support Helps

With your sponsorship, I can:
- Dedicate more time to bug fixes and features
- Keep infrastructure running
- Respond to issues faster
- Support the community better

## Current Status

**$[X]/month** of $[Y] goal (fund 1 day/week maintenance)

## Sponsorship Tiers

### $5/month - Supporter
- Sponsor badge in README
- Credit in release notes

### $25/month - Contributor  
- ↑ All above benefits
- Priority issue triage
- Early access to features
- Monthly email updates

### $100/month - Sponsor
- ↑ All above benefits  
- Monthly group office hours
- Early releases (2 days before public)
- Priority feature voting
- Logo in README

### $500/month - Enterprise
- ↑ All above benefits
- Dedicated Slack channel
- Quarterly strategy calls
- Custom feature consultation

### Custom - Let's Talk
Contact for custom arrangements.

## Thank You!

Every sponsor makes a difference. Thank you for supporting 
open source development! 🙏

[See more info](SPONSORS.md)
```

---

## Checklist: Sponsorship Setup

- [ ] GitHub Sponsors profile created
- [ ] Profile bio clear and compelling
- [ ] Why sponsorship matters documented
- [ ] Sponsorship tiers defined (3-5 tiers)
- [ ] Clear benefits for each tier
- [ ] Sponsor button in repo sidebar
- [ ] Sponsor link in README
- [ ] Plan for communicating with sponsors
- [ ] Plan for fund transparency
- [ ] Alternative funding sources linked (OpenCollective, Patreon)
- [ ] SPONSORS.md or equivalent created
- [ ] Monthly email to sponsors (scheduled)
- [ ] Annual transparency report planned

---

## Red Flags & Cautions

❌ **Don't promise what you can't deliver**
- No guaranteed features from sponsorship
- No one-on-one consulting bundled
- Realistic about your time

❌ **Don't give up control of the project**
- Sponsorship funds time, not direction
- You still make final decisions
- Money doesn't equal voting rights

❌ **Don't neglect non-sponsors**
- Feature benefits are public
- Releases public for everyone
- Don't create "sponsor-only" version

❌ **Don't disappear after getting funding**
- Actually use funds as described
- Report transparently on spending
- Communicate regularly with sponsors

✅ **Do be honest**
- Real explanation of what funds do
- Transparent spending
- Realistic about your availability

✅ **Do engage sponsors**
- Monthly updates
- Respond to feedback
- Thank them genuinely

✅ **Do keep the project healthy**
- Use funds as promised
- Publish open transparency reports
- Maintain community trust
