# Quick Start: Set Up Your GitHub Playbook This Week

**Timeline**: 2–3 hours total (spread across the week, not all at once)

---

## This Week's Mission

By Friday, you'll have:
- ✅ GitHub repo created (`hidden-realities-playbook`)
- ✅ Project files pushed to GitHub
- ✅ First story added (example or your own)
- ✅ Synced to Mac or second device
- ✅ Ready to start capturing stories

---

## Day 1 (Monday): Create GitHub Repo — 30 min

1. Go to **github.com** → sign in (or create free account)
2. Click **+** (top right) → **New repository**
3. Fill in:
   ```
   Repository name: hidden-realities-playbook
   Description: Real stories from implementing ISO 27001 ISMS. 
                A practitioner's guide to the hidden tasks nobody tells you about.
   Public ✓ (yes, public)
   Add a README file ✓
   Add .gitignore ✓ (select "Python")
   Choose a license ✓ (select "MIT License")
   ```
4. Click **Create repository**

**Done.** Your repo exists.

---

## Day 2 (Tuesday): Clone to Laptop — 20 min

Open Terminal (Mac) or Command Prompt (Windows):

```bash
# Navigate to where you want the folder
cd ~/Documents

# Clone the repo
git clone https://github.com/[YOUR-USERNAME]/hidden-realities-playbook.git

# Move into it
cd hidden-realities-playbook

# Verify it worked
ls -la
```

You should see folders and files appearing.

---

## Day 3 (Wednesday): Add Project Files — 30 min

**Option A: Using Terminal** (copy the files we created)
```bash
# If you can access /home/claude from your machine:
cp -r /home/claude/hidden-realities-playbook/* ~/Documents/hidden-realities-playbook/

# Or manually:
# Create folders
mkdir -p stories chapters teaser-posts resources

# Then copy individual files (I'll help)
```

**Option B: Manual Copy**
- Download the files from my outputs folder (I'll provide links)
- Copy them into your local `hidden-realities-playbook/` folder
- Your folder structure should match what I show below ✓

**Result**: Your laptop folder now has:
```
hidden-realities-playbook/
├── README.md
├── CONTRIBUTING.md
├── GITHUB_SETUP.md
├── LICENSE
├── stories/
│   └── 2026-08-15_discovery-documentation-gaps.md (example)
├── chapters/
├── teaser-posts/
└── resources/
    ├── story-template.md
    ├── GITHUB_WORKFLOW.md
    ├── SETUP_GUIDE.md
    ├── TEASER_STRATEGY.md
    ├── PROJECT_CHARTER.md
    └── Playbook_Story_Capture.xlsx
```

---

## Day 4 (Thursday): Commit & Push to GitHub — 15 min

```bash
# Go to your repo folder
cd ~/Documents/hidden-realities-playbook

# Check what changed
git status

# Stage all changes
git add .

# Commit
git commit -m "Initial commit: Set up playbook project structure and documentation"

# Push to GitHub
git push origin main

# Done! Check github.com/[your-username]/hidden-realities-playbook
```

Go to your repo on GitHub. You should see all the files now.

---

## Day 5 (Friday): Clone to Mac + Add First Story — 25 min

### Clone to Mac
```bash
# Open Terminal on Mac
cd ~/Documents

# Clone the repo
git clone https://github.com/[YOUR-USERNAME]/hidden-realities-playbook.git

# Verify it's the same as laptop
ls -la hidden-realities-playbook/
```

### Add Your First Story
**Option A: Use the Example** (fastest)
- It's already in `/stories/2026-08-15_discovery-documentation-gaps.md`
- Just leave it there

**Option B: Add Your Own Story** (better)
1. Open `resources/story-template.md` (read it)
2. Create new file: `stories/2026-09-05_your-story-title.md`
3. Copy template content
4. Fill in your real story (15–20 min, rough is fine)
5. Save

### Commit & Push
```bash
# From Mac
cd ~/Documents/hidden-realities-playbook

# Add your new story
git add stories/2026-09-05_your-story-title.md

# Commit
git commit -m "Add story: [Your Story Title]"

# Push
git push origin main

# Check github.com — your story should be there!
```

---

## End of Week: You're Live

**Check**:
- [ ] GitHub repo created (public)
- [ ] All files pushed (visible on GitHub.com)
- [ ] Cloned to laptop
- [ ] Cloned to Mac
- [ ] First story added
- [ ] Story pushed to GitHub

**If everything is there, you're done.**

Send me the link: `github.com/[your-username]/hidden-realities-playbook`

I'll verify it and we're ready to capture stories.

---

## Next Week: Start Capturing

- Add a story based on something that happened in your ISMS project this week
- Use `resources/story-template.md` as your guide
- Commit and push it to GitHub
- That's your rhythm: capture → commit → push (weekly or as stories emerge)

---

## If Something Goes Wrong

### "Permission denied when pushing"
- You haven't authenticated GitHub on this machine
- **Solution**: Use GitHub Desktop (handles auth automatically)
- Or: Email me, I'll walk you through git config

### "Files aren't showing up on GitHub.com"
- You pushed but GitHub didn't update
- **Solution**: Hard refresh (Cmd+Shift+R on Mac) or wait 5 seconds

### "Merge conflict"
- You edited the same file on two devices
- **Solution**: Use GitHub Desktop (handles this gracefully)
- Or: Email me, we'll resolve it

### "I can't clone to Mac"
- You either can't authenticate or the link is wrong
- **Solution**: Copy-paste the link from github.com/[your-username]/hidden-realities-playbook (green "Code" button)

---

## Pro Tip: Use GitHub Desktop

If terminal feels overwhelming, download **GitHub Desktop** (free):

1. Go to **github.com/desktop**
2. Download for Mac/Windows
3. Sign in with GitHub account
4. Click "Add" → "Clone Repository"
5. Find `hidden-realities-playbook`
6. Choose folder location
7. **From then on**: Click buttons instead of typing commands

GUI version:
- Click folder icon to open files
- See changes (red/green highlighted)
- Type commit message
- Click "Commit" and "Push"

Much easier than terminal for beginners.

---

## Your GitHub Rhythm (Going Forward)

### Weekly
- Add 1 story (`stories/YYYY-MM-DD_slug.md`)
- Commit + push (`git push origin main`)
- Story is now on GitHub

### Monthly (1st Friday)
- Pull latest stories: `git pull origin main`
- Send me message: "September playbook sync — X new stories"
- I review, draft teaser posts, we discuss
- Update story statuses in the files

### Quarterly (End of each quarter)
- Outline chapters
- Start drafting playbook
- Plan for launch

---

## That's It

You've got this. It's just:
- **Day 1**: Create repo (GitHub.com)
- **Day 2**: Clone to laptop (Terminal)
- **Day 3**: Copy files (Finder or Terminal)
- **Day 4**: Push to GitHub (Terminal)
- **Day 5**: Clone to Mac (Terminal)

One hour each day (or all at once if you prefer). By Friday, you're live.

---

## Questions?

- Stuck on a step? Ask me.
- Terminal feels weird? Use GitHub Desktop.
- Need help copying files? I'll provide download links.
- Anything else? Send a message.

You're building something real. This is just infrastructure to make it easier.

**Let's go.**
