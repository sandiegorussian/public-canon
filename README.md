# denis-lavrinenko

The public canon site of **Denis Lavrinenko** — a small, versioned set of case studies and documents on operations, software, and human-governed AI practice.

**Status: draft · not yet published.** This repository holds an implementation-ready static site that has not been released. Every page is marked *Draft · Not published* and carries `noindex, nofollow`; there is no publication date, no live URL, and no analytics.

## What this is

A calm, documentary, static website — plain HTML and one stylesheet, no build step, no JavaScript, no cookies, no trackers, no third-party fonts or scripts. The site presents a homepage and a first publication candidate:

- **The Human-Review Band Is the Product** — a practice-based case study of a purpose-bounded review of a decade-old contact archive.

Additional case studies and documents are listed on the homepage as clearly marked *planned* placeholders; they are not yet written or published.

## Architecture

- Static HTML + CSS; a single inline-referenced SVG diagram; canonical Markdown source for the article.
- Privacy-preserving by construction: no analytics, cookies, pixels, embeds, external fonts, or network requests. The only assets a browser loads are the local stylesheet and the local SVG.
- Designed to be served as a plain static site (e.g., GitHub Pages) with a custom name-based domain later.

## Hosting model and paths

The intended near-term deployment is a GitHub Pages **project site** served under the
`/public-canon/` path (i.e., `https://<owner>.github.io/public-canon/`), transitioning
to a **custom-domain root** later.

- The homepage and the case-study page use site-relative links that work at the
  local root, under `/public-canon/`, and at a custom-domain root.
- `404.html` is fully self-contained (its styles are inlined, so it needs no
  external asset at any base path). Its single home link targets `/public-canon/`
  for the project-site phase; at custom-domain cutover that one value becomes `/`.
- **Crawler control:** page-level `<meta name="robots" content="noindex, nofollow">`
  is present on every page and is the primary control during the project-site
  phase. A project site cannot control the host-root robots file: standards-
  compliant crawlers read `https://<owner>.github.io/robots.txt`, which belongs to
  the account root, **not** this repository. The `robots.txt` in this repo is
  effective only for a root/custom-domain deployment. A true host-root
  `robots.txt` is therefore an external configuration matter for the
  custom-domain root, not a defect of this repository.

## Local preview

No dependencies required. Either open `index.html` in a browser, or serve locally if your browser blocks local asset loading:

```sh
python3 -m http.server 8137 --bind 127.0.0.1
# then open http://127.0.0.1:8137/index.html
```

## Publication status

Publication remains pending. The site stays unpublished until a separate release step sets the publication date and canonical URL and removes the draft markers. A downloadable PDF of the case study is planned at launch and is generated only from the final, appendix-free HTML at that time — see `print/README.md`.

## License / copyright

See `COPYRIGHT.md`. The site code and the article/diagram are all rights reserved unless a license is added later. No open-source or Creative Commons license currently applies.

## Contact

After launch, contact will be via LinkedIn. No public email is provided.
