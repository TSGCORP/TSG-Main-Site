# TSG website (tsg-corp.com)

Static site for TSG, hosted on GitHub Pages. No build step: edit the HTML, commit, and the site updates.

## Files
- `index.html`, `services.html`, `about.html`, `contact.html` — the four pages
- `css/style.css` — all styling (colors and fonts are variables at the top)
- `assets/` — logo files; add your photos here
- `CNAME` — tells GitHub Pages to serve the site at tsg-corp.com (keep this file)
- `.nojekyll` — tells GitHub to serve files as-is

## Before launch
1. **Photos.** Each gray dotted box is a `<div class="ph">` placeholder. Replace it with the `<img>` tag shown in the HTML comment next to it, and drop the photo in `assets/`.
2. **Testimonials.** Fill in the two bracketed quotes on `index.html`, or delete that section.
3. **Client ticker.** On `index.html`, replace the 20 bracketed `[Client 1]` to `[Client 20]` names with real client names or logos (see the comment in the HTML). Confirm each client is comfortable being named. Delete the section if you'd rather not show clients yet.
4. **Contact form.** Create a free form at formspree.io and replace `YOUR_FORM_ID` in `contact.html`.
5. **Scheduler link.** Paste your booking link into `contact.html` where the comment says SCHEDULER.
6. **LinkedIn links.** Replace the `https://www.linkedin.com/` links in the footer and About page with your profile and The Comp Desk newsletter URL.

## Publish on GitHub Pages
1. Create a new public repository on github.com (for example `tsg-site`).
2. Upload every file and folder in this package to the repository (drag and drop works on the GitHub website).
3. In the repository go to **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, choose branch `main` and folder `/ (root)`, and save.
4. In the same Pages settings, under **Custom domain**, enter `tsg-corp.com` and save. Turn on **Enforce HTTPS** once the certificate is ready (can take up to an hour).

## Point the domain at GitHub
At your domain registrar (wherever tsg-corp.com is registered), replace the Canva DNS records with these. Remove any existing A, AAAA, or CNAME records for the root and `www` that point to Canva.

| Type | Host | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | YOUR-GITHUB-USERNAME.github.io |

Leave your MX records (email) untouched. DNS changes can take a few hours to propagate. Verify the records against GitHub's current documentation (docs.github.com, "Managing a custom domain for your GitHub Pages site") before saving.

## Editing later
Change the text in the HTML files directly. Colors and fonts live in the `:root` block at the top of `css/style.css`.
