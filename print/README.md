# Print / PDF

**No PDF is generated yet.** A downloadable PDF of the case study is planned at
launch. It is produced only from the final, appendix-free HTML **after** the
lifecycle wording and release state are final, so a last bounded text update (if
any) is not stranded in a stale export.

## Reproducible export (at release, operator-approved)

1. Open `case-studies/human-review-band/index.html`.
2. Print → **Save as PDF**.
3. Paper A4 or Letter; margins Default; background graphics off.
4. Save as `the-human-review-band-is-the-product.pdf`.

Proposed location once released: `documents/the-human-review-band-is-the-product.pdf`.

## Print stylesheet

`assets/styles.css` (`@media print`) switches to a white palette, hides the
header/nav/footer note, keeps the draft banner as an outlined note, avoids page
breaks after headings and inside the figure and blockquote, and adds page
numbers.

## Appendix exclusion

The PDF is exported from the HTML case-study page, which contains only the
public article. There is no appendix in any HTML source; do not export from any
other source.
