# Contributing to Hidden Realities

## How to Capture a Story

### Step 1: Use the Template
1. Copy `resources/story-template.md`
2. Name it: `YYYY-MM-DD_your-story-slug.md`
3. Example: `2026-08-15_discovery-documentation-gaps.md`

### Step 2: Fill in the Sections
Go through each section of the template:
- **The Assumption**: What did you think would happen?
- **The Reality**: What actually happened?
- **Why It Matters**: Why does this gap matter?
- **The Decision**: What did you decide to do?
- **The Lesson**: What should someone else know?
- **Time Investment**: How long did this take?
- **Context**: Any other details
- **Related Stories**: Other stories this connects to

**Keep it rough.** Don't polish yet. 15–20 minutes per story is the goal.

### Step 3: Save & Commit
1. Save the file to `/stories` folder
2. Open Terminal/Git and run:
   ```bash
   cd hidden-realities-playbook
   git add stories/YYYY-MM-DD_your-story-slug.md
   git commit -m "Add story: [Story Title]"
   git push origin main
   ```

### Step 4: Notify Me
Send a message in Claude: "New story added: [story title] — check `/stories/YYYY-MM-DD_slug.md`"

---

## When to Capture a Story

### Good Triggers
- **You discover something that contradicts the standard** (e.g., "ISO says organize this way; our org does it totally different")
- **A task takes way longer than expected** (you learn why hidden work exists)
- **A stakeholder resists or surprises you** (reveals why people don't care about security)
- **You have to redo something** (the first approach didn't work)
- **You solve a problem in a creative way** (others could learn from it)

### Examples
- "Found 47 undocumented processes"
- "Our document storage is a mess"
- "Finance team won't use the template we created"
- "Had to reformat 200 documents because the standard format wasn't right"
- "Senior leadership finally cared when we tied security to audit risk"

---

## Story Guidelines

### What Makes a Good Story
1. **Real**: It happened in your project (not hypothetical)
2. **Specific**: Names dates, numbers, team dynamics
3. **Honest**: You don't pretend to know something you don't
4. **Actionable**: Someone can learn from it and do something differently
5. **Anonymized**: No real company names, people names, or sensitive data

### What NOT to Do
- Don't include confidential data
- Don't name people (use roles instead: "Finance lead", "IT director", etc.)
- Don't name the company (use "the org", "my company", "the department")
- Don't share trade secrets or financial data
- Don't make it up

### Anonymization Examples
- ❌ "Sarah in Finance refused to document her processes"
- ✅ "The Finance lead initially resisted documenting ad-hoc procedures"

- ❌ "Acme Corp uses 4 different document storage systems"
- ✅ "The organization had documents scattered across 4 different storage systems"

- ❌ "Revenue process: Take the CSV from SAP, upload to SharePoint, email PDF to billing"
- ✅ "A critical financial control involved manual data transfer between 3 systems with no audit trail"

---

## Story Status Workflow

As you work on a story, move it through these statuses:

| Status | Meaning |
|--------|---------|
| **Raw** | First draft, rough notes captured (you just added it) |
| **Drafted** | I've reviewed it, proposed a teaser post, you've filled in gaps |
| **Reviewed** | We've discussed it, it's polished, ready for publishing |
| **Ready** | Approved for LinkedIn teaser or playbook chapter |
| **Published** | Story has been published on LinkedIn or in a chapter |

**Update the status line** when you make changes:
```markdown
**Status**: Raw → Drafted → Reviewed → Ready → Published
```

---

## Monthly Workflow

### First Friday of Each Month (Sync Day)

1. **You**: Add any new stories from the past month to `/stories`
2. **You**: Commit and push to GitHub
3. **You**: Send me a message: "September playbook sync — [# of new stories] added"
4. **Me**: Review all new stories in `/stories`
5. **Me**: Identify patterns + strongest stories
6. **Me**: Draft 2–3 teaser post options in `/teaser-posts`
7. **We**: Discuss which posts to publish
8. **You**: Update story statuses to "Reviewed" or "Ready"
9. **You**: Push final versions, I publish LinkedIn posts

---

## File Naming Convention

Stories go in `/stories/` with consistent naming:

```
YYYY-MM-DD_story-slug.md

Examples:
- 2026-08-15_discovery-documentation-gaps.md
- 2026-08-22_legacy-format-mess.md
- 2026-09-05_stakeholder-resistance-finance.md
- 2026-09-12_storage-consolidation.md
```

**Slug** (the part after the date):
- Use hyphens to separate words
- 2–5 words
- Describe the story in short form
- Keep it lowercase

---

## GitHub Basics (Quick Cheat Sheet)

### First Time Setup
```bash
# Clone the repo
git clone https://github.com/[your-username]/hidden-realities-playbook.git
cd hidden-realities-playbook

# Check your status
git status
```

### Every Time You Add a Story
```bash
# See what changed
git status

# Stage your new story file
git add stories/YYYY-MM-DD_story-slug.md

# Commit with a message
git commit -m "Add story: [Story Title]"

# Push to GitHub
git push origin main
```

### See Your History
```bash
# See recent commits
git log --oneline

# See all your stories
ls -la stories/
```

---

## Asking Questions

### If You're Stuck
1. Check `resources/story-template.md` again
2. Look at published stories in `/stories` for examples
3. Ask me in Claude: "How do I structure this story?" or "Is this anonymized enough?"

### If You Want to Suggest a Topic
Open a GitHub Issue:
1. Go to your repo → Issues → New Issue
2. Title: "Story idea: [topic]"
3. Description: What you're curious about
4. I'll respond with thoughts

---

## How Your Stories Become the Playbook

1. **You capture** raw stories (15–20 min each)
2. **I synthesize** monthly (identify patterns, flag strongest stories)
3. **We draft** teaser posts (LinkedIn; builds audience)
4. **We outline** playbook structure (which stories go in which chapters)
5. **I draft chapters** pulling multiple related stories + tools
6. **We review** and polish
7. **We launch** playbook (Jan 2027) + sell to audience

---

## Questions?

- Anything unclear about the template?
- How to use GitHub (if new to it)?
- When to capture stories?
- How to anonymize something?

Send me a message. Happy to help.

---

## Thanks for Contributing

Every story you capture is real experience that helps practitioners. You're building something that solves an actual problem. That matters.

Keep it real. Keep it honest. The rough version is perfect.
