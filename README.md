# Offer Snapshot Audit

This sample report shows a price mismatch between a product list and a saved shop page. The checking software itself is not included.

To view the example:

1. On GitHub, choose **Code > Download ZIP**.
2. Extract the ZIP file.
3. Open [sample-report/report.html](sample-report/report.html) in a browser, or open [report.json](sample-report/report.json) for raw results.

The sample compares a CSV with saved product-page HTML. For example, the CSV says **10.00 EUR**, while the page says **12.00 EUR**: the report marks **MISMATCH**. Missing or unclear page information is **UNKNOWN**; invalid CSV rows are **INVALID_INPUT**.

The sample is fictional and uses the reserved `.test` domain. It does not fetch live pages, change your product list or shop, run JavaScript, access Merchant Center/accounts, or prove Google approval.

This is only a static example. The software is not public here; there is no checkout or software licence grant.

See the [input contract](docs/input-contract.md) and [expected results](docs/expected-results.md) for details.

To share feedback, use [New issue > Synthetic workflow feedback](https://github.com/Somitsadev/offer-snapshot-audit-demo/issues/new/choose). Tell us what you do now to compare a product list with a shop page, and whether preparing these files for an offline report would be useful. Use invented values only; do not upload files or include private data, live URLs, credentials or customer information.

Offer Snapshot Audit is not affiliated with Google or Merchant Center.
