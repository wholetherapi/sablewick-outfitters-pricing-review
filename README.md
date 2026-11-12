# Sablewick Outfitters — Pricing Review

Quarterly price-audit workspace maintained by the category pricing team.

## Repository layout

- `templates/shortlist-template.json` — blank record template (one element)
- `reports/<year>-<quarter>/shortlist.json` — published quarterly shortlists
- `README.md` — format and conventions

## Publishing a quarter

Add `reports/<year>-<quarter>/shortlist.json` on the audit branch for that
quarter (for example, the Q4 2026 shortlist is committed to
`reports/2026-Q4/shortlist.json` on `q4-audit`).

### Shortlist Record Schema

Each shortlist file is a JSON array. Every element is an object with exactly
these five keys:

| key | type | notes |
| --- | --- | --- |
| `item_code` | string | catalog SKU of the product |
| `canonical_url` | string | absolute URL of the product page |
| `display_name` | string | product title exactly as shown on the page |
| `featured_price` | string | current featured-offer price, two decimal places, no currency symbol |
| `offer_seller` | string | seller shown in the featured offer |

Write one element per audited item. Do not add extra keys. Prices are decimal
strings (`"54.00"`), not numbers.

## Quarterly shortlists

- `reports/2026-Q3/shortlist.json` — Camp Lighting shortlist (published)
