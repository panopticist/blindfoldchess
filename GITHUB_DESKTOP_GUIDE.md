# Complete GitHub Desktop Setup Guide

This is a detailed, step-by-step guide for publishing your Jekyll site using GitHub Desktop on Mac.

## Part 1: Prepare Your GitHub Account

### Step 1: Create GitHub Account (if needed)
If you don't already have a GitHub account:
1. Go to https://github.com
2. Click "Sign up"
3. Follow the registration process

### Step 2: Download and Install GitHub Desktop
1. Go to https://desktop.github.com
2. Click "Download for macOS"
3. Open the downloaded file
4. Drag GitHub Desktop to your Applications folder
5. Open GitHub Desktop from Applications
6. Sign in with your GitHub account

## Part 2: Create Your Repository on GitHub

### Step 1: Go to GitHub.com
1. Open your web browser
2. Go to https://github.com
3. Sign in if you haven't already

### Step 2: Create a New Repository
1. Click the "+" icon in the top-right corner
2. Select "New repository"

### Step 3: Configure Repository Settings
Fill in the following:
- **Repository name:** `blindfoldchess` (lowercase, no spaces)
  - Alternative: Use `yourusername.github.io` to make it your main personal site
- **Description:** "Website for Blindfold Chess: The Book"
- **Public/Private:** Select **Public** (required for free GitHub Pages)
- **Initialize repository:** Leave ALL checkboxes UNCHECKED
  - Do NOT add README
  - Do NOT add .gitignore
  - Do NOT choose a license
- Click the green "Create repository" button

### Step 4: Note Your Repository URL
After creating, you'll see a page with setup instructions. Note the URL at the top - it will be something like:
```
https://github.com/yourusername/blindfoldchess
```

## Part 3: Set Up Your Local Repository

### Step 1: Locate Your Site Folder
1. Find where you saved the `blindfoldchess-jekyll` folder
2. Remember this location (e.g., Downloads, Desktop, Documents)

### Step 2: Open GitHub Desktop
1. Open GitHub Desktop from Applications
2. Make sure you're signed in (your username should appear in the top right)

### Step 3: Add Your Local Repository
1. Click **"File"** in the menu bar
2. Select **"Add Local Repository..."**
3. Click the **"Choose..."** button
4. Navigate to and select the `blindfoldchess-jekyll` folder
5. Click **"Add Repository"**

### Step 4: Initialize Git Repository (if needed)
If you see an error saying "This directory does not appear to be a Git repository":
1. Click **"Create a repository"** in the error dialog
2. In the dialog that appears:
   - Name: `blindfoldchess-jekyll`
   - Description: "Static Jekyll site for Blindfold Chess book"
   - Keep "Git Ignore" as None
   - Keep "License" as None
3. Click **"Create Repository"**

## Part 4: Make Your First Commit

### Step 1: Review Changes
In GitHub Desktop, you should see:
- Left panel: List of all your files (they should all be checked)
- Right panel: Preview of file contents

### Step 2: Create Commit
1. At the bottom left, you'll see:
   - **Summary box** (required)
   - **Description box** (optional)
2. In the Summary box, type: `Initial site setup`
3. In the Description box (optional), type: `Converting from Squarespace to Jekyll`
4. Click the blue **"Commit to main"** button

## Part 5: Publish to GitHub

### Step 1: Publish Repository
After committing, you'll see a button that says **"Publish repository"** in the top right
1. Click **"Publish repository"**
2. In the dialog that appears:
   - Name: Should already be filled in as `blindfoldchess-jekyll` or `blindfoldchess`
   - Description: Should already be filled in
   - **IMPORTANT:** Make sure "Keep this code private" is **UNCHECKED**
   - Organization: Leave as "None"
3. Click the blue **"Publish repository"** button

### Step 2: Confirm Publishing
1. GitHub Desktop will upload all your files (this may take 30 seconds to a minute)
2. When done, the "Publish repository" button will change to "Push origin"
3. You should see "Last fetched just now" at the bottom

## Part 6: Enable GitHub Pages

### Step 1: Go to Your Repository on GitHub
1. In GitHub Desktop, click **"Repository"** in the menu bar
2. Select **"View on GitHub"** (or press Cmd+Shift+G)
3. This opens your repository in your web browser

### Step 2: Access Settings
1. On your repository page, click the **"Settings"** tab (top right area)
2. In the left sidebar, scroll down and click **"Pages"**

### Step 3: Configure GitHub Pages
1. Under "Source":
   - Click the dropdown that says "None"
   - Select **"Deploy from a branch"**
2. Under "Branch":
   - First dropdown: Select **"main"**
   - Second dropdown: Select **"/ (root)"**
   - Click **"Save"**

### Step 4: Wait for Deployment
1. A blue box will appear saying "GitHub Pages source saved"
2. Refresh the page after 30 seconds
3. You should see a green box with: "Your site is live at https://yourusername.github.io/blindfoldchess/"
4. Click the link to view your site!

**Note:** The first deployment can take 2-3 minutes. If you see a 404 error, wait another minute and refresh.

## Part 7: Set Up Custom Domain (blindfoldchess.net)

### Step 1: Add Custom Domain in GitHub
1. While still in **Settings → Pages**
2. Under "Custom domain", type: `www.blindfoldchess.net`
3. Click **"Save"**
4. GitHub will create a CNAME file in your repository

### Step 2: Configure DNS
You need to update DNS settings where your domain is registered (e.g., Squarespace, GoDaddy, Namecheap):

#### For Squarespace Domain:
1. Log into Squarespace
2. Go to Settings → Domains
3. Click on blindfoldchess.net
4. Click "DNS Settings"
5. Add these records:
   - **CNAME Record:**
     - Host: `www`
     - Points to: `yourusername.github.io`
   - **A Records** (add all four):
     - Host: `@`, Points to: `185.199.108.153`
     - Host: `@`, Points to: `185.199.109.153`
     - Host: `@`, Points to: `185.199.110.153`
     - Host: `@`, Points to: `185.199.111.153`

### Step 3: Enable HTTPS
1. After DNS propagates (5 minutes to 24 hours)
2. Return to Settings → Pages
3. Check the box for **"Enforce HTTPS"**

## Part 8: Making Future Updates

### Adding/Editing Content

#### Method 1: Edit on Your Computer
1. Open the file you want to edit in any text editor (TextEdit, VS Code, etc.)
2. Make your changes
3. Save the file
4. Open GitHub Desktop
5. You'll see your changes listed in the left panel
6. Write a summary (e.g., "Updated about page")
7. Click "Commit to main"
8. Click "Push origin" to upload to GitHub
9. Your site will update in 1-2 minutes

#### Method 2: Edit on GitHub.com
1. Go to your repository on GitHub
2. Click on the file you want to edit
3. Click the pencil icon (Edit this file)
4. Make your changes
5. Scroll down and click "Commit changes"
6. Your site will update in 1-2 minutes

### Adding Images
1. Download images to your computer
2. Place them in the `assets/images/` folder
3. In GitHub Desktop:
   - Files will appear in the changes list
   - Write summary: "Added images"
   - Click "Commit to main"
   - Click "Push origin"

### Adding Blog Posts
1. Create a new file in the `_posts` folder
2. Name it: `YYYY-MM-DD-title-of-post.md` (e.g., `2024-03-15-new-world-record.md`)
3. Add front matter and content (see README for template)
4. Commit and push via GitHub Desktop

## Troubleshooting

### Problem: Changes aren't showing on the live site
**Solution:** 
- Wait 2-3 minutes after pushing
- Hard refresh your browser (Cmd+Shift+R on Mac)
- Check GitHub Actions tab to see if build succeeded

### Problem: 404 error on the live site
**Solution:**
- Make sure GitHub Pages is enabled (Settings → Pages)
- Wait a few minutes for initial deployment
- Check that your repository is Public

### Problem: Custom domain not working
**Solution:**
- Verify DNS records are correct
- Wait for DNS propagation (can take up to 48 hours)
- Check status at whatsmydns.net

### Problem: Can't push to GitHub
**Solution:**
- Make sure you're signed into GitHub Desktop
- Try: Repository → Pull (to sync with GitHub)
- Then try pushing again

## Quick Reference Commands

### In GitHub Desktop:
- **See changes:** Changes tab (left side)
- **Commit changes:** Write summary → "Commit to main"
- **Upload to GitHub:** "Push origin" button
- **Download updates:** "Pull origin" button
- **View online:** Repository → View on GitHub

### Common Workflow:
1. Make changes to files
2. Open GitHub Desktop
3. Review changes
4. Write commit summary
5. Click "Commit to main"
6. Click "Push origin"
7. Wait 1-2 minutes
8. Visit your site to see changes

## Need Help?

- **GitHub Desktop Docs:** https://docs.github.com/en/desktop
- **GitHub Pages Docs:** https://docs.github.com/en/pages
- **Jekyll Docs:** https://jekyllrb.com/docs/

## Success Checklist

- [ ] GitHub Desktop installed and signed in
- [ ] Repository created on GitHub.com
- [ ] Local folder added to GitHub Desktop
- [ ] Files committed
- [ ] Repository published (not private)
- [ ] GitHub Pages enabled
- [ ] Site loads at github.io URL
- [ ] Custom domain configured (optional)
- [ ] DNS updated (optional)
- [ ] Images added (optional but recommended)

Congratulations! Your site is now live and you're saving $200-300 per year!
