COVID-19 Data Analysis Dashboard

An exploratory data analysis project that examines COVID-19 confirmed cases, deaths, and recoveries by country/region using Python and Power BI. The project combines data inspection and visualization in a Jupyter Notebook with an interactive dashboard for summarizing key metrics and comparing regions.

Project Overview

The notebook analyzes a COVID-19 dataset containing 321 records and six fields: Date, State, Region, Confirmed, Deaths, and Recovered. The records shown in the notebook are dated 29 April 2020.

The Power BI report presents summary KPI cards, a region slicer, regional comparisons, a table of key metrics, and a funnel visual for confirmed, recovered, and death totals.

Objectives

Inspect the dataset structure, data types, and missing values.

Explore COVID-19 cases, deaths, and recoveries across regions.

Identify regions with the highest confirmed-case totals and compare death counts.

Filter records with fewer than 10 confirmed cases for part of the analysis.

Build a Power BI dashboard to communicate the main metrics visually.

Tools & Technologies

Python

Pandas — data inspection, filtering, grouping, aggregation, and sorting

Seaborn & Matplotlib — exploratory charts and missing-value visualization

Jupyter Notebook — analysis workflow

Microsoft Power BI — KPI cards, slicer, bar charts, table, and funnel chart

Dataset

The notebook expects a CSV file named 4. Covid_19_data.csv with the following columns:

Column

Description

Date

Date associated with the record

State

State/province when available

Region

Country or region

Confirmed

Confirmed COVID-19 cases

Deaths

Reported deaths

Recovered

Reported recoveries

Data note: The notebook's displayed dataset has 321 rows. State contains 181 missing values, while the other five columns have no missing values in the initial inspection. The analysis reflects a historical snapshot, not current COVID-19 statistics.

Analysis Performed

Loaded the data with Pandas and inspected sample rows, dimensions, column information, and non-null counts.

Checked missing values using Pandas and visualized them with a Seaborn heatmap.

Created exploratory scatter, line, and bar plots.

Grouped records by Region and aggregated confirmed cases, deaths, and recoveries.

Sorted regional totals to compare high- and low-count regions.

Filtered out records where Confirmed < 10 for the subsequent notebook analysis.

Queried India's record for 29 April 2020 and sorted the dataset by confirmed cases in ascending and descending order.

Built a Power BI report with KPI cards, a region slicer, regional bar charts, a summary table, and a funnel visual.

Key Findings from the Notebook

The dataset contains 321 records in the initial load.

181 State values are missing, so that field should be treated carefully in any state-level analysis.

In the notebook's regional aggregation, the United States (US) has the highest confirmed-case total: 1,039,909.

The India record shown for 29 April 2020 reports 33,062 confirmed cases, 1,079 deaths, and 8,437 recoveries.

The notebook also compares regional death and recovery totals and filters out records with fewer than 10 confirmed cases.

These findings are specific to the dataset and analysis captured in this project; they should not be interpreted as current figures.

Repository Structure

Suggested GitHub repository layout:

covid-19-data-analysis/
├── 4.covid-19.ipynb
├── covid-19 analysis.pbix
├── 4. Covid_19_data.csv
└── README.md

Add the CSV only if you have permission to redistribute it. If you do not include it, add a note explaining where the dataset can be obtained.

How to Run the Python Notebook

Install Python and Jupyter Notebook, or use Google Colab.

Install the required libraries:

pip install pandas seaborn matplotlib jupyter

Place the dataset CSV in the project folder.

Open 4.covid-19.ipynb.

Update the CSV path in the notebook's pd.read_csv(...) cell to a relative path, for example:

data = pd.read_csv("4. Covid_19_data.csv")

Run the notebook cells in order.

How to View the Power BI Dashboard

Install Microsoft Power BI Desktop.

Open covid-19 analysis.pbix.

Use the region slicer to explore the report's regional visuals and metrics.

Notes and Limitations

This is a historical analysis based on records dated 29 April 2020, not a live or predictive COVID-19 model.

The notebook uses a local Windows file path. Replace it with a relative path before publishing so other users can run the notebook.

Missing State values are present in the source data.

The filter Confirmed < 10 modifies the in-memory DataFrame for later notebook cells; rerun the notebook from the beginning to reproduce the original state.

Validate metric definitions and Power BI calculations before using the dashboard for formal reporting.

Skills Demonstrated

Data cleaning and inspection, exploratory data analysis (EDA), missing-value analysis, aggregation with Pandas, sorting and filtering, data visualization, KPI reporting, and dashboard development in Power BI.
