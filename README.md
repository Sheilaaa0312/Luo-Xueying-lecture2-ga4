# IC/CP-W05 — BigQuery SQL Lecture 2

**Author:** Xueying Luo  
**Lecture:** Intermediate/Advanced BigQuery for GA4  
**Date:** October 26, 2026

## Six main topics, ten examples

| Lecture topic | Separate SQL queries / screenshots |
| --- | --- |
| 1. CTEs (`WITH`) | Query 1 |
| 2. Arrays + `UNNEST` | Queries 2 and 3 |
| 3. `STRING_AGG`, `ARRAY_AGG` | Queries 4, 5, and 6 |
| 4. Joins | Query 7 |
| 5. Window functions + `QUALIFY` | Queries 8 and 9 |
| 6. Approximate functions | Query 10 |

The original lecture contains **six topic headings** and **ten executable examples**. All ten are retained because the assignment asks for each SQL query, its explanation, and its output screenshot.

## Three files to submit to Canvas

1. `Luo-Xueying-lecture2-ga4.qmd` — Quarto notebook containing fenced, non-executing SQL code, explanations, screenshot evidence, and appendix links.
2. `Luo-Xueying-lecture2-ga4.html` — self-contained HTML with the ten screenshots embedded.
3. `Luo-Xueying-lecture2-ga4.sql` — all ten queries arranged under the six lecture topics and organized with SQL comments.

## Other files in this project

- `images/query-01.png` to `images/query-10.png` — all ten genuine screenshots of BigQuery results.
- `styles.css` — optional custom styling for an HTML render.
- `index.html` — copy of the HTML report to serve via GitHub Pages.
- `bigquery-lecture-2.Rproj` — RStudio project file.

Keep the `images/` directory in the same project folder as the `.qmd` when editing or rendering in Quarto.

## Required before final Canvas submission: Publish and verify GitHub links

The report includes the intended URLs below, **but they were not confirmed as published or working at the time this package was prepared**:

- Repository: https://github.com/Sheilaaa0312/Luo-Xueying-lecture2-ga4
- GitHub Pages: https://sheilaaa0312.github.io/Luo-Xueying-lecture2-ga4/

1. Create or open a public GitHub repository named `Luo-Xueying-lecture2-ga4`.
2. Open the local RStudio/Positron project and connect it to that repository. Use **Git commit and push** to upload the project files (including `index.html`).
3. Go to **GitHub repository → Settings → Pages → Deploy from a branch** and select `main`, `/(root)`.
4. Verify both links work. The final HTML must contain a clickable link to the live GitHub Pages report, as required by your instructor.
5. If you edit the `.qmd`, render it in Quarto and make sure `index.html` contains that latest HTML before pushing again.
6. Submit the three deliverables above on Canvas only **after** GitHub Pages is working.

## Accuracy notes

- Query 6 preserves the lecture's alias `total_add_to_cart_events`, but `COUNT(*)` counts **unnested item rows**, not necessarily separate add-to-cart events.
- Query 7 computes distinct transactions per user × 100. This is not exactly the fraction of users who completed a purchase. Its transaction ID field uses `ecommerce.transaction_id`, matching the successfully executed query in the screenshot.
- Query 9 uses a rolling window of seven available daily rows. If dates with no purchases were absent, the window would not be seven consecutive calendar days.

The BigQuery screenshots show the user executed the ten SQL examples successfully. The HTML output is packaged as a standalone file with embedded images. No new BigQuery execution was performed while revising the report.
