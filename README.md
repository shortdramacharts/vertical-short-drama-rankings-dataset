# Vertical Short Drama Rankings Dataset (12 Languages)

Open, reproducible snapshots of global vertical short drama (microdrama) rankings and cross-language title mappings published by **[Short Drama Charts](https://shortdramacharts.com/)**.

- **Live Charts**: https://shortdramacharts.com/rankings/
- **12-Language Viewing Guides**: https://shortdramacharts.com/best-short-dramas/
- **Scoring & Data Methodology**: https://shortdramacharts.com/methodology/
- **Latest Snapshot (UTC)**: `2026-11-25`
- **Coverage**: **613 verified localized editions** across **222 distinct works** and **12 languages** (`en, pt, fr, ja, es, ar, de, th, zh-Hant, id, ko, ru`)
- **Update Cadence**: Weekly snapshots pushed every Monday UTC (with dated archive CSVs)

---

## Files Included

| File | Description |
|---|---|
| `data/rankings-latest.csv` / `.json` | Latest snapshot of all 613 localized vertical drama editions with 24-hour and 7-day rank positions, heat index (0–100), platform, genres, episode counts, and canonical detail URLs. |
| `data/rankings-2026-11-25.csv` | Immutable dated archive snapshot for reproducibility and historical comparison. |
| `data/multilingual-title-map.csv` / `.json` | Cross-language title lookup table mapping all 222 distinct vertical dramas across up to 12 languages (`en, es, pt, fr, de, ja, ko, ar, id, th, zh-Hant, ru`). |

---

## Data Dictionary (`rankings-latest.csv`)

| Column | Type | Description |
|---|---|---|
| `snapshot_date_utc` | string (YYYY-MM-DD) | UTC date when the snapshot was exported. |
| `work_slug` | string | Stable work identifier shared across language editions. |
| `language_code` | string (BCP 47) | Edition language (`en`, `ko`, `ja`, `es`, `pt`, `fr`, `de`, `ar`, `id`, `th`, `zh-Hant`, `ru`). |
| `localized_title` | string | Verified localized release title for the given language edition. |
| `canonical_en_title` | string | English catalog reference title (when available). |
| `platform` | string | Primary short-drama streaming platform (e.g. NetShort, DramaBox, ReelShort, GoodShort). |
| `genres` | string | Pipe-delimited genre tags (`romance|werewolf|billionaire|...`). |
| `episodes` | integer | Documented episode count at last verification (blank if unverified). |
| `rank_24h` | integer | Language-level 24-hour chart rank at snapshot time. |
| `rank_7d` | integer | Language-level 7-day rolling chart rank at snapshot time. |
| `heat_24h` / `heat_7d` | float (0–100) | Composite index derived from documented chart placements and search-demand estimates (not official platform stream counts). |
| `data_source` | string | Transparent attribution of underlying ranking inputs. |
| `checked_date` | string (YYYY-MM-DD) | Date the catalog record was last verified. |
| `detail_url` | URL | Permanent public reference page on `shortdramacharts.com`. |

---

## Important Caveats & Transparency

- Heat scores are **composite chart indexes**, not raw official platform view counts or revenue figures.
- Episode counts and language editions only include records verified in our catalog; unverified fields are left blank rather than estimated.
- Full scoring methodology: https://shortdramacharts.com/methodology/

---

## Citation & License

Licensed under **CC BY 4.0**. If you use this dataset in an article, video, newsletter, or research note, please attribute:

> Short Drama Charts (2026-11-25). *Global Vertical Short Drama Rankings & 12-Language Title Dataset*. https://shortdramacharts.com/

Contact & corrections: `contact@shortdramacharts.com`
