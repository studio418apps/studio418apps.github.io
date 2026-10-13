<p align="center">
  <img src="assets/teapot.svg" alt="Studio 418" width="120">
</p>

<h1 align="center">Studio 418</h1>

<p align="center">
  <em>HTTP 418 · I'm a teapot</em><br>
  Small, thoughtful, ad-free apps — brewed in Antalya.
</p>

<p align="center">
  <a href="https://studio418apps.github.io">Website</a> ·
  <a href="https://medium.com/@studio418apps">Medium</a> ·
  <a href="mailto:studio418apps@gmail.com">Contact</a>
</p>

---

This repository hosts the Studio 418 website, published with GitHub Pages at **[studio418apps.github.io](https://studio418apps.github.io)**. It includes the studio homepage and the product, privacy and support pages for our apps.

## Apps

| App | Status | Links |
|---|---|---|
| **Sit Happens** | On the App Store | [Page](https://studio418apps.github.io/sit-happens/) · [App Store](https://apps.apple.com/tr/app/sit-happens/id6794938801) |
| **JellyFish Routine** | On the App Store | [Page](https://studio418apps.github.io/jellyfish-routine/) · [App Store](https://apps.apple.com/tr/app/jellyfish-routine/id6776623835) |
| **BookFrog** | Coming soon | [Page](https://studio418apps.github.io/bookfrog/) · [Privacy](https://studio418apps.github.io/bookfrog/privacy.html) · [Support](https://studio418apps.github.io/bookfrog/support.html) |
| **Mandarin Yoga** | Client project | [Page](https://studio418apps.github.io/mandarin-yoga/) |

## Structure

```
index.html              Studio homepage
assets/                 Shared stylesheet, logo and favicon
<app>/index.html        App page
<app>/privacy.html      Privacy policy (TR + EN), where applicable
<app>/support.html      Support and FAQ (TR + EN), where applicable
.nojekyll               Serves the site as-is, including .well-known/
```

The site is plain HTML and CSS with no build step. To preview it locally:

```bash
python3 -m http.server
```

Then open http://localhost:8000.

## Contact

Questions, feedback or a project idea? Write to **[studio418apps@gmail.com](mailto:studio418apps@gmail.com)**.

---

<sub>© 2026 Studio 418 · Antalya, Türkiye. All rights reserved. The site content, logo and app names may not be reused without permission.</sub>
