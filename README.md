# makanapo-data

Published data for **[makana.fm](https://makana.fm)** — the `Makanapō` deals feature
(Honolulu kama'aina discounts & happy-hour deals).

## Contents

| File | Description |
|---|---|
| `deals.json` | The published deal set. Generated daily. |

## CDN

The iOS app reads this file over jsDelivr:

```
https://cdn.jsdelivr.net/gh/tanabe11/makanapo-data@main/deals.json
```

## Notes

- **Generated output — do not edit by hand.** This repository is written automatically by the
  daily build pipeline; manual commits will be overwritten on the next run.
- Every record carries a `last_verified` date and a `status` (`active` / `unverified` / `expired`).
  `unverified` records are discovery leads with a `source_url`, not confirmed deals.
- Records hold **facts only** (name, address, discount terms, hours, source link). No descriptions,
  photos, or article text are copied from sources — always confirm at the linked `source_url`.
