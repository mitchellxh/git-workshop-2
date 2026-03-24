# Git & GitHub Workshop – Part 2: GitHub Pages

A hands-on workshop for publishing your first website using Git and GitHub Pages.

## Workshop Files

- `2026-Git-2.2.pptx` - Lecture slides
- `index.html` - Website template
- `style.css` - Styling
- `script.js` - Interactive features

---

## Activity 1: Clone the Template

```bash
# Navigate to your Desktop (or wherever you want to save your project)
cd ~/Desktop

# Clone the template repository
git clone https://github.com/mitchellxh/git-workshop-2.git

# Go into the project folder
cd git-workshop-2
```

Verify the files are there:

```bash
ls -l
```

---

## Activity 2: Personalize Your Page

1. Open `index.html` in your text editor
2. Find `YOUR_USERNAME` and replace it with your GitHub username
3. Change the heading "Welcome to My GitHub Page!" to something personal
4. Save the file

### Stage and commit your changes

```bash
# Check what changed
git status

# Stage all changes
git add .

# Commit with a descriptive message
git commit -m "Personalize my GitHub page"
```

---

## Activity 3: Push to Your Own Repository

### Create a new repository on GitHub

1. Go to GitHub.com
2. Click the **+** icon (top right) → **New repository**
3. Name it something like `my-first-website`
4. Keep it **Public**
5. **Don't** initialize with README (we already have files)
6. Click **Create repository**

### Connect and push

```bash
# Remove the template remote
git remote remove origin

# Add your repository as the new remote
git remote add origin git@github.com:YOUR_USERNAME/my-first-website.git

# Push to GitHub
git push -u origin main
```

If you get an error about `main` not existing:

```bash
git branch -M main
git push -u origin main
```

---

## Activity 4: Enable GitHub Pages

1. Go to your repository on GitHub.com
2. Click **Settings**
3. Click **Pages** in the left sidebar
4. Under **Source**, select **Deploy from a branch**
5. Under **Branch**, select **main**, leave folder as **/ (root)**
6. Click **Save**
7. Click the **Actions** tab to watch the build

After 2-5 minutes, your site will be live at:

```
https://YOUR_USERNAME.github.io/my-first-website/
```

---

## Activity 5: Make Another Change

Practice the full Git workflow:

```bash
# 1. Edit a file (try changing colors in style.css)

# 2. Check what changed
git status

# 3. Stage changes
git add .

# 4. Commit
git commit -m "Update site styles"

# 5. Push to GitHub
git push
```

Your GitHub Pages site will automatically update!

**Remember: Save → Add → Commit → Push**

---

## Quick Reference

| Command | What it does |
|---------|-------------|
| `git clone [url]` | Copy a repository to your computer |
| `git status` | See what files have changed |
| `git add .` | Stage all changes for commit |
| `git commit -m "message"` | Save changes with a description |
| `git push` | Upload changes to GitHub |
| `git pull` | Download changes from GitHub |

## Troubleshooting

| Problem | Solution |
|---------|----------|
| "Permission denied" | Make sure you're using SSH URL and your key is added to GitHub |
| "Failed to push" | Run `git pull` first, then `git push` |
| Can't see Pages site | Wait 5-10 minutes, verify URL, check Pages is enabled in Settings |
| "Please tell me who you are" | Run `git config --global user.name` and `user.email` (see Part 1 workshop) |
