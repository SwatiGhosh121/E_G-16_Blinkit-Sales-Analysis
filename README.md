# E_G-16_Blinkit-Sales-Analysis

Blinkit sales, operations, and customer analytics project with a staged workflow for data validation, ETL, analysis, and dashboard delivery.

## Project Objective

Build a decision-ready analytics pipeline for Blinkit by:
- validating dataset quality and fit at Gate 1,
- standardizing and cleaning raw data,
- running EDA and statistical analysis,
- preparing final dashboard-ready data,
- publishing a Tableau Public dashboard with interactive filters.

## Folder Structure And File Explanations

### Root Files
- `README.md`: Master project guide, execution plan, and deliverables tracker.
- `etl_log_blinkit_updated.docx`: External ETL notes/log (reference artifact).

### `data/raw/` (Never Edit In Place)
Raw source files committed as immutable inputs:
- `blinkit_customer_feedback.csv`: Customer reviews, ratings, and feedback text/labels.
- `blinkit_customers.csv`: Customer profile and demographic-level attributes.
- `blinkit_delivery_performance.csv`: Delivery timelines and SLA-related fields.
- `blinkit_inventory.csv`: Base inventory snapshot/details.
- `blinkit_inventory_new.csv`: Additional/updated inventory extract.
- `blinkit_marketing_performance.csv`: Campaign-level performance metrics.
- `blinkit_order_items.csv`: Order line-item granularity data.
- `blinkit_orders.csv`: Order-level transaction records.
- `blinkit_products.csv`: Product catalog and category mappings.
- `category_icons.xlsx`: Category icon metadata/reference.
- `Rating_Icon.xlsx`: Rating icon metadata/reference.

### `data/processed/`
- `blinkit_cleaned_dashboard_data.csv`: Cleaned and standardized dataset used for dashboarding and analysis.

### `notebooks/`
- `02_cleaning.ipynb`: ETL cleaning pipeline and transformation log.
- `03_eda.ipynb`: Exploratory data analysis (trends, distributions, outliers).
- `04_statistical_analysis.ipynb`: Correlation, regression, and hypothesis testing as applicable.
- `05_final_load_prep.ipynb`: KPI computation and final Tableau load preparation.

### `docs/`
- `gate_1_proposal.md`: Gate 1 submission draft (problem statement + dataset link + approval checkpoint).
- `initial_data_dictionary.md`: Initial data dictionary template.
- `dataset_backup_options.md`: Backup dataset options from the same sector.

### `deliverables/tableau_screenshots/`
Stores published dashboard screenshots for GitHub submission.

## Renames Completed

The following naming cleanups were applied for consistency:
- `FINAL(3)_CLEANED_DASHBOARD_DATA (1).csv` -> `data/processed/blinkit_cleaned_dashboard_data.csv`
- `data/raw/blinkit_orders (1).csv` -> `data/raw/blinkit_orders.csv`
- `data/raw/Category_Icons (1).xlsx` -> `data/raw/category_icons.xlsx`
- `data/raw/blinkit_inventoryNew.csv` -> `data/raw/blinkit_inventory_new.csv`
- `ETL_Log_Blinkit_Updated.docx` -> `etl_log_blinkit_updated.docx`

## Execution Plan (As Requested)

### Day 3: Gate 1 - Go/No-Go Checkpoint
- Submit Gate 1 proposal with:
	- problem statement,
	- dataset link,
	- initial data dictionary.
- Wait for mentor approval before deep analysis.
- Keep at least 2 backup datasets ready from the same sector.

Primary files:
- `docs/gate_1_proposal.md`
- `docs/initial_data_dictionary.md`
- `docs/dataset_backup_options.md`

### Day 4-5: ETL Pipeline And Cleaning
- Commit raw data only in `data/raw/` (no in-place edits).
- Build and log cleaning pipeline in `notebooks/02_cleaning.ipynb`.
- Write cleaned output to `data/processed/`.
- Commit notebooks and processed artifacts to GitHub.

Deliverable:
- Fully standardized cleaned dataset, ready for analysis.

### Week 2 Objective
Uncover insights, build Tableau dashboard, and finalize reporting.

### Day 6-7: EDA And Statistical Analysis
- Run EDA in `notebooks/03_eda.ipynb`.
- Run statistical analysis in `notebooks/04_statistical_analysis.ipynb`.
- Compute KPIs and prepare final load in `notebooks/05_final_load_prep.ipynb`.

### Day 8-9: Tableau Dashboard
- Build dashboard in Tableau Public for decision-making.
- Include interactive filters (no hard-coded numbers).
- Publish dashboard and store screenshots in `deliverables/tableau_screenshots/`.
- Record public URL in project documentation/README after publishing.

## Git Workflow Notes
- Keep `data/raw/` immutable.
- Add all transformations to notebook logs and markdown notes.
- Commit frequently by milestone (Gate 1, ETL complete, EDA complete, Stats complete, Dashboard complete).
