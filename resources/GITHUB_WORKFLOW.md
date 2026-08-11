# GitHub as Your Playbook Sync & Workflow Tool

This is how GitHub replaces the Google Drive/Excel approach and becomes your central repository for the entire playbook project.

---

## Why GitHub (Not Just Google Drive)?

### Google Drive/Excel ✅ Good For
- Shared editing in real-time
- Simple drop-in-and-forget storage

### GitHub ✅ Better For
- **Version control**: See the history of every story (who wrote what, when, why)
- **Single source of truth**: One place for all project files (stories, posts, chapters, resources)
- **Writing-native format**: Markdown is better for long-form stories than Excel cells
- **Collaboration**: Easy to review, comment, suggest changes
- **Portfolio**: Public repo shows you're actively building something (credibility)
- **Free & unlimited**: No file limits, no subscription costs
- **Professional**: This is how real projects are managed

### Comparison Table

| Feature | Google Drive | Excel | GitHub |
|---------|--------------|-------|--------|
| Cross-device sync | ✅ Yes | ✅ Yes (via Drive) | ✅ Yes |
| Version history | ✅ Basic | ✅ Basic | ✅✅ Full version control |
| Easy story editing | ❌ Not really | ❌ Awkward in cells | ✅✅ Native markdown |
| Collaborative review | ✅ Comments | ✅ Comments | ✅✅ PR reviews, suggestions |
| Public portfolio | ❌ Private | ❌ Private | ✅✅ Show your work |
| Free | ✅ Yes | ❌ Requires Office 365 | ✅ Yes (public) |
| Open to community | ❌ No | ❌ No | ✅ People can follow, star, engage |

**Bottom line**: For a playbook built in public, GitHub is the better home.

---

## Your GitHub Workflow (Simplified)

### Weekly: Add a Story

**On Laptop (or Mac—doesn't matter)**
1. Create new file: `stories/2026-09-XX_story-title.md`
2. Copy template from `resources/story-template.md`
3. Fill in the 7 sections (rough is fine)
4. Save the file

**Terminal (1 minute)**
```bash
cd ~/Documents/hidden-realities-playbook
git add stories/2026-09-XX_story-title.md
git commit -m "Add story: [Story Title]"
git push origin main
```

**Done.** Your story is now:
- On GitHub (backed up, safe)
- Accessible from any device (laptop, Mac, phone, anywhere)
- Part of the version history
- Visible to anyone who follows your repo

### Monthly: Synthesis & Posts (1st Friday)

**You**
1. Pull latest changes from GitHub (get all new stories)
2. Send message: "September playbook sync — 4 new stories added"

**Me**
1. Review all stories in `/stories`
2. Identify patterns + strongest ones
3. Draft 2–3 teaser posts in `/teaser-posts` folder
4. Commit them to GitHub

**We discuss**
- Which posts to publish
- What to edit
- What's next

**You**
1. Review my drafts
2. Edit/approve
3. Copy to LinkedIn
4. Update story status: "Raw" → "Reviewed" → "Ready" → "Published"

---

## File Organization in GitHub

```
hidden-realities-playbook/
│
├── README.md                           # Project overview (people see this first)
├── CONTRIBUTING.md                     # How to capture stories
├── GITHUB_SETUP.md                     # Setup instructions
├── LICENSE                             # MIT license
│
├── stories/                            # Raw story captures
│   ├── 2026-08-15_discovery-docs-gaps.md
│   ├── 2026-09-05_legacy-format-mess.md
│   ├── 2026-09-12_stakeholder-resistance.md
│   └── ... (one new story per week)
│
├── teaser-posts/                       # LinkedIn post drafts
│   ├── 2026-09-02_intro-post.md
│   ├── 2026-09-09_value-prop-post.md
│   ├── 2026-09-16_story-1-teaser.md
│   └── published/                      # Archive of published posts
│       └── 2026-09-02_intro-post.md
│
├── chapters/                           # Playbook chapter drafts (starts Nov)
│   ├── 00-introduction.md
│   ├── 01-discovery-assessment.md
│   ├── 02-legacy-documentation.md
│   └── ... (filled in during drafting phase)
│
└── resources/                          # Reference materials
    ├── story-template.md               # Copy this to create new stories
    ├── SETUP_GUIDE.md
    ├── TEASER_STRATEGY.md
    ├── PROJECT_CHARTER.md
    ├── GITHUB_WORKFLOW.md              # This file
    └── Playbook_Story_Capture.xlsx     # Backup of Excel tracker
```

---

## Cross-Device Workflow Example

### Scenario: You're Working on Laptop Monday, Mac Friday

**Monday (Laptop)**
1. Had a breakthrough in GR3 workshop
2. Sit down, create story file: `2026-09-05_discovery-breakthrough.md`
3. Fill in template (rough draft, 15 min)
4. Commit and push:
   ```bash
   git add stories/2026-09-05_discovery-breakthrough.md
   git commit -m "Add story: Discovery workshop breakthrough"
   git push origin main
   ```
5. **Story is now on GitHub** (backed up, safe)

**Friday (Mac)**
1. Open Terminal:
   ```bash
   cd ~/Documents/hidden-realities-playbook
   git pull origin main
   ```
2. You now have the story from Monday on your Mac
3. Read it, think about it over coffee
4. Add notes or polish
5. Commit again:
   ```bash
   git add stories/2026-09-05_discovery-breakthrough.md
   git commit -m "Polish story: Add context"
   git push origin main
   ```

**Monday Next Week (Laptop)**
1. Pull again:
   ```bash
   git pull origin main
   ```
2. You have your Mac edits + any new stories from Friday

**GitHub.com (Public)**
- Anyone following your repo sees all of this
- They see the progression: raw → polished → published
- Builds credibility: "Look, they're actively working on this"

---

## Advantages of GitHub Over Excel

### 1. Stories Are Readable Online

**Excel**:
- Email the file → people open it → it's in a spreadsheet cell → hard to read

**GitHub**:
- Go to github.com/[your-username]/hidden-realities-playbook
- Click `/stories/`
- Click a story
- **It's beautifully formatted, easy to read, sharable as a link**

Example: `github.com/[you]/hidden-realities-playbook/blob/main/stories/2026-08-15_discovery-docs-gaps.md`

You can share that link on LinkedIn, and people read the story directly.

### 2. Version History

**Excel**:
- You edit story 1.0 → email me → I edit → Version 1.2 back to you
- Confusing filenames: `Story_FINAL_v2_actual_final_IQBAL_EDITS.xlsx`

**GitHub**:
- Story is in one place
- Click "History" and see every edit, every commit
- Revert to old version if needed
- Comments on specific lines

### 3. Collaborative Editing

**Excel**:
- You send me the file → I edit it → send back → you merge changes

**GitHub**:
- I create a draft post in `/teaser-posts/`
- You comment directly on the file (line-by-line)
- We iterate without sending files back and forth

### 4. Public Portfolio

**Excel**:
- Private folder only people you share with see

**GitHub**:
- Public repo (you can choose)
- Shows up in your GitHub profile
- Employers/clients see: "Oh, they're actively building a playbook"
- Search engines eventually index it

### 5. Community Engagement

**Excel**:
- Static, isolated

**GitHub**:
- People can "Star" your repo (like, bookmark it)
- People can "Watch" it (get notified when you add stories)
- People can open Issues (e.g., "Can you cover X topic?")
- Later: people might contribute their own stories

---

## Setting Up Once, Using Everywhere

### Day 1 (One-Time Setup)
1. Create GitHub repo (5 min, on any device)
2. Clone to laptop (5 min)
3. Clone to Mac (5 min)

### From Then On
1. **Laptop**: Add story → commit → push
2. **Mac**: Pull → see story → edit → push
3. **Laptop**: Pull → see Mac edits
4. **GitHub.com**: See everything (public version)

**That's it.** No sync issues, no version conflicts (if you follow simple rules).

---

## Simple Rules to Avoid Conflicts

1. **Commit before switching devices**
   - Done on laptop? `git push`
   - Going to Mac? `git pull` first

2. **Pull before you work**
   ```bash
   git pull origin main
   ```

3. **Edit different files on different devices** (or the same files at different times)
   - You can't edit the same story on laptop AND Mac at the same time
   - But you can edit Story A on laptop, Story B on Mac, no problem

4. **Use "main" branch** (don't worry about advanced GitHub stuff)

---

## Recommended Tools

### For Command Line
- **Mac/Linux**: Terminal (built-in) ✅
- **Windows**: Git Bash (free download)

### For GUI (Easier)
- **GitHub Desktop** (github.com/desktop) — Easiest, free
  - No terminal commands
  - Click buttons to add/commit/push
  - See changes visually

### For Editing Stories
- **VS Code** (free) — write in markdown, nice formatting
- **Markdown editor** (Markdownify, MacDown) — cleaner than Word
- **Nano/Vim** (terminal) — if you're comfortable with it
- **Literally any text editor** — plain text files, works anywhere

---

## FAQ: GitHub Concerns

### Q: Is GitHub complicated?
**A**: Not for your use case. You're doing:
- Add files
- Commit
- Push
- Pull

That's 80% of what GitHub does. Use GitHub Desktop if terminal feels scary.

### Q: What if I make a mistake?
**A**: GitHub has full history. You can:
- Revert to old version
- Undo a commit
- Ask me for help

No data is ever truly lost on GitHub.

### Q: Do people have to see my repo?
**A**: No. Create it as **Private** if you want. But **Public** is better for:
- Building audience (people can follow)
- Credibility (showing active work)
- Portfolio (shows in your GitHub profile)

You can also make it public later (when it's polished).

### Q: What if I want to keep some stories private?
**A**: Use `.gitignore`. Create a `_private/` folder:
```markdown
# .gitignore
_private/
```

Files in `_private/` won't be pushed to GitHub. Keep raw drafts there, move to `/stories` when ready.

### Q: GitHub is free forever?
**A**: Yes. Public repos are free and unlimited. (Private repos: free with limits, or paid for unlimited.)

---

## Switching from Excel to GitHub

### Keep the Excel Workbook?
**Yes**, keep it in `/resources/` as a backup:
- Track progress (stories captured, statuses)
- Dashboard (followers, engagement)
- Not your primary workflow, but nice for metrics

### Stop Using Google Drive for Story Sync?
**Yes**. GitHub is now your single source of truth.

### But What About Monthly Uploads to Claude?
**Same thing, easier**:
- Instead of uploading Excel: send GitHub link
- I access the repo directly (no file upload needed)
- I see all stories, latest versions, history
- Faster, cleaner, no version confusion

---

## Transition Week

**This week**:
1. Create GitHub repo (`hidden-realities-playbook`)
2. Copy all files we created into it
3. Commit and push
4. Test: Clone to Mac (or other device)
5. Add first story
6. Commit, push, pull on other device
7. Confirm it works

**Next week**:
- Start adding stories to GitHub (instead of Excel)
- Use GitHub as your source of truth
- Keep Excel as a metrics dashboard (optional)

---

## You're Ready

GitHub is the professional, scalable home for your playbook project.

It's also **public**, which means:
- People see you working
- Stories can go viral on LinkedIn
- Builds credibility (active, transparent, real)
- Community can engage

That's the real power here. Not just storage, but a signal to the world: "I'm building something real, and I'm showing my work."

---

## Next Steps

1. Read `GITHUB_SETUP.md` (step-by-step repo creation)
2. Create the repo
3. Clone to laptop + Mac
4. Add your first story using `resources/story-template.md`
5. Push it
6. Send me the GitHub link
7. We're live

Questions? Ask. GitHub clicks once you've done it once.
