# denis-lavrinenko

The public canon site of **Denis Lavrinenko** — a small, versioned set of case studies and documents on operations, software, and human-governed AI practice.

**Status: published.** This repository is served as a GitHub Pages project site at `https://sandiegorussian.github.io/public-canon/`. There is no analytics, there are no cookies, and there are no trackers.

## What this is

A calm, documentary, static website — plain HTML and one stylesheet, no build step, no JavaScript, no cookies, no trackers, no third-party fonts or scripts. The site presents a homepage and its first published case study:

- **The Human-Review Band Is the Product** — a practice-based case study of a purpose-bounded review of a decade-old contact archive.

Additional case studies and documents are listed on the homepage as clearly marked *planned* placeholders; they are not yet written or published.

## Architecture

- Static HTML + CSS; a single inline-referenced SVG diagram; canonical Markdown source for the article.
- Privacy-preserving by construction: no analytics, cookies, pixels, embeds, external fonts, or network requests. The only assets a browser loads are the local stylesheet and the local SVG.
- Served as a plain static site on GitHub Pages, with a custom name-based domain possible later.

## Hosting model and paths

The current deployment is a GitHub Pages **project site** served under the
`/public-canon/` path (i.e., `https://sandiegorussian.github.io/public-canon/`),
with a possible transition to a **custom-domain root** later.

- The homepage and the case-study page use site-relative links that work at the
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

Contact is via LinkedIn. No public email is provided.
