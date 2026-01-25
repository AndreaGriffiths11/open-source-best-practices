# Choosing a License

Most people overthink licensing. Here's a straightforward guide.

## Quick Decision Tree

**Do you want people to use your code freely, with no restrictions?**
- Yes → **MIT License**
- No, I want commercial protection → **Apache 2.0**
- No, derivative work must stay open source → **GPL v3**

That covers 99% of cases.

---

## The Common Licenses

### MIT License

**What it does**: "Use this however you want. Just credit me."

**Allows**:
- Commercial use ✅
- Modification ✅
- Distribution ✅
- Private use ✅

**Requires**:
- License and copyright notice included ✅

**Restrictions**:
- None. Liability disclaimer is included.

**Best for**:
- Libraries you want widely adopted
- Personal projects
- Most open source projects
- When you don't care about commercial derivatives

**Examples using MIT**: React, jQuery, Node.js, Rails, Lua

**Complexity**: Simplest. One page.

---

### Apache License 2.0

**What it does**: "Use this freely. But if you modify it, you have to explain your changes and include a patent grant."

**Allows**:
- Commercial use ✅
- Modification ✅
- Distribution ✅
- Private use ✅

**Requires**:
- License and copyright notice included
- Statement of changes made
- Include NOTICE file (if provided)

**Restrictions**:
- Trademark use is restricted (you can't call your derivative product by the same name)
- Patent indemnification clause (if you sue them over patents, it nullifies the license)

**Best for**:
- Enterprise/commercial projects
- When you want patent protection
- If you've invested in the code and want some legal safety

**Why it's better than MIT for business**:
- Explicit patent grant (important if you hold patents)
- Trademark protection
- Still very permissive, but with guardrails

**Examples using Apache 2.0**: Kubernetes, Apache projects, Android (partial)

**Complexity**: Medium. More legal language.

---

### GPL v3 (GNU General Public License)

**What it does**: "Use this freely. But if you distribute it or use it in a product, your derivative must also be open source under GPL."

**This is "copyleft"** - freedom is contagious. If you use GPL code, your code must be GPL too.

**Allows**:
- Commercial use ✅
- Modification ✅
- Distribution ✅

**Requires**:
- Source code must be available
- Modifications must be documented
- License and copyright notice included
- If you distribute software using GPL code, you must provide source

**Restrictions**:
- You cannot make it proprietary
- Derivative work must use GPL v3
- If you sell software with GPL code, you must provide source (or offer to)

**Best for**:
- Protecting open source community
- When you want to ensure improvements stay public
- If you believe in "free software" (in the GNU sense)
- When you specifically don't want commercial entities to close-source derivatives

**Examples using GPL v3**: WordPress, GIMP, VLC, Linux Kernel (v2, technically)

**Complexity**: High. Lots of legal language. Strict enforcement.

**Warning**: Some companies avoid GPL because of the copyleft requirement. Affects adoption.

---

### Other Common Licenses

#### BSD 2-Clause / BSD 3-Clause
- Like MIT but slightly different legal language
- 2-Clause: simpler, BSD 3-Clause adds clause about endorsement
- Use MIT instead (simpler)

#### ISC License
- Functionally equivalent to MIT
- Use MIT instead (more recognizable)

#### LGPL (GNU Lesser GPL)
- Like GPL but less strict: libraries can be linked from proprietary software
- Rarely needed. Use MIT or Apache 2.0 instead.

#### Mozilla Public License 2.0 (MPL)
- Hybrid: if you modify the licensed file, it stays MPL
- But you can add proprietary files around it
- Good compromise between permissive and copyleft
- Most developers stick with MIT/Apache/GPL (less confusion)

#### AGPL v3
- Like GPL v3 but stricter: if you run the software as a service (SaaS), users have rights to the source
- Very restrictive. Avoid unless you specifically want to prevent SaaS companies from using your code without open-sourcing their service
- Very few projects use this

---

## Decision Scenarios

### "I'm building a library for others to use"

**Question 1: Do you work for a company?**
- Yes, and the company might use this in commercial products → **Apache 2.0** (legal protection)
- Yes, but it's just a utility tool → **MIT** (simpler, faster adoption)
- No, it's personal/hobby → **MIT** (simplest)

**Question 2: Do you care if companies build proprietary software on top?**
- I don't care → **MIT**
- I want their improvements to be open source too → **GPL v3**
- I want legal safety but they can keep improvements private → **Apache 2.0**

---

### "I'm open-sourcing internal company code"

Go with **Apache 2.0**:
- Clear patent indemnification (company lawyers like this)
- Trademark protection (company brand is protected)
- Still very permissive
- Industry standard for big tech companies

---

### "I'm releasing a framework (Django, Rails-like)"

Choose **MIT or Apache 2.0**:
- High adoption is important
- GPL would scare away some enterprise users
- MIT if you want maximum adoption
- Apache 2.0 if you're backed by a company

**Don't use GPL**—it would limit adoption for frameworks.

---

### "I'm building a development tool (linter, bundler, etc.)"

**MIT** for most cases:
- Developers prefer MIT
- Widespread adoption matters
- No strong reason to restrict usage

**Exception**: If you're explicitly trying to prevent commercial forks, consider GPL v3 (but this hurts adoption).

---

### "I'm releasing research code"

**MIT** or **Apache 2.0**:
- Academics prefer permissive licenses
- GPL creates issues for commercial follow-up research
- MIT is simplest

---

## Mixing Licenses

If your project depends on multiple licenses:

**Safe combinations**:
- MIT + MIT = OK (use MIT)
- MIT + Apache 2.0 = Use Apache 2.0 (it's stricter, compatible with both)
- MIT + GPL = Use GPL (copyleft applies to the whole thing)
- Apache 2.0 + GPL = Technically complex. Avoid this situation.

**Red flag**: Depending on GPL code in a proprietary project. GPL is contagious.

---

## How to Add a License

1. Go to your GitHub repo
2. Click "Add file" → "Create new file"
3. Name it `LICENSE` (or `LICENSE.md`)
4. GitHub shows templates. Select your license.
5. GitHub auto-fills the text with the correct year and author
6. Commit it

Or:

1. Visit [choosealicense.com](https://choosealicense.com)
2. Read the summary of each
3. Copy the full text
4. Paste into LICENSE file in your repo

---

## Remember

- **MIT**: "Use it, I don't care what you do with it"
- **Apache 2.0**: "Use it, but be upfront about changes and don't use my name for your version"
- **GPL v3**: "Use it, but if you distribute modifications, you must open-source them too"

Most projects use MIT. You're safe with that.

GitHub licenses are not legal advice. If your code has significant legal implications, talk to a lawyer. But for 99% of open source projects, pick MIT and move on.
