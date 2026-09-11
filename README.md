# denis-lavrinenko

The public canon site of **Denis Lavrinenko** — a small, versioned set of case studies and documents on operations, software, and human-governed AI practice.

**Status: published.** This repository is served as a GitHub Pages project site at `https://sandiegorussian.github.io/public-canon/`. There is no first-party analytics, there are no first-party cookies, and there are no trackers; the four Credly credential badges on the Credentials page are the only third-party embeds, and no other page loads them.

## What this is

A calm, documentary, static website — plain HTML and one stylesheet, no build step, no first-party JavaScript, cookies, or trackers, no third-party fonts. The single exception is the four live Credly credential badges on the Credentials page (`credentials/`), which load Credly’s official embed script once and one badge iframe per credential; those embeds may make external requests to Credly and set their own cookies. The homepage and the case-study page load no third-party resources. The site presents a homepage, its first published case study, and a credentials page:

- **The Human-Review Band Is the Product** — a practice-based case study of a purpose-bounded review of a decade-old contact archive.
- **Credentials** — two Google learning records on Coursera: the Google AI Professional Certificate (seven courses, in progress; three completed) and the completed five-course Google AI Essentials specialization, each linking to its issuer’s verification pages.

Additional case studies and documents are listed on the homepage as clearly marked *planned* placeholders; they are not yet written or published.

## Architecture

- Static HTML + CSS; a single inline-referenced SVG diagram; canonical Markdown source for the article.
- Privacy-preserving by construction: no analytics, cookies, pixels, or external fonts of this site’s own. Besides the local stylesheet and images, the only external resources a browser loads are Credly’s embed script and the four badge iframes on the Credentials page; the homepage and the case-study page load only local assets.
- Served as a plain static site on GitHub Pages, with a custom name-based domain possible later.

## Hosting model and paths

The current deployment is a GitHub Pages **project site** served under the
`/public-canon/` path (i.e., `https://sandiegorussian.github.io/public-canon/`),
with a possible transition to a **custom-domain root** later.

- The homepage, the Credentials page, and the case-study page use site-relative links that work at the
  local root, under `/public-canon/`, and at a custom-domain root.
- `404.html` is fully self-contained (its styles are inlined, so it needs no
  external asset at any base path). Its single home link targets `/public-canon/`
  for the project-site phase; at custom-domain cutover that one value becomes `/`.
- **Crawler control:** pages carry `<meta name="robots" content="index, follow">`.
  Note that a project site cannot control the account host-root robots file:
  standards-compliant crawlers read `https://sandiegorussian.github.io/robots.txt`,
  which belongs to the account root, **not** this repository. The `robots.txt` in
  this repo governs a root or custom-domain deployment of this repository.

## Local preview

No dependencies required. Either open `index.html` in a browser, or serve locally if your browser blocks local asset loading:

```sh
python3 -m http.server 8137 --bind 127.0.0.1
# then open http://127.0.0.1:8137/index.html
```

## Publication status

Published 2026-08-03 as a GitHub Pages project site. No downloadable PDF is provided at this release; if one is added later it will be generated only from the final, appendix-free HTML at that time — see `print/README.md`.

## License / copyright

See `COPYRIGHT.md`. The site code and the article/diagram are all rights reserved unless a license is added later. No open-source or Creative Commons license currently applies.

## Contact

Contact is via [LinkedIn](https://www.linkedin.com/in/sandiegorussian/). No public email is provided.
