# London Housing Market Analysis (1995-2025) 📈🏠

## Project Overview
This project provides a comprehensive analysis of the London property market evolution over the last 30 years. Using the official **UK House Price Index (HPI)** dataset, I conducted an end-to-end data pipeline to uncover regional growth patterns, market decoupling from national benchmarks, and the complex relationship between transaction volumes and property valuations.

This work serves as a practical application of the methodologies mastered during the **IBM Data Analysis with Python** professional certification.

## Executive Summary of Findings
* **Explosive Borough Growth:** Identified "gentrification leaders" such as **Hackney**, which recorded a staggering price appreciation of nearly **900%** since 1995.
* **National Decoupling:** Quantified the widening "London Premium," illustrating how London flat prices now closely mirror detached house prices in the rest of the UK.
* **Price-Volume Dynamics:** Applied non-linear regression (Quadratic) to model market liquidity, revealing how price volatility stabilises as monthly transaction volumes increase.

## Technical Implementation
### Data Pipeline & Engineering
* **ETL Process:** Extracted raw Excel data, handled missing values (encoded as '-' in source), and standardised temporal features.
* **Data Reshaping:** Utilised `melt` and `pivot` operations to transform wide-format government data into tidy data structures for time-series analysis.
* **Statistical Analysis:** Calculated Pearson correlation coefficients globally and per-borough to measure market sensitivity.

### Tech Stack
* **Language:** Python 3.9
* **Libraries:** * `Pandas`: Data manipulation and structural analysis.
    * `Seaborn` & `Matplotlib`: Advanced statistical visualisations and publication-quality charts.
    * `NumPy`: Numerical operations and trend modeling.
* **Environment:** Jupyter Notebook / VS Code.

## Data Dictionary (`df_london_combined`)

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| **Date** | datetime64[ns] | The first day of the month for the recorded data point (e.g., 1995-01-01). |
| **Borough** | object (string) | The specific London local authority/administrative district (e.g., Hackney, Tower Hamlets). |
| **Average_Price** | float64 | The mean residential property price within the borough for that month, measured in GBP (£). |
| **Sales_Volume** | float64 | The total number of registered property sales transactions completed during the month. |

---

### Key Data Features in `df_type` (Benchmark Data)
* **London_Price_Detached/Flat:** Average prices specifically for detached properties and flats in the London region.
* **UK_Price_Detached:** National average price for detached homes, used as a benchmark for regional performance comparison.

## How to Run
1. Clone the repository: `git clone https://github.com/alav23/UK_House_Price.git`
2. Install dependencies: `pip install pandas seaborn matplotlib`
3. Open `London_Analysis.ipynb` in Jupyter or VS Code.

---
**Author:** Annalaura Veglio
**Certification:** IBM Data Analysis with Python (Cognitive Class)


