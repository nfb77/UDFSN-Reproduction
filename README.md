# UDFSN-Reproduction README

This repository contains the replication code and accompanying datasets used to produce the descriptive figures presented in the manuscript:

 **Forster-Benson, Nicholas.** *Upzoning, Density, and the Financialization of Space in Nashville.*

---
## File Information
- **Rmd file:** `UDFSN Reproduction.Rmd`
- **Data file:** `nashville_cbd_tract_rent_2000_2022.csv`, `nashville_cbd_tract_price_2000_2022.csv`, `nashville_cbd_tract_income_2000_2022.csv`, `US_rent_2000_2022.csv`, `US_price_2000_2022.csv`, `US_income_2000_2022.csv`
- **Output:** [View PDF document](<UDFSN-Reproduction.pdf>) (`UDFSN-Reproduction.pdf`)

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

NDP (2008). Annual residential report 2008. Technical report, Nashville Downtown Part-
nership. <https://ctycms.com/tn-nashville/docs/residential_report_2008.pdf>.

NDP (2025). Annual residential report 2025. Technical report, Nashville Downtown Partnership. <https://ctycms.com/tn-nashville/docs/2025-residential-report-1.pdf>.

Used for all population estimates.

Used to extend downtown rent estimates through 2025.

### U.S. Department of Housing and Urban Development (HUD)

American Housing Survey national rental statistics used as comparison benchmarks.

---


### Geographic Classification

The Nashville datasets classify census tracts into two categories:

- **Core CBD** — Census tracts comprising downtown Nashville.
- **Adjacent Tracts** — Census tracts whose centroids fall within **3 kilometers** of the Core CBD. This comparison group was held constant within each decennial Census geography to account for boundary changes over time.

Because Census tract boundaries were redrawn in 2010 and again in 2020, separate tract definitions are used for each Census geography.

#### Census 2000 Geography
*Used for 2000 Census data and 2005–2009 ACS estimates.*

**Core CBD**

- Tract 146 (FIPS: 47037014600)
- Tract 147 (FIPS: 47037014700)

**Adjacent Tracts (3 km buffer)**

127.02, 113, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 149, 159, 160, 161, 162, 163, 164, 165, 166, 168, 169, 170, 171, and 172.

#### Census 2010 Geography
*Used for 2010 Census data and 2011–2019 ACS estimates.*

**Core CBD**

- Tract 195 (FIPS: 47037019500)

**Adjacent Tracts (3 km buffer)**

113, 117, 118, 119, 121, 122, 126, 127.02, 134, 135, 136.01, 136.02, 137, 138, 139, 142, 143, 144, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 172, 173, 192, 193, 194, and 196.

#### Census 2020 Geography
*Used for 2020–2022 ACS estimates.*

**Core CBD**

- Tract 195.02 (FIPS: 47037019502)
- Tract 195.03 (FIPS: 47037019503)

**Adjacent Tracts (3 km buffer)**

113, 117, 118, 119, 121, 122, 126, 127.02, 134, 135, 136, 137.01, 137.02, 138, 139, 142, 143, 144, 159, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 172, 173, 192, 193, 194.01, 194.02, 195.01, and 196.

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


# Contact


Email: <a href="mailto:nforsterbenson@fas.harvard.edu">nforsterbenson@fas.harvard.edu</a>

---
