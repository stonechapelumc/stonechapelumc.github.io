# Stone Chapel UMC — Website

A static (no-database) redesign of the Stone Chapel United Methodist Church
website. It's just HTML and one CSS file, so it can be hosted for free and
will load fast on any device.

## What's here

```
index.html            Welcome / home page
history/index.html    Our History
staff/index.html      Leadership
photos/index.html     Historic Photos (a stub, ready to fill in)
contact-us/index.html Visit Us
styles.css            All styling for every page (edit colors/fonts here once)
assets/               Drop images here (see assets/README.txt)
404.html              Friendly "page not found" page
CNAME                 Tells GitHub Pages to serve the site at stone-chapel.org
sitemap.xml           Helps search engines
.nojekyll             Tells GitHub to serve the files as-is
```

## Hosting: do you need Bluehost + WordPress?

No. Because nothing on the site is dynamic, WordPress (and the Bluehost plan
behind it) is more than this needs — it's a database, a login, plugins, and
security updates for a site that is really just a handful of pages. A static
host is simpler, faster, and free.

**Recommended: GitHub Pages** (free, reliable, supports your custom domain).

### Deploy on GitHub Pages

1. Create a free account at github.com (if you don't have one).
2. Make a new repository — a public repo named `stone-chapel` is fine.
3. Upload everything in this folder to the repo (drag-and-drop in the browser
   works; keep the folder structure — `history/`, `staff/`, etc.).
4. In the repo: **Settings → Pages → Build and deployment → Source: Deploy
   from a branch**, pick `main` and `/ (root)`, then Save.
5. The site goes live in a minute or two at
   `https://<your-username>.github.io/stone-chapel/`.

### Point stone-chapel.org at it

The included `CNAME` file already names `stone-chapel.org`. To finish:

1. In **Settings → Pages → Custom domain**, confirm `stone-chapel.org`.
2. At your domain registrar (wherever the domain is managed — possibly through
   Bluehost), set DNS records:
   - Four `A` records for the apex `stone-chapel.org` pointing to GitHub's IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record for `www` pointing to `<your-username>.github.io`
3. Back in Settings → Pages, tick **Enforce HTTPS** once it's available.

DNS can take a little while to propagate. Keep Bluehost running until the new
site resolves correctly, then you can cancel the WordPress hosting.

(If you'd rather not use GitHub at all, the same files work on Netlify or
Cloudflare Pages — both free — or even uploaded to your existing Bluehost as
plain files. Nothing about the site is GitHub-specific except the CNAME/.nojekyll
convenience files.)

## Updating the site

You don't need to be a programmer for the common edits:

- **Weekly announcements** live in ONE place: the "News & Events" block near the
  bottom of `index.html`. Change the date in the `asof` line and edit the list
  items. (Look for the big comment that says "THIS IS THE ONE PLACE TO UPDATE.")
- **Service time / address / phone** appear in the colored band on the home page
  and in the footer of every page.
- **Add a photo:** put the image file in `assets/` (or `assets/photos/`), then
  follow the commented example in the relevant page to swap a placeholder for an
  `<img>` tag.
- **Colors and fonts** are all defined at the top of `styles.css` under
  `:root` — change them once and every page updates.

## A note on images

The placeholders on the History, Leadership, and Historic Photos pages are
ready for *your own* photographs of the actual church, congregation, and
grounds. For a 240-year-old historic site, real photos of the real place are
far more meaningful (and more honest) than generic stock imagery — and they
sidestep any licensing questions entirely. All the decorative artwork on the
site (the chapel illustration, the cross mark, the icons) is original and
license-free.

If you ever do want stock photography for a blank spot, use a source with a
clear free license — for example Unsplash, Pexels, or Wikimedia Commons images
marked public domain / CC0 — and keep a note of the source.
```
