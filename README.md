# Offer Snapshot Audit

Offer Snapshot Audit is a static demonstration of a narrow offline diagnostic for investigating price and availability differences between a normalized product export and saved product-page HTML.

The examples use fictional products and the reserved `.test` host. No live site, account or customer data is involved.

## What the example shows

The supported input is:

- one CSV with the exact header `id,link,price,currency,availability`;
- one saved HTML file per row at `pages/<id>.html`;
- JSON-LD structured data containing a Product and one unambiguous Offer.

The comparison checks price, currency and availability in the supplied files and produces evidence suitable for JSON and HTML reporting. Clear equality is **MATCH**, a clear difference is **MISMATCH**, missing or ambiguous page evidence is **UNKNOWN**, and malformed required feed rows are **INVALID_INPUT**.

This repository is a static worked example, not runnable software. The executable beta is separate and is not included here; this repository has no checkout or software license grant. To inspect the example, open [report.html](sample-report/report.html) in a browser or download [report.json](sample-report/report.json) for machine-readable results. The sample inputs and expected classifications are in [samples/input](samples/input) and [docs/expected-results.md](docs/expected-results.md).

## Limits

The diagnostic does not:

- fetch URLs or make network requests;
- access Merchant Center, Search Console, accounts or credentials;
- execute JavaScript or test rendered, checkout, geo, device, shipping or regional behavior;
- infer values when page evidence is absent or ambiguous;
- promise a Google diagnosis, approval, ranking, eligibility or revenue result.

A **MATCH** means that the supported values in the supplied snapshots agree under the documented rules. It is not evidence that Google will accept or reapprove a product. See the [input contract](docs/input-contract.md) for the supported field and classification rules.

## Feedback

If you have a first-hand workflow involving this kind of mismatch, you can request beta access or suggest a useful feature through the [feedback issue form](.github/ISSUE_TEMPLATE/feedback.yml), when enabled. Describe the problem and general workflow using synthetic values only. Do not upload files or include live URLs, product IDs, customer information, credentials, account details or copied page source.

Offer Snapshot Audit is not affiliated with Google, Merchant Center or any referenced platform.
