# Input contract

The example uses a normalized product export and saved product-page HTML. It does not fetch or modify either input.

## Feed

The CSV header must be exactly:

~~~text
id,link,price,currency,availability
~~~

Each row needs:

- `id`: a stable safe filename token mapping to `pages/<id>.html`;
- `link`: an HTTP(S) product URL supplied as data; it is never fetched;
- `price`: a finite, non-negative decimal;
- `currency`: exactly one of `EUR`, `USD` or `GBP`;
- `availability`: one of `in_stock`, `out_of_stock`, `preorder` or `backorder`.

The sample uses fictional IDs and `.test` URLs. Do not replace them with live or customer data in a public example.

## Saved page

A saved HTML file may contain a JSON-LD script with a Product and an Offer. The supported comparison fields are:

- Offer price;
- Offer priceCurrency, restricted to EUR, USD or GBP;
- Offer availability, using the documented schema.org availability aliases.

The association must be unambiguous through the product ID or canonical URL and a single comparable offer. Missing, malformed, conflicting or ambiguous page evidence is UNKNOWN. A missing or malformed required feed field is INVALID_INPUT. The diagnostic must not guess.

## Interpretation

- **MATCH:** all three supported fields are readable and equal after documented normalization.
- **MISMATCH:** the selected structured offer is readable and at least one supported field differs.
- **UNKNOWN:** page evidence is absent, malformed, ambiguous or not comparable.
- **INVALID_INPUT:** the normalized feed row is structurally or semantically invalid.

These labels describe the supplied snapshots only. They do not explain Google’s internal systems or guarantee remediation.

