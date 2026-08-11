# Setting Up Your GitHub Repository

## Step 1: Create the Repository (GitHub.com)

1. Go to **[github.com](https://github.com)** and log in (or create an account)
2. Click **+** in the top right → **New repository**
3. Fill in:
   - **Repository name**: `hidden-realities-playbook`
   - **Description**: "Real stories from implementing ISO 27001 ISMS. A practitioner's guide to the hidden tasks and organizational complexities nobody tells you about."
   - **Public** or **Private** (choose **Public** if you want followers to see it; **Private** if you want to keep it just for yourself for now)
   - ✅ **Add a README file** (you'll replace it with ours)
   - ✅ **Add .gitignore** → select **Python** (or **Node** if you use Node; doesn't matter much)
   - ✅ **Choose a license** → **MIT License** (open, allows sharing/adaptation)
4. Click **Create repository**

---

## Step 2: Set Up Locally on Your Laptop

Open Terminal (Mac) or Command Prompt (Windows) and run:

```bash
# Navigate to where you want the folder
cd ~/Documents
# or: cd /Users/[yourname]/Documents

# Clone the repository
git clone https://github.com/[your-username]/hidden-realities-playbook.git

# Move into the folder
cd hidden-realities-playbook
```

**Replace `[your-username]` with your actual GitHub username.**

---

## Step 3: Replace Files with Our Structure

We already created the proper structure. Now you'll copy it into your cloned repo:

```bash
# Remove the default README (keep the structure, just replace README)
# We'll overwrite it with our version

# List what's there
ls -la
```

You should see:
- `.git/` (hidden folder — don't touch)
- `.gitignore`
- `README.md`
- Maybe `LICENSE` (from setup)

---

## Step 4: Copy Our Project Files

I'm going to package all the files we created. You'll:

1. Download the ZIP of our folder structure (I'll provide this)
2. Copy each file into your GitHub folder
3. Commit and push

**For now**, let me create a package:

```bash
# On your laptop, in the cloned repo folder, run:

# Copy the files from /home/claude/hidden-realities-playbook/
# To your local ~/Documents/hidden-realities-playbook/

# Option A: If you have access to /home/claude on this machine:
cp -r /home/claude/hidden-realities-playbook/* ~/Documents/hidden-realities-playbook/

# Option B: Manually create folders
mkdir -p stories chapters teaser-posts resources

# Then you'll add the individual files (README.md, etc.) manually or via download
```

---

## Step 5: Verify the Structure

After copying files, run:

```bash
# List all files
ls -la

# You should see:
# .git/
# .gitignore
# README.md (our version with the project overview)
# CONTRIBUTING.md
# GITHUB_SETUP.md
# LICENSE
# stories/
# chapters/
# teaser-posts/
# resources/
```

---

## Step 6: First Commit & Push

```bash
# Check status
git status

# You should see new/modified files (in red)

# Stage all changes
git add .

# Commit
git commit -m "Initial commit: Set up playbook structure and documentation"

# Push to GitHub
git push origin main

# Check it worked by going to github.com/[your-username]/hidden-realities-playbook
# You should see all the files now!
```

---

## Step 7: Set Up on Your Mac

Once it's on GitHub, getting it on your Mac is easy:

```bash
# On your Mac, open Terminal and run:
cd ~/Documents

# Clone the same repo
git clone https://github.com/[your-username]/hidden-realities-playbook.git

# Now you have it on both machines!
```

---

## Step 8: Sync Between Laptop & Mac

### When You're on Laptop and Add a Story
```bash
cd ~/Documents/hidden-realities-playbook

# Create/edit your story file in stories/
# (or use a text editor to add it)

# Then commit and push
git add stories/2026-09-05_story-title.md
git commit -m "Add story: Story Title"
git push origin main
```

### When You Switch to Mac
```bash
cd ~/Documents/hidden-realities-playbook

# Pull the latest changes (the story from your laptop)
git pull origin main

# Now you have it! Edit, add more stories, etc.
git add stories/2026-09-12_another-story.md
git commit -m "Add story: Another Story"
git push origin main
```

---

## Step 9: Simplify with a Git Client (Optional)

If command line feels clunky, use a **Git GUI**:

### Free Options
- **GitHub Desktop** (github.com/desktop) — Easiest, graphical
- **Sourcetree** (atlassian.com/sourcetree) — Powerful, free
- **Gitkraken** (gitkraken.com) — Beautiful, free tier

### Using GitHub Desktop (Recommended for Beginners)
1. Download **GitHub Desktop**
2. Log in with your GitHub account
3. Click **File** → **Clone repository**
4. Select your `hidden-realities-playbook`
5. Choose folder location
6. Now you can:
   - Click the folder icon to edit files
   - See changes without terminal
   - Commit/push via buttons

---

## Quick Commands Reference

### Common Tasks

**I added a story file, now what?**
```bash
git add stories/YYYY-MM-DD_story.md
git commit -m "Add story: [Title]"
git push origin main
```

**I want to see what changed**
```bash
git status
```

**I want to get the latest changes from GitHub (from your other machine)**
```bash
git pull origin main
```

**I want to see my commit history**
```bash
git log --oneline
```

**I want to see only the stories I've added**
```bash
ls -la stories/
```

---

## Cross-Device Workflow (Simplified)

### Scenario 1: You're on Laptop
1. Add story to `/stories/YYYY-MM-DD_slug.md`
2. Terminal:
   ```bash
   git add stories/YYYY-MM-DD_slug.md
   git commit -m "Add story: [Title]"
   git push origin main
   ```
3. Done. Now it's on GitHub.

### Scenario 2: You Switch to Mac
1. Open Terminal:
   ```bash
   cd ~/Documents/hidden-realities-playbook
   git pull origin main
   ```
2. Now you have the latest story. Edit, add more, repeat.

### Scenario 3: You Want to See What's on GitHub (Web)
1. Go to `github.com/[your-username]/hidden-realities-playbook`
2. Click on `/stories` folder
3. See all your stories + timestamps
4. Click any story to read it online

---

## Troubleshooting

### "Permission denied" when pushing
- You didn't authorize GitHub on this machine
- Use **GitHub Desktop** (handles auth automatically) or run:
  ```bash
  git config --global user.name "[Your Name]"
  git config --global user.email "[your-email@example.com]"
  ```

### "Merge conflict"
- You edited the same file on two machines
- Use GitHub Desktop (easier) or ask me for help

### "I pushed and it's not on GitHub"
- Check: `git push` output should say "✓ main → main" or similar
- Refresh github.com page (might need hard refresh: Cmd+Shift+R on Mac)

### "I can't find my repo on GitHub"
- Go to `github.com/[your-username]` → look in Repositories list
- Or: `github.com/[your-username]/hidden-realities-playbook`

---

## Best Practices

1. **Commit often** (don't wait until you have 10 stories)
   - 1 story = 1 commit
   - Message: `"Add story: [Story Title]"`

2. **Pull before you work** (get latest changes)
   ```bash
   git pull origin main
   ```

3. **Use clear filenames**
   - ✅ `2026-08-15_discovery-documentation-gaps.md`
   - ❌ `story1.md` or `final_final_version.md`

4. **Commit messages matter**
   - ✅ "Add story: Documentation gaps discovered"
   - ❌ "update" or "changes"

5. **Keep files in the right folders**
   - Stories → `/stories/`
   - Teaser posts → `/teaser-posts/`
   - Drafts → `/chapters/`
   - Resources → `/resources/`

---

## Next: Tell Me When You're Done

Once your repo is set up:

1. Create your first story (use `resources/story-template.md`)
2. Commit and push it to GitHub
3. Send me the link: `github.com/[your-username]/hidden-realities-playbook`
4. I'll verify it's working and we're ready to go

---

## Questions?

- Git feels confusing? → Use GitHub Desktop (much simpler)
- Not sure about the folder structure? → Check the repo on GitHub.com
- How do I add a story? → See `CONTRIBUTING.md`
- Something broke? → Send me a message with error output

You've got this. GitHub is powerful once it clicks.
