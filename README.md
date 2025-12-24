# EdTech Market Potential Analysis: World Bank Education Data

## Project Overview

This repository contains a Jupyter Notebook detailing an **Exploratory Data Analysis (EDA)** of the World Bank's Education Statistics (EdStats) dataset. The primary goal of this analysis is to provide strategic insights to an EdTech company, helping them identify and prioritize international markets with the highest client potential for their services.

The analysis focuses on a period from 2010 to 2015, using key socio-economic and educational indicators to build a composite score for market attractiveness.

## Business Objectives

The analysis was designed to answer three critical business questions for the EdTech company:

1.  **Which countries have high client potential for our services?** (Identification of attractive markets)
2.  **What is the projected evolution of client potential in these countries?** (Trend analysis for strategic planning)
3.  **In which countries should the company prioritize its operations?** (Final recommendation based on composite scoring)

## Methodology

The analysis followed a structured approach to transform raw data into actionable recommendations:

1.  **Data Selection and Cleaning:** Initial loading and inspection of the EdStats dataset, focusing on the `EdStatsData` and `EdStatsCountry` tables.
2.  **Indicator Filtering:** Indicators were selected based on their relevance to EdTech market potential (e.g., enrollment, GDP per capita, internet access) and data quality (minimizing missing values).
3.  **Key Indicators Used:**
    *   `Internet users (per 100 people)` (Proxy for digital readiness)
    *   `Enrolment in secondary education, both sexes (number)` (Proxy for immediate market size)
    *   `Enrolment in tertiary education, all programmes, both sexes (number)` (Proxy for advanced market size)
    *   `GDP per capita (constant 2005 US$)` (Proxy for economic capacity and ability to pay)
4.  **Market Potential Scoring:**
    *   An **"Average Over Years"** metric (2010-2015) was calculated for each country and each selected indicator.
    *   For each indicator, the **Top 25** countries with the highest average value were identified.
    *   A final list of **Priority Countries** was established by selecting only those countries that appeared in the Top 25 list for **at least three** of the four key indicators.
5.  **Trend Analysis:** Visualization of the evolution of the key indicators for the final priority countries to assess market stability and growth.

## Key Findings and Priority Countries

Based on the composite scoring methodology, the following countries demonstrated the highest and most consistent market potential across the selected indicators:

| Rank | Country | Justification |
| :--- | :--- | :--- |
| 1 | **United States** | High enrollment numbers, strong GDP per capita, and high internet penetration. |
| 2 | **Japan** | Excellent economic capacity and high digital readiness, coupled with large tertiary enrollment. |
| 3 | **Germany** | Strong and stable economic indicators, large secondary and tertiary education systems. |
| 4 | **France** | Consistent performance across all four indicators, particularly in enrollment and GDP. |
| 5 | **United Kingdom** | High scores in economic and digital readiness, indicating a mature and accessible market. |

These five nations are recommended as the **Priority Countries** for the EdTech company's initial market entry or focused expansion efforts.

## How to Use the Notebook

### Prerequisites

To run this analysis locally, you will need:

*   Python 3.x
*   Jupyter Notebook or JupyterLab
*   The following Python libraries:
    *   `pandas`
    *   `numpy`
    *   `matplotlib`
    *   `seaborn`
*   The original World Bank EdStats dataset files (not included in this repository due to size, but required for the notebook to run).

### Running the Analysis

1.  Clone this repository:
    ```bash
    git clone https://github.com/ziram1/Educational-Systems-Data-Analysis
    ```
2.  Download the World Bank Education Statistics dataset from the official World Bank Data Catalog: https://datacatalog.worldbank.org/search/dataset/0038480/education-statistics
3.  Ensure the necessary data files (e.g., `EdStatsData.csv`, `EdStatsCountry.csv`) are placed in the correct directory structure as referenced in the notebook.
4.  Open the notebook:
    ```bash
    jupyter notebook notebook.ipynb
    ```
5.  Execute the cells sequentially to reproduce the data cleaning, analysis, scoring, and visualization steps.

