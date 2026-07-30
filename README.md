# Landline Recording Website

Single-page static site for Landline Recording (Hoboken, NJ). No build step — just HTML/CSS/JS.

## Deploy with GitHub Pages

1. Drop `index.html` and the `images/` folder into the root of your repo (keep them side by side).
2. In the repo: **Settings → Pages → Source → Deploy from a branch → main / (root)**.
3. Site goes live at `https://<username>.github.io/<repo>/` (or your custom domain if configured under Pages → Custom domain).

## Editing text

All copy lives directly inside `index.html` — open it in any text editor (or right on GitHub via the pencil icon on the file) and edit the words between the HTML tags. Nothing is pulled from a CMS or separate data file. Key spots:

- Hero headline/subhead: near the top, inside `<section class="hero">`.
- Services cards: inside `<section id="services">`, one `<div class="service-card">` per service.
- About bio + quote: inside `<section id="about">`.
- Rates table: inside `<section id="rates">`.
- Gear lists: inside `<section id="gear">`, grouped in `<details>` blocks.
- Contact email/phone/socials: inside `<section id="contact">`.

Just don't touch anything inside `<style>` or `<script>` unless you're changing design/behavior — that's CSS/JS, not page copy.

## Photos

All 11 photos from the `Images` folder are in `images/` (converted from HEIC to JPEG) and wired into the page:

- About section: `gallery_shot_1.jpg` (portrait of Jon with the Jazzmaster)
- Gallery (10 photos): `IMG_8323.jpg`, `IMG_8324.jpg`, `IMG_8430.jpg`, `gallery_shot_2.jpg`, `gallery_shot_3.jpg`, `IMG_0096.jpg`, `IMG_0113.jpg`, `IMG_1541.jpg`, `IMG_0867.jpg`, `IMG_0870.jpg`

Want to add more later? Drop additional JPGs into `images/` and add another `<div class="gallery-item"><img src="images/yourfile.jpg" alt="..."></div>` inside `<section id="gallery">` in `index.html` — the grid auto-adjusts to however many items are there.

- **Colors/fonts**: adjust the CSS variables at the top of the `<style>` block (`--bg`, `--accent`, etc.) and the Google Fonts link if you want a different typeface.

## Custom domain

If you want `landlinerecording.com` to point here instead of Wix, add a `CNAME` file with the domain in it and update your DNS records per GitHub's custom domain docs.
