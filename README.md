# Reazwan Ahmed — Portfolio (GitHub Pages)

Static version of myportfolioreazwan.com, ready to host for free on GitHub Pages.

---

## Setup: GitHub Pages (free hosting)

### 1. Create a GitHub account
Go to [github.com](https://github.com) → Sign up.

### 2. Create a new repository
- Click the **+** icon → **New repository**
- Name it: `reazwanahmed.github.io` (use your actual GitHub username)
- Set it to **Public**
- Click **Create repository**

### 3. Upload the files
- On your new repo page, click **uploading an existing file** (or drag files in)
- Upload everything in this folder — including the subfolders:
  - `index.html`
  - `style.css`
  - `steering-knuckle-design/` (the whole folder)
  - `tennis-ball-launcher/` (the whole folder)
  - `submarine-cfd-analysis/` (the whole folder)
- Click **Commit changes**

> **Note:** GitHub's web uploader doesn't handle folders well. Drag the entire unzipped folder onto the upload page, or use the GitHub Desktop app to push the files.

### 4. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages** (left sidebar)
- Under **Source** → select **Deploy from a branch**
- Branch: **main** / Folder: **/ (root)**
- Click **Save**

Your site will be live at `https://reazwanahmed.github.io` within a minute or two.

---

## Set up the contact form (Formspree — free)

The contact form uses [Formspree](https://formspree.io), which handles submissions without any server.

1. Go to [formspree.io](https://formspree.io) → Sign up free
2. Create a new form → it gives you a form ID like `xabcdefg`
3. In `index.html`, find this line:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID"
   ```
   Replace `YOUR_FORM_ID` with your actual ID.
4. Done — form submissions go straight to your email.

---

## Custom domain (optional)

If you want `myportfolioreazwan.com` to point here instead of WordPress:

1. Create a file called `CNAME` (no extension) in the root of your repo, containing just:
   ```
   myportfolioreazwan.com
   ```
2. At your domain registrar, update the DNS:
   - Add 4 A records pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - Or add a CNAME record: `www` → `reazwanahmed.github.io`
3. In GitHub Pages settings, enter your custom domain.

DNS changes take up to 24 hours to propagate.

---

## Notes

- Images are still loaded from `myportfolioreazwan.com` — they'll work as long as that WordPress site stays up. If you cancel WordPress, you'd need to re-host the images somewhere (e.g. upload them to the GitHub repo itself).
- Slideshows use [Swiper.js](https://swiperjs.com) loaded from a CDN — requires an internet connection to view.
