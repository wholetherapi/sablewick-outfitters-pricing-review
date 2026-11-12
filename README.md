# Fernhollow Outfitters — Pricing Review

Quarterly price-audit workspace maintained by the category pricing team.

## Repository layout

- `templates/shortlist-template.json` — blank record template
- `reports/` — one folder per quarter, e.g. `reports/2026-Q3/shortlist.json`

## Publishing a quarter

Create or update `reports/<year>-<quarter>/shortlist.json` on the audit branch for that quarter.

### Shortlist Record Schema

Every shortlist is a JSON array. Each element is an object with exactly these five keys:

| key | type | meaning |
| --- | --- | --- |
| `item_code` | string | catalog SKU of the product |
| `canonical_url` | string | absolute URL of the product page |
| `display_name` | string | product title exactly as shown on the page |
| `featured_price` | string | current featured-offer price, two decimal places, no currency symbol |
| `offer_seller` | string | seller shown in the featured offer |

Do not add extra keys. Prices are decimal strings (`"54.00"`), not numbers.
