# US Fragrance Trends 2026 — Most-Searched Fragrance In Every US State

**Original research dataset by [PerfumeM](https://perfumem.com)** — published May 2026

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

---

## Overview

This dataset analyzes 12 months of Google Trends interest-by-region data across 30 of the most-talked-about fragrances of 2024–2026 (designer, niche, viral / TikTok, and celebrity scents), broken down by all 51 US states and the District of Columbia.

**Headline finding:** Old Spice ranks as the most-searched fragrance in 43 states. **Eight states pick something completely different** — and the pattern reveals significant outlier preferences:

| State | #1 Searched Fragrance | Category |
|---|---|---|
| Alaska | Coco Mademoiselle (Chanel) | Designer luxury women's |
| Louisiana | Polo Blue (Ralph Lauren) | Designer men's |
| Mississippi | Polo Blue (Ralph Lauren) | Designer men's |
| Montana | Marc Jacobs Daisy | Designer women's |
| New Mexico | Ariana Grande Cloud | Celebrity / viral |
| North Dakota | Glossier You | Niche / clean beauty |
| South Dakota | Coco Mademoiselle (Chanel) | Designer luxury women's |
| Vermont | Glossier You | Niche / clean beauty |

Read the full analysis: **https://perfumem.com/blogs/news/most-searched-fragrance-by-us-state-2026**

---

## What's in this repository

```
us-fragrance-trends-2026/
├── data/
│   ├── winning_fragrance_per_state.csv    # State → top-searched fragrance + score + 2nd place
│   └── raw_interest_by_state.csv          # Full matrix (30 fragrances × 51 regions)
├── charts/
│   ├── 01-states-won-bar.png              # Bar chart: # of states each fragrance dominates
│   ├── 02-us-state-map.png                # US choropleth map of state winners
│   └── 03-outlier-states.png              # The 8 states that reject Old Spice + their picks
├── LICENSE                                 # CC BY 4.0 — free to use with attribution
└── README.md                               # This file
```

---

## Data dictionary

### `winning_fragrance_per_state.csv`

| Column | Description |
|---|---|
| `state` | US state name (or "District of Columbia") |
| `winning_fragrance` | Highest-scoring fragrance in that state from our 30-fragrance set |
| `score` | Relative interest score 0–100 (Google Trends standard) for the winner |
| `second_place` | Second-highest fragrance |
| `second_score` | Relative interest score for #2 |

### `raw_interest_by_state.csv`

Wide matrix. Rows = US states. Columns = 30 fragrances. Cells = relative interest score 0–100.

---

## Methodology

PerfumeM pulled Google Trends `interest_by_region` data (geographic resolution = US state, time horizon = 12 months ending May 2026) for 30 fragrances selected to represent the breadth of American fragrance search behavior:

- **Men's designer staples:** Dior Sauvage, Bleu de Chanel, Acqua di Gio Profondo, Versace Eros, Polo Blue, Yves Saint Laurent Y, Tom Ford Tobacco Vanille, Creed Aventus
- **Women's bestsellers:** Chanel No 5, YSL Black Opium, Marc Jacobs Daisy, Viktor Rolf Flowerbomb, Lancome La Vie Est Belle, Gucci Bloom, Coco Mademoiselle, J'adore Dior, Light Blue Dolce Gabbana
- **Niche / luxury:** Maison Francis Kurkdjian Baccarat Rouge 540, Le Labo Santal 33, Tom Ford Lost Cherry, Byredo Mojave Ghost, Jo Malone English Pear Freesia
- **Viral / TikTok:** Phlur Missing Person, Sol de Janeiro Cheirosa 62, Glossier You
- **Celebrity:** Ariana Grande Cloud
- **Designer evergreens / mass-market:** Aventus Cologne, Old Spice, Ellis Brooklyn Myth

For each US state and DC, we identified the fragrance with the highest relative search interest score (Google Trends 0–100 scale). State-level rankings reflect search volume relative to total search activity within that state, normalized across the 30-fragrance set.

### Limitations

- Google Trends scores are **relative**, not absolute volume.
- The 30-fragrance set is intentionally curated rather than exhaustive — a state's "winning" fragrance is the most-searched within our index, not necessarily the single most-searched fragrance in the entire Google index.
- Excluding mass-market terms like "Old Spice" from the analysis would surface different state-level winners that are obscured by its dominance. We left it in to surface the outlier story.

---

## Use cases

This dataset is suitable for:

- **Journalism / data stories** — state-by-state consumer behavior trend reporting
- **Academic research** — fragrance market segmentation, regional consumer preference studies
- **Marketing analysis** — competitive intelligence for fragrance brands and retailers
- **AI / ML training** — entity recognition for US fragrance market, regional preference modeling

---

## Citation

If you use this dataset in research, journalism, articles, blog posts, or any public-facing work, please cite as:

> PerfumeM. (2026). *US Fragrance Trends 2026: Most-Searched Fragrance In Every US State.* Retrieved from https://perfumem.com/blogs/news/most-searched-fragrance-by-us-state-2026

Or in BibTeX:
```bibtex
@dataset{perfumem_us_fragrance_2026,
  author       = {PerfumeM},
  title        = {US Fragrance Trends 2026: Most-Searched Fragrance In Every US State},
  year         = {2026},
  publisher    = {PerfumeM},
  url          = {https://perfumem.com/blogs/news/most-searched-fragrance-by-us-state-2026}
}
```

---

## License

This dataset is released under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

You are free to:

- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

Under the following terms:

- **Attribution** — You must give appropriate credit to **[PerfumeM (https://perfumem.com)](https://perfumem.com)**, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests PerfumeM endorses you or your use.

Full license text: [LICENSE](./LICENSE)

---

## About PerfumeM

[PerfumeM](https://perfumem.com) is an independent fragrance e-commerce platform built around full-page research dossiers for every product. Each of the 3,000+ fragrances in the catalog comes with a dedicated page covering scent composition, performance benchmarks, climate scoring, and perfumer attribution — far beyond the thin marketing copy most fragrance retailers offer.

- **Website:** https://perfumem.com
- **Founder:** Ahmad Khan
- **Wikidata:** [Q139795065](https://www.wikidata.org/wiki/Q139795065)
- **Data inquiries:** info@perfumem.com

---

## Updates + future datasets

This is the first in an ongoing series of fragrance industry datasets PerfumeM will publish. Follow this repo for updates, and check **https://perfumem.com/blogs/news** for full analyses.

Planned upcoming datasets:
- Father's Day Cologne Performance Index (June 2026)
- Heat-Stability Fragrance Report Summer 2026 (July 2026)
- Holiday Gifting Fragrance Trends (November 2026)

---

## Contact

For media inquiries, custom data slices, or expert commentary on US fragrance market trends:

**info@perfumem.com**

---

*Dataset published 2026-05-14. Methodology and findings validated. Free to use under CC BY 4.0 with attribution to [PerfumeM](https://perfumem.com).*
