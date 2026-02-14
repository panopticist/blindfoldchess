# Blindfold Chess Website

Static Jekyll site for Blindfold Chess: The Book by Eliot Hearst and John Knott.

## About This Site

This is a Jekyll-based static site converted from the original Squarespace site at blindfoldchess.net. It contains all the main content about the book, including reviews, blog posts, author information, and book excerpts.

## Setup Instructions

### Prerequisites

- GitHub account (you already have this!)
- GitHub Desktop installed on your Mac
- Ruby and Jekyll installed (optional, only needed for local testing)

### Quick Start: Publishing to GitHub Pages

1. **Create a new repository on GitHub:**
   - Go to github.com and sign in
   - Click the "+" icon in the top right, select "New repository"
   - Name it: `blindfoldchess` (or `yourusername.github.io` for a personal site)
   - Make it **Public**
   - Do NOT initialize with README (we already have files)
   - Click "Create repository"

2. **Upload your site files using GitHub Desktop:**
   - Open GitHub Desktop
   - Click "File" → "Add Local Repository"
   - Click "Choose..." and navigate to the `blindfoldchess-jekyll` folder
   - If it says the folder isn't a Git repository, click "Create a repository"
   - Fill in the repository name (should match what you created on GitHub)
   - Click "Create Repository"
   
3. **Publish to GitHub:**
   - In GitHub Desktop, you should see all your files listed
   - Write a commit message like "Initial site setup"
   - Click "Commit to main"
   - Click "Publish repository" (top right)
   - Make sure "Keep this code private" is UNCHECKED
   - Click "Publish repository"

4. **Enable GitHub Pages:**
   - Go to your repository on github.com
   - Click "Settings" (top right)
   - Click "Pages" in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Under "Branch", select "main" and "/root"
   - Click "Save"
   - Wait 2-3 minutes, then your site will be live at: `https://yourusername.github.io/blindfoldchess/`

### Setting Up Your Custom Domain (blindfoldchess.net)

1. **Add custom domain in GitHub:**
   - In your repository Settings → Pages
   - Under "Custom domain", enter: `www.blindfoldchess.net`
   - Click "Save"
   - Check the "Enforce HTTPS" box (after DNS is configured)

2. **Update your DNS settings:**
   You'll need to update your DNS records where your domain is registered. Add these records:

   **For www.blindfoldchess.net (recommended):**
   - Type: `CNAME`
   - Name: `www`
   - Value: `yourusername.github.io`
   - TTL: `3600` (or default)

   **For the root domain (blindfoldchess.net):**
   You have two options:

   **Option A - Using ALIAS or ANAME records (if your DNS provider supports it):**
   - Type: `ALIAS` or `ANAME`
   - Name: `@`
   - Value: `yourusername.github.io`

   **Option B - Using A records (works with all DNS providers):**
   Add four A records:
   - Type: `A`, Name: `@`, Value: `185.199.108.153`
   - Type: `A`, Name: `@`, Value: `185.199.109.153`
   - Type: `A`, Name: `@`, Value: `185.199.110.153`
   - Type: `A`, Name: `@`, Value: `185.199.111.153`

3. **Wait for DNS propagation:**
   - DNS changes can take 5 minutes to 48 hours to propagate
   - You can check status at: https://www.whatsmydns.net/

### Adding Images

The site currently references images that need to be added. You'll need to download images from the original Squarespace site and add them to the `assets/images/` folder:

Required images:
- `alekhine.jpg` - Alexander Alekhine playing blindfold (homepage)
- `philidor_exhibition.jpg` - Philidor playing blindfolded (excerpt page)
- `alekhine-blindfold.jpg` - Alekhine playing blindfold (excerpt page)

To add images:
1. Download images from the Squarespace site or save them from web archives
2. Place them in the `assets/images/` folder in your local copy
3. Commit and push the changes using GitHub Desktop

## Local Development (Optional)

If you want to preview changes on your computer before publishing:

### Installing Jekyll on Mac

1. **Install Homebrew** (if not already installed):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install Ruby:**
   ```bash
   brew install ruby
   ```

3. **Add Ruby to your PATH:**
   Add this to your `~/.zshrc` file:
   ```bash
   export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
   ```
   Then restart your terminal or run:
   ```bash
   source ~/.zshrc
   ```

4. **Install Jekyll and Bundler:**
   ```bash
   gem install jekyll bundler
   ```

### Running the Site Locally

1. **Navigate to your site folder:**
   ```bash
   cd path/to/blindfoldchess-jekyll
   ```

2. **Install dependencies:**
   ```bash
   bundle install
   ```

3. **Serve the site:**
   ```bash
   bundle exec jekyll serve
   ```

4. **View in browser:**
   Open `http://localhost:4000` in your web browser

5. **Stop the server:**
   Press `Ctrl+C` in the terminal

### Making Changes

After making any changes to your site:

1. **Using GitHub Desktop:**
   - Open GitHub Desktop
   - You'll see your changes listed
   - Write a description of what you changed
   - Click "Commit to main"
   - Click "Push origin" (top right)
   - Changes will appear on your live site in 1-2 minutes

## Updating Content

### Adding a new blog post:

1. Create a new file in `_posts/` folder
2. Name it: `YYYY-MM-DD-title-of-post.md`
3. Add front matter at the top:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD
   author: Author Name
   ---
   ```
4. Write your content below the front matter
5. Commit and push changes

### Editing pages:

1. Edit the `.md` files in the root folder (e.g., `about-the-authors.md`)
2. Keep the front matter at the top (the part between `---` marks)
3. Edit the content below
4. Commit and push changes

## Cost

- **GitHub Pages hosting: FREE**
- **Domain name: ~$10-15/year** (you already have this)
- **Total yearly cost: ~$10-15** (vs. $200-300 with Squarespace!)

## Support

If you need help:
- GitHub Pages documentation: https://docs.github.com/en/pages
- Jekyll documentation: https://jekyllrb.com/docs/
- GitHub Desktop documentation: https://docs.github.com/en/desktop

## Site Structure

```
blindfoldchess-jekyll/
├── _config.yml           # Site configuration
├── _layouts/             # Page templates
│   ├── default.html      # Main template
│   └── post.html         # Blog post template
├── _posts/               # Blog posts
│   └── 2011-12-16-marc-lang-new-world-record-46-games.md
├── assets/
│   ├── css/
│   │   └── style.css     # Stylesheet
│   └── images/           # Images (need to be added)
├── index.md              # Homepage
├── excerpt.md            # Book excerpt
├── blog.md               # Blog index
├── about-the-authors.md  # About page
├── buy-the-book.md       # Purchase info
├── reviews-and-press.md  # Reviews page
├── Gemfile               # Ruby dependencies
└── README.md             # This file
```
