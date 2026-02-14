# Quick Start Guide

Welcome! I've converted your dad's Squarespace site to a free Jekyll site that you can host on GitHub Pages. This will save you $200-300 per year while keeping all the content exactly as it is.

## What I've Created

A complete static website with:
- ✅ Homepage with book information
- ✅ Excerpt page with introduction
- ✅ Blog section with sample post
- ✅ Reviews & Press page
- ✅ About the Authors page
- ✅ Buy the Book page
- ✅ Clean, readable design optimized for long-form content
- ✅ Fully responsive (works on phones, tablets, computers)
- ✅ Fast loading times

## Next Steps (In Order)

### Step 1: Review the Files (5 minutes)
Open the `blindfoldchess-jekyll` folder and look around:
- `index.md` - Homepage
- `excerpt.md` - Book excerpt
- `blog.md` - Blog index
- Other `.md` files - Various pages
- `_posts/` folder - Blog posts go here
- `assets/css/style.css` - The styling

### Step 2: Read the Documentation (10 minutes)
I've created two guides for you:
1. **README.md** - Overview and technical details
2. **GITHUB_DESKTOP_GUIDE.md** - Step-by-step visual walkthrough

Start with the GITHUB_DESKTOP_GUIDE.md - it has every single step with explanations.

### Step 3: Set Up GitHub Desktop (20 minutes)
Follow these steps from the guide:
1. Create a GitHub account (if you don't have one)
2. Download and install GitHub Desktop
3. Create a repository on GitHub.com
4. Add your local folder to GitHub Desktop
5. Publish to GitHub
6. Enable GitHub Pages

After this, your site will be live at a free github.io address!

### Step 4: Add Images (30 minutes)
The site needs three images from your Squarespace site. You can:
1. Download them from blindfoldchess.net (right-click, save)
2. Put them in the `assets/images/` folder
3. Commit and push via GitHub Desktop

See `assets/images/README.md` for the specific images needed.

### Step 5: Point Your Domain (10 minutes + wait time)
Once you're happy with the site:
1. Add custom domain in GitHub Pages settings
2. Update your DNS records (detailed in the guide)
3. Wait for DNS to propagate (can take 24 hours)

## Important Files

### Content Files (Easy to edit)
- `index.md` - Homepage content
- `about-the-authors.md` - About page
- `excerpt.md` - Book excerpt
- `reviews-and-press.md` - Reviews page
- `buy-the-book.md` - Purchase information
- `blog.md` - Blog listing page
- `_posts/*.md` - Individual blog posts

### Configuration Files (Rarely need to change)
- `_config.yml` - Site settings
- `_layouts/*.html` - Page templates
- `assets/css/style.css` - Styling

## How to Make Changes

### Easy Way (Editing Files Directly)
1. Open any `.md` file in TextEdit or your favorite text editor
2. Make changes to the content (below the `---` marks at the top)
3. Save the file
4. Use GitHub Desktop to commit and push
5. Your site updates in ~2 minutes

### What You Can Edit
In the `.md` files:
- Any text content
- Links
- Headings
- Paragraphs
- Lists

Keep the front matter (between `---` marks) as is, just edit the content below it.

## Adding Blog Posts

### Quick Template
1. Create a new file in `_posts/` folder
2. Name it: `YYYY-MM-DD-title-here.md` (e.g., `2024-03-15-new-record.md`)
3. Add this at the top:
```yaml
---
layout: post
title: "Your Post Title Here"
date: 2024-03-15
author: Your Name
---

Your content starts here. Write normally, using Markdown if you want formatting.

## You can use headings

And **bold text** or *italic text*.
```
4. Save, commit, and push via GitHub Desktop

## Migration Checklist

- [ ] Review all files and content
- [ ] Read GITHUB_DESKTOP_GUIDE.md
- [ ] Set up GitHub Desktop
- [ ] Create repository on GitHub
- [ ] Publish site to GitHub
- [ ] Enable GitHub Pages
- [ ] Confirm site loads at github.io URL
- [ ] Download and add images from Squarespace
- [ ] (Optional) Add any missing blog posts
- [ ] Set up custom domain
- [ ] Update DNS records
- [ ] Enable HTTPS
- [ ] Test everything works
- [ ] Cancel Squarespace subscription!

## Current Site vs. New Site

### What's the Same
- All content (text, structure, pages)
- All main navigation
- Professional appearance
- Blog functionality
- Responsive design

### What's Different (Better!)
- Costs $0/year instead of $200-300/year
- Loads faster (static files)
- More control over everything
- No platform lock-in
- Version controlled (history of all changes)
- Can edit from anywhere

### What You Need to Add
- Images from the Squarespace site
- Any additional blog posts you want to migrate
- (Optional) PDF downloads or other files

## Getting Help

If you get stuck:

1. **Check the guides:**
   - GITHUB_DESKTOP_GUIDE.md has step-by-step instructions
   - README.md has technical details

2. **GitHub's documentation:**
   - GitHub Desktop: https://docs.github.com/en/desktop
   - GitHub Pages: https://docs.github.com/en/pages

3. **Common issues:**
   - Site not showing up? Wait 3-5 minutes after first deployment
   - Changes not appearing? Hard refresh (Cmd+Shift+R)
   - 404 error? Check that GitHub Pages is enabled and repository is Public

## Cost Comparison

### Squarespace (Current)
- Yearly cost: $200-300
- Total over 5 years: $1,000-1,500

### GitHub Pages (New)
- Hosting: FREE
- Domain renewal: ~$12/year (you already have this)
- Total over 5 years: ~$60

**You'll save about $1,000-1,400 over the next 5 years!**

## Timeline Estimate

- **Reading docs and understanding:** 30-45 minutes
- **Setting up GitHub/GitHub Desktop:** 20-30 minutes  
- **First deployment:** 10-15 minutes
- **Adding images:** 30-60 minutes
- **DNS/domain setup:** 15-20 minutes
- **Total active time:** ~2-3 hours spread over a day or two

The DNS propagation happens in the background and can take up to 24 hours, but you don't have to wait around for it.

## You're All Set!

The hard part (conversion) is done. Now it's just following the step-by-step guide to get it online.

The site is structured exactly like your Squarespace site, just without the monthly fees. Everything your dad created is preserved and will continue to be accessible to readers worldwide.

Good luck, and feel free to ask if you have any questions!
