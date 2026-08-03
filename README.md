# Blindfold Chess: The Book — blindfoldchess.net

The website for *Blindfold Chess: History, Psychology, Techniques, Champions,
World Records, and Important Games* by Eliot Hearst and John Knott (McFarland, 2009).

This is a static [Jekyll](https://jekyllrb.com) site hosted for free on GitHub
Pages, migrated from Squarespace in 2026. All 5 pages and 31 blog posts were
preserved exactly, with their original URLs, so old links and search results
keep working.

## How this repository is organized

| Location | What it is |
|---|---|
| `index.md` | The home page |
| `excerpt.md`, `reviews-and-press.md`, `about-the-authors.md`, `buy-the-book.md` | The other pages |
| `blog.md` | The blog index (builds its list automatically) |
| `_posts/` | The 31 blog posts, one file each, named `YYYY-MM-DD-title.md` |
| `_layouts/`, `assets/css/style.css` | The site's design |
| `assets/images/`, `assets/files/` | Images and PDFs (filled in automatically — see below) |
| `image-manifest.txt` + `.github/workflows/download-images.yml` | The image-rescue system |
| `CNAME` | Tells GitHub Pages your custom domain |

## Publishing entirely in the browser (no desktop app)

You can skip GitHub Desktop and do everything on github.com:

**Step 1 — Create the repository.**
On github.com, click the **+** (top-right) → **New repository**.
- Name: `blindfoldchess`
- Visibility: **Public** (required for free GitHub Pages)
- Check **"Add a README file"** (this initializes the repository so the
  upload screen works; your real README will replace it in the next step)
- **Create repository**

**Step 2 — Upload the site files.**
On the repository page: **Add file → Upload files**. Open your unzipped
site folder, select everything inside it (Ctrl/Cmd+A), and drag it all onto
the upload area. Wait for every file to finish listing (58 files, ~40 in
assets may show as none yet — that's fine, assets start empty), type
`Initial site import` in the commit box, and click **Commit changes**.
> Note: your computer hides the `.github` folder, so it won't come along in
> the drag — that's expected. Step 3 recreates its one file.

**Step 3 — Create the image-download automation by hand.**
1. On the repository page: **Add file → Create new file**
2. In the name box type exactly: `.github/workflows/download-images.yml`
   (typing the `/` characters creates the folders)
3. Paste in the full contents of the `download-images.yml` file (it's in
   your zip under `.github/workflows/`, and Claude also provided it as a
   separate file for easy copying — open it in any text editor)
4. **Commit changes.** This immediately triggers the download — check the
   **Actions** tab for the green check.

**Step 4 — Turn on GitHub Pages.**
Same as Step 5 of the desktop instructions: **Settings → Pages →
Deploy from a branch → main / (root) → Save**.

**Editing later in the browser:** navigate to any file, click the pencil
icon, edit, Commit changes. The live site updates in 1–2 minutes.

## Publishing for the first time (GitHub Desktop)

You need: a GitHub account and [GitHub Desktop](https://desktop.github.com) installed and signed in
(GitHub Desktop menu → Settings/Options → Accounts → sign in to GitHub.com).

**Step 1 — Create the repository.**
In GitHub Desktop: **File → New Repository…**
- Name: `blindfoldchess` (any name works)
- Local Path: somewhere easy to find, e.g. your Documents folder
- Leave everything else unchecked/default → **Create Repository**

**Step 2 — Add the site files.**
In GitHub Desktop click **Repository → Show in Finder** (Mac) or
**Show in Explorer** (Windows). Copy the *entire contents* of the site folder
you downloaded (everything inside `blindfoldchess/` — including the hidden
`.github` folder) into this repository folder.
> Tip: if you copy the files from the unzipped folder with Cmd/Ctrl+A, the
> hidden `.github` folder comes along automatically on most systems. To verify
> it arrived, check GitHub Desktop's "Changes" list for
> `.github/workflows/download-images.yml`.

**Step 3 — Commit.**
Back in GitHub Desktop you'll see all the files listed under **Changes**.
In the "Summary" box at bottom-left type `Initial site import` and click
**Commit to main**.

**Step 4 — Publish.**
Click **Publish repository** (top bar). **Uncheck "Keep this code private"**
(GitHub Pages on a free account requires a public repository) → **Publish Repository**.

**Step 5 — Turn on GitHub Pages.**
1. In GitHub Desktop: **Repository → View on GitHub** (opens github.com)
2. Click **Settings** (right end of the repository's tab bar) → **Pages** (left sidebar)
3. Under **Build and deployment** → Source: **Deploy from a branch**;
   Branch: **main**, folder **/ (root)** → **Save**

Within a few minutes your site is live at
`https://YOUR-USERNAME.github.io/blindfoldchess/`… except it will immediately
redirect to your custom domain (because of the `CNAME` file), which won't work
until you do the DNS step below. To preview before DNS is ready, you can
temporarily delete the `CNAME` file (commit + push), then restore it later —
or just proceed straight to the domain setup.

**Step 6 — Confirm the images downloaded themselves.**
Publishing triggers the image-rescue automation. On the repository page on
github.com, click the **Actions** tab. You should see
"Download images from Squarespace" running or completed (green check).
When done, all 39 images and 3 PDFs exist as real files in `assets/` in this
repository — the site no longer depends on Squarespace in any way.
If any download shows a warning, tell Claude or re-run it: **Actions →
Download images from Squarespace → Run workflow**. (Re-running is always safe;
it skips files it already has.)

## Pointing www.blindfoldchess.net at the new site

Your domain is registered *through Squarespace*, so do this **before**
cancelling the website subscription:

**A. Keep the domain registration.** In Squarespace: **Settings → Domains →
blindfoldchess.net**. Squarespace domains survive website-subscription
cancellation as a separate ~$20/year product (they'll bill the domain
separately). Alternatively, transfer the domain to another registrar like
Cloudflare (~$10/year) — either works; keeping it at Squarespace is simplest.

**B. Update DNS records.** In the domain's DNS settings, delete the existing
Squarespace website records and add:
- A `CNAME` record: host `www` → `YOUR-USERNAME.github.io.`
- Four `A` records for the bare domain, host `@`, pointing to GitHub Pages:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`

**C. Tell GitHub about the domain.** On github.com: repository **Settings →
Pages → Custom domain**: enter `www.blindfoldchess.net` → **Save**. Wait for
the DNS check to pass, then tick **Enforce HTTPS** (the option appears once
GitHub has issued the free certificate — can take up to an hour).

**D. Verify, then cancel Squarespace.** Once `https://www.blindfoldchess.net`
loads the new site, spot-check a few blog posts and the Excerpt page, confirm
the Actions image download succeeded (Step 6), and only then cancel the
Squarespace *website* subscription (keeping the domain per step A).

## Activate the contact form (one-time, ~5 minutes)

The form on About the Authors needs a free form-handling account:
1. Sign up at [formspree.io](https://formspree.io) (free tier: 50 messages/month)
2. Create a new form; choose the email address that should receive messages
3. Copy the form's ID (an 8-character code in the endpoint URL,
   `https://formspree.io/f/XXXXXXXX`)
4. In `about-the-authors.md`, replace `YOUR_FORM_ID` with that code
   (edit the file in any text editor, or directly on github.com with the
   pencil icon), commit, and push

Until then the form displays but submissions go nowhere.

## Making edits later

Every page and post is a plain text file. Edit it (any text editor, or the
pencil icon on github.com), then in GitHub Desktop: write a summary → 
**Commit to main** → **Push origin**. The live site updates in 1–2 minutes.

To add a new blog post, copy an existing file in `_posts/`, rename it with the
new date and title, and edit the front matter (the block between `---` lines)
and body.

## Previewing on your own computer (optional — most people never need this)

GitHub Pages builds the site for you, so local preview is only for
convenience. If you ever want it:
1. Install Ruby (macOS has it; Windows: [rubyinstaller.org](https://rubyinstaller.org), choose "Ruby+Devkit")
2. In a terminal, in the repository folder:
   `gem install bundler` then `bundle install` (first time only)
3. `bundle exec jekyll serve` and open http://localhost:4000
4. Ctrl+C stops it. Changes to files appear on reload.
