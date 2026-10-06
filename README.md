# Pharma Sales Performance Dashboard (Power BI)

An end-to-end Power BI project analysing distributor-level sales data from a pharmaceutical manufacturer operating in Germany and Poland — from raw CSV to an interactive, multi-page report.

## Tools Used
- **Python (pandas)** – data profiling and sanity checks
- **Power Query** – cleaning and shaping the data
- **Power BI Desktop** – star-schema data model, DAX measures, report design

<img width="1280" height="720" alt="Fiver gig thumnail (2)" src="https://github.com/user-attachments/assets/d62a2fd3-84a6-4985-adc1-2ab39bbd841a" />


## Contents
- [Business Context](#business-context)
- [Questions Answered](#questions-answered)
- [Data](#data)
- [Workflow](#workflow)
- [Report Pages](#report-pages)
- [Key Insights](#key-insights)
- [Running It Yourself](#running-it-yourself)
- [Credits](#credits)
- [Contact](#contact)

## Business Context
A pharmaceutical manufacturer sells through wholesale distributors rather than directly to buyers. Each distributor shares its sales records as CSV files, giving the manufacturer visibility down to individual hospitals and pharmacies. This project turns those records into a reporting tool for three audiences: leadership, sales managers, and the head of sales.

## Questions Answered

| Audience | What they need to know |
|:--|:--|
| Leadership | How are total sales trending over years and months? Which cities, channels, drug classes and individual drugs bring in the most revenue? |
| Sales managers & reps | How do distributors compare? Who are the top 5 products, customers and cities? How do sales split across channels and sub-channels? |
| Head of Sales | Which teams, managers and reps perform best? Which products and product classes drive each team's results? (Filterable by year and month) |

<img width="1438" height="813" alt="Screenshot 2026-10-06 at 7 15 39 AM" src="https://github.com/user-attachments/assets/afbc2bc5-28c7-4c12-a1a5-f8f12e841722" />

## Data
Source: [Foresight BI practice datasets](https://foresightbi.com.ng/practice-data/3-datasets-for-your-portfolio/)

| Column | Meaning |
|:--|:--|
| Distributor | Wholesaler supplying the sale |
| Customer Name | Buying hospital or pharmacy |
| City / Country | Customer location |
| Latitude / Longitude | Coordinates used for map visuals |
| Channel | Buyer type (Hospital, Pharmacy) |
| Sub-channel | Buyer sector (e.g. Government, Private) |
| Product Name / Product Class | Drug and its therapeutic class |
| Quantity / Price / Sales | Units sold, unit price, revenue |
| Month / Year | Time of sale |
| Name of Sales Rep / Manager / Sales Team | Who handled the sale |


<img width="1265" height="707" alt="Screenshot 2026-10-06 at 7 16 07 AM" src="https://github.com/user-attachments/assets/fde13f2a-9c13-4add-9866-5dcc448d3db4" />


## Workflow

### 1. Data profiling (pandas)
Before building anything, I profiled the dataset in Python to check its quality:
- Missing values: **TODO – what you found**
- Negative or unusual values in Quantity/Sales: **TODO – e.g. returns, and how you handled them**
- Category counts and numeric ranges: **TODO – e.g. number of distributors, products, cities**

Notebook: [`data-exploration.ipynb`](data-exploration.ipynb)

<img width="1265" height="707" alt="Screenshot 2026-10-06 at 7 16 14 AM" src="https://github.com/user-attachments/assets/5ae08eb9-b5ac-43df-b33c-30d09df14b6f" />

### 2. Cleaning (Power Query)
- **TODO – e.g. renamed columns, set data types, handled negative sales**

### 3. Data model (Power BI)
The flat CSV mixes descriptive fields and numbers, so I split it into a **star schema**: one fact table of sales transactions surrounded by dimension tables for **TODO – e.g. product, customer, distributor, sales rep, date**.

### 4. Key DAX measures
- **TODO – e.g. Total Sales, Total Quantity, YoY Growth %, Rank by Sales**

## Report Pages

### Overview
Company-wide sales at a glance, with a year filter.

### Distributors & Customers
Distributor comparison with drill-down to products, plus top customers and cities.

### Sales Team
Team, manager and rep performance, broken down by product and product class, with year and month slicers.

## Key Insights
- **TODO – 3 to 5 findings from your dashboard, with numbers.**

## Running It Yourself
- Download [`pharma-analysis.pbix`](pharma-analysis.pbix). The data model is embedded, so no separate dataset download is required. Open it with the free [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/desktop).

## Credits
- Dataset: [Foresight BI](https://foresightbi.com.ng/practice-data/3-datasets-for-your-portfolio/)

## Contact
**Harsh Kumar** · [LinkedIn](https://linkedin.com/in/harshkumar23/) · [GitHub](https://github.com/harshskumar232)
