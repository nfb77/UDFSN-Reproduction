# UDFSN-Reproduction README

This repository contains the replication code and accompanying datasets used to produce the descriptive figures presented in the manuscript:

> **Forster-Benson, Nicholas.** *Upzoning, Density, and the Financialization of Space in Nashville.*

---
## File Information
- **Data file names:** `df_indexed_rent.csv`,`growth_df_adj.csv`,`master_df.csv`,`vacancy_growth_df.csv`,`pop_growth.csv`
- **Rmd file name:** `UDFSN Reproduction.Rmd`
- **Data file names:**
│   ├── nashville_cbd_tract_rent_2000_2022.csv
│   ├── nashville_cbd_tract_price_2000_2022.csv
│   ├── nashville_cbd_tract_income_2000_2022.csv
│   ├── US_rent_2000_2022.csv
│   ├── US_price_2000_2022.csv
│   └── US_income_2000_2022.csv
- **Output:** [View PDF document](UDFSN Reproduction.pdf)

---

## Nashville CBD Datasets

Three datasets contain annual estimates for census tracts located within downtown Nashville (CBD) and adjacent comparison tracts.

| Dataset | Description |
|----------|-------------|
| `nashville_cbd_tract_rent_2000_2022.csv` | Median gross rent by tract and year |
| `nashville_cbd_tract_price_2000_2022.csv` | Median owner-occupied housing value by tract and year |
| `nashville_cbd_tract_income_2000_2022.csv` | Median household income by tract and year |

Each dataset contains observations for:

- Census year
- Census tract
- Geographic classification (`CBD` or `Adjacent`)
- Estimate
- Margin of error (ACS years)

The replication code aggregates tract-level observations into annual averages for:

- Core CBD
- Average adjacent tracts

---

## National Comparison Datasets

National median values are included for comparison.

| Dataset | Description |
|----------|-------------|
| `US_rent_2000_2022.csv` | U.S. median gross rent |
| `US_price_2000_2022.csv` | U.S. median home value |
| `US_income_2000_2022.csv` | U.S. median household income |

---

# Data Sources

The datasets were compiled from publicly available sources.

### U.S. Census Bureau

- Census 2000 Summary File 3
- 2010 Census tract definitions
- American Community Survey (ACS) 5-Year Estimates (2005–2022)

Tables used include:

- **B25064** – Median Gross Rent
- **B25077** – Median Value of Owner-Occupied Housing Units
- **B19013** – Median Household Income
- Historical Census 2000 equivalents:
  - H063001
  - H085001
  - P053001

### Nashville Downtown Partnership

Nashville Downtown Partnership (2025).

*Annual Residential Report 2025.*

Used to extend downtown rent and population estimates through 2025.

### U.S. Department of Housing and Urban Development (HUD)

American Housing Survey national rental statistics used as comparison benchmarks.

---

# Software Requirements

The replication script was developed in **R**.

Required packages include:

```r
ggplot2
dplyr
tidyr
readr
scales
fixest
knitr
tidycensus
purrr
httr
lubridate
```

Install missing packages using:

```r
install.packages(c(
  "ggplot2",
  "dplyr",
  "tidyr",
  "readr",
  "scales",
  "fixest",
  "knitr",
  "tidycensus",
  "purrr",
  "httr",
  "lubridate"
))
```

---



# Geographic Definitions

The analysis focuses on downtown Nashville using Census tract definitions corresponding to the central business district (CBD).

Comparison areas consist of immediately adjacent census tracts, allowing the manuscript to contrast changes within the upzoned downtown against nearby neighborhoods over time.

---


# Contact


Email: <mailto:nforstebenson@g.harvard.edu>

---
