# Final Project — Infectious Disease Statistics

This project uses PostgreSQL to normalize and analyze the `infectious_cases` dataset and implement SQL functions for date and disease-indicator calculations.

## Dataset

- **Source:** Course-provided `infectious_cases.csv`, included in `data/`

- **Size:** 10,521 records, 12 columns, 245 geographic entities

- **Coverage:** Annual disease indicators for countries, regions, and geographic groups, 1920–2023

## Implementation

1. Create the `pandemic` schema and import the source CSV into a raw table.

2. Normalize the data into `pandemic.entities` (245 entities) and `pandemic.stat` (10,521 annual records), with PK, FK, and UNIQUE constraints.

3. Calculate average, minimum, maximum, and total rabies indicators; return the top 10 by average.

4. Calculate full years elapsed since January 1 of each observation year.

5. Create and test `years_since()` and `average_cases_per_period()` for monthly, quarterly, and semiannual averages.

## Repository

- `fp_Kalashnikov_Mykola.ipynb` — queries, explanations, and saved outputs

- `data/infectious_cases.csv` — original input file

- `screenshots/` — SQL queries, tables, and results

- `README.md` — project overview and instructions

## How to Run

1. Download `data/infectious_cases.csv` from this repository to your computer, keeping its original filename.

2. Open the notebook in **Google Colab** and select **Runtime → Restart session and run all**.

3. When `files.upload()` prompts you, select the downloaded `infectious_cases.csv`. It will be placed at `/content/infectious_cases.csv`.

4. The notebook installs dependencies, launches local PostgreSQL with `pgserver==0.1.4`, and runs the SQL analysis.

**Note:** Opening the notebook in Colab does not automatically copy the repository CSV into Colab. Upload it when prompted. Internet access is required for dependency installation; no separate database server is needed. Results using `CURRENT_DATE` depend on the execution date.
