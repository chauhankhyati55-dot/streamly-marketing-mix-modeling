

# Streamly+ Marketing Mix Modeling (MMM) Project – R Implementation
Marketing Mix Modeling (MMM) project for Streamly+, a fictional streaming service. Includes 2 years of simulated weekly marketing data, adstock and saturation transformations, incremental channel impact analysis, marginal ROI estimation, and budget optimization using R.

This repo contains a realistic end-to-end Marketing Mix Modeling project for a fictional subscription video streaming service, **Streamly+**.

## Objective

Estimate the incremental impact of different marketing channels (Meta, Search, YouTube, Display, Email) on weekly new subscriptions and explore how to reallocate budget to improve performance.

## Tech Stack

- Language: **R**
- Key packages: `tidyverse`, `lubridate`, `broom`

## Data

- **File:** `data/mmm_streamly.csv`
- **Rows:** 104 weeks (2 years)
- **Columns (main):**
  - `spend_meta`, `spend_search`, `spend_youtube`, `spend_display`, `spend_email`
  - `seasonality_index`
  - `competitor_index`
  - `promo_flag`
  - `subs_new` (weekly new subscriptions)

The dataset is synthetic but generated using a realistic data-generating process with:

- Adstock (carryover) effects on media
- Diminishing returns (saturation via log transform)
- Seasonality
- Competitor activity spikes
- Promotional periods

## Structure

```text
streamly_mmm_project/
├── data/
│   └── mmm_streamly.csv
├── scripts/
│   ├── generate_mmm_data.R   # creates the dataset
│   └── mmm_model.R           # fits the MMM and analyzes results
└── README.md
