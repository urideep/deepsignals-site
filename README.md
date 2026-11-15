# Deep Signals website

Static single-page site for deepsignals.tech. No build step, no dependencies.

## Structure

```
index.html          the whole site: markup, CSS and JS in one file
assets/
  logo.png          colour wordmark (transparent)
  logo-white.png    white wordmark for dark backgrounds
  favicon.svg
  uri.jpg, nadav.jpg, harel.jpg      team photos, 600x600
  img/              hero slideshow and section images, 1920x1080 JPG
README.md
```

## Editing

- Copy lives in `index.html`; the canonical wording is kept in the Claude Project doc `claude/canonical-messaging.md`. Change there first, then here.
- Hero slideshow: the `.slide` divs near the top of `<body>` and the `caps` array in the script at the bottom. Add an image to `assets/img/`, add a div and a caption.
- Status labels ("Pilot phase") appear in the hero note, the router cards, the market panels, the section pills and the traction strip. Search for the phrase to change all of them.
- Pilot form: replace `REPLACE_ME` in the form `action` with a Formspree (or similar) endpoint. Until then the Send button tells visitors to email instead.
- LinkedIn link in the footer: replace `REPLACE_ME` with the company page URL.
- Fonts: Manrope from Google Fonts. To self-host, download the woff2 files, put them in `assets/fonts/`, and replace the `<link>` tags with `@font-face` rules.

## Deploy

Any static host works. GitHub Pages: push to `main`, then Settings → Pages → Deploy from branch `main`, folder `/ (root)`. Add a `CNAME` file containing `deepsignals.tech` (or `www.deepsignals.tech`) once DNS is pointed at GitHub Pages.

Images are already sized and compressed (hero images 170–640 KB each). Total site weight about 6 MB, dominated by the eight hero images; if that matters, convert `assets/img/*.jpg` to WebP at quality 75.
