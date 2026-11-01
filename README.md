# Ebola Outbreak Analysis in Sierra Leone | R

## View Ebola Analysis
[View the HTML Analysis Report]([Ebola_Analysis.html](https://github.com/chrisnkanta/Ebola-Analysis/blob/main/Ebola_Analysis.html])


## Project Overview

This project explores reported Ebola virus disease (EVD) cases in Sierra Leone using R. It examines case classification, demographic characteristics (age and sex), and the geographical distribution of reported cases across districts.

The goal is to demonstrate a practical data analysis workflow: importing data, assessing data quality, preparing variables, conducting exploratory data analysis (EDA), and communicating findings through tables and visualizations.

## Project Objectives

- Examine reported cases by case status, age group, and sex.
- Compare confirmed case counts across demographic groups.
- Explore how reported case counts vary by district.
- Assess data quality, including missing values and duplicate records.
- Communicate descriptive findings using tables and charts.

## Dataset

The analysis expects a CSV file at `data/ebola_sierra_leone.csv` with these fields:

| Variable | Description |
|---|---|
| `status` | Case classification, such as confirmed or suspected |
| `age` | Recorded age |
| `sex` | Recorded sex |
| `district` | District associated with the record |

Add the dataset to the `data/` folder before running the analysis. Confirm the source, definitions, and permitted use of the data before publishing it.

## Tools & Technologies

- R
- Tidyverse (`readr`, `dplyr`, `ggplot2`)
- janitor
- inspectdf
- knitr
- flextable
- here

## Analysis Workflow

1. Import the CSV dataset using `readr` and `here`.
2. Inspect key variables for missing values.
3. Check for exact duplicate rows and create a de-duplicated analysis dataset.
4. Standardize case-status and sex values for consistent grouping.
5. Create age categories: Child (under 18), Young Adult (18–29), and Adult (30 or older).
6. Summarize case status, confirmed cases by sex, confirmed cases by age group and sex, and case counts by district.
7. Visualize demographic and district-level counts.

## Key Questions

- How are records distributed across confirmed and suspected case classifications?
- How many confirmed records are recorded for each sex?
- How are confirmed case counts distributed across the defined age groups?
- How do reported case counts vary across districts?
- How complete are the key fields, and are exact duplicate rows present?

## Interpretation & Limitations

This is a descriptive analysis of records in the supplied dataset. Counts are not the same as population-based rates or individual infection risk. Comparisons between groups should be interpreted cautiously because population denominators, reporting completeness, testing access, and other epidemiological context may not be available.

The analysis does not establish causes of infection or explain differences between demographic groups. Further work using reliable population estimates, dates, and additional epidemiological variables would be needed to investigate rates and outbreak trends.

## Run the Project

1. Open `Ebola_Analysis.Rmd` in RStudio.
2. Place `ebola_sierra_leone.csv` in the `data/` folder.
3. Install the required packages if they are not already installed.
4. Knit the R Markdown file to HTML.

The knitted output will generate an updated `Ebola_Analysis.html` report with tables and charts based on the dataset.

## Repository Structure

```text
Ebola_Analysis/
├── README.md
├── Ebola_Analysis.Rmd
├── Ebola_Analysis.html
├── data/
│   └── ebola_sierra_leone.csv
└── images/
```

## Skills Demonstrated

- Data importing and preparation
- Data quality assessment
- Exploratory data analysis (EDA)
- Descriptive statistics and frequency analysis
- Demographic and geographical analysis
- Data visualization
- R programming
- Analytical communication
