## Chen-Che (Jess) Chang

MS in Business Analytics candidate at UCLA Anderson (December 2026), based in Los Angeles. Previously a data analyst at LINE Taiwan and a data and GTM operations intern at Bobyard. BA in Philosophy, National Taiwan University.

[LinkedIn](www.linkedin.com/in/chen-che-chang) · ffrankychang@gmail.com

---

### Holiday release effects on US box office

[Repository](https://github.com/Jess-ChangTW/movie-holiday-boxoffice) · [Project page](https://jess-changtw.github.io/movie-holiday-boxoffice/) · [Tableau story](https://public.tableau.com/app/profile/chen.che.chang1002/viz/holiday_box_office/Story1)

Studios release horror films before Halloween and romance films before Valentine's Day. This project measures whether that strategy pays off, and how much of the effect comes from the holiday itself rather than from studios scheduling their biggest films on those dates.

[![Box office dashboard](https://raw.githubusercontent.com/Jess-ChangTW/movie-holiday-boxoffice/main/images/dashboard_boxoffice.png)](https://public.tableau.com/app/profile/chen.che.chang1002/viz/holiday_box_office/Story1)

**Data.** 56,393 US theatrical titles from the TMDB API, matched to US domestic gross from the OMDb API. Main sample of 2,636 films (2010-2025) with at least $1M gross, excluding re-releases.

**Findings**
- Horror's share of weekly releases rises from a 20% average to 30-34% in the five weeks before Halloween. Romance clusters in the week before Valentine's Day.
- In the Halloween window, horror's median gross is $36.7M vs $22.8M at other times, while the median for all other films falls from $24.1M to $11.3M.
- After controlling for budget, franchise, MPA rating, IMDb rating, year and month, genre-matched films still earn about 50-60% more in holiday windows (horror p ≈ 0.01, romance p ≈ 0.04). About half of the raw premium is explained by studio selection.

**Methods.** Two-proportion z-tests, bootstrap confidence intervals, difference-in-differences on log gross, OLS with a genre x window interaction and robust standard errors, robustness checks across window widths and sample definitions.

**Tools.** Python (pandas, statsmodels), REST APIs, Tableau

---

### NYC housing signals pipeline

UCLA MSBA team project · Pipeline lead · [Repository](https://github.com/Jess-ChangTW/nyc-housing-signals-pipeline)

Tested whether NYC 311 nuisance complaints act as a leading indicator of home value growth at the ZIP-code level, 2020-2024, ahead of slower Census updates. I built the data pipeline, from raw data cleaning in PySpark to the gold table used for analysis.

**What I built**
- PySpark jobs on Google Cloud Dataproc that clean and standardize three sources: NYC 311 Open Data (incremental daily loads, filtered to the needed fields), Zillow Home Value Index (reshaped from a wide monthly time series to long format) and US Census ACS 5-year estimates (income, education, population).
- A two-tier Snowflake warehouse: a staging layer loaded from Parquet files in Google Cloud Storage, and a production star schema with ZIP, year and complaint-type dimensions.
- The gold fact table at ZIP x year grain, joining home values, complaint counts, income and education, with complaints per 1,000 residents, year-over-year changes and signals adjusted against the citywide average for each year.
- SQL validation checks for grain, row counts and missing values.

**Result.** The table powered the team's analysis, which found that changes in complaint rates were weak predictors of home value growth, while income and education were much stronger signals.

**Tools.** PySpark, Google Cloud (GCS, Dataproc), Snowflake, SQL, Python

---

### Other work

**Multi-level genre classification** · UCLA MSBA capstone with Sony Pictures Television (in progress). Visualization and documentation lead.

**Bobyard**, Data & GTM Operations Intern (2026). Built Python scrapers for public contractor license databases in several US states and UK procurement data; cleaned and deduplicated the results and supported customer-profile analysis in SQL.

**LINE Taiwan**, Data Analyst. Community content and short video analytics.

### Skills

Python (pandas, scikit-learn, statsmodels, PySpark), SQL, R, Tableau, Snowflake, Google Cloud, Airflow, Gurobi
