# Expected results

This synthetic sample contains no live site data.

| Row ID | Expected status | Reason |
|---|---|---|
| `match` | MATCH | Price 19.90 EUR and `InStock` agree with the feed. |
| `mismatch` | MISMATCH | The saved page price differs from the feed price. |
| `ambiguous` | UNKNOWN | More than one Offer is present without an unambiguous matching offer identity. |
| `unknown` | UNKNOWN | The page has no supported structured Offer evidence. |

These classifications describe the supplied snapshots only. They are not customer results and do not predict a Google decision.

