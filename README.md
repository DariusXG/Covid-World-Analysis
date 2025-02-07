# COVID-19 SQL Analysis & Visualization Project

This project showcases my ability to use SQL for advanced data analysis by exploring COVID-19 datasets. I used a series of SQL queries to extract insights from COVID-19 case, death, and vaccination data. The results from these queries were then used to create interactive visualizations in Tableau, which are attached to this repository.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [SQL Analysis Details](#sql-analysis-details)
  - [Data Retrieval](#data-retrieval)
  - [Death and Infection Rates](#death-and-infection-rates)
  - [Global and Continental Aggregations](#global-and-continental-aggregations)
  - [Vaccination Analysis](#vaccination-analysis)
  - [Views and Temporary Tables](#views-and-temporary-tables)
- [Tableau Visualizations](#tableau-visualizations)
- [Technologies Used](#technologies-used)
- [How to Run the Project](#how-to-run-the-project)
- [Conclusion](#conclusion)

---

## Project Overview

This project analyzes COVID-19 data stored in a SQL Server database named `PortfolioProject`. It covers several key areas:

- **Basic Data Retrieval:** Fetching complete datasets with necessary filters.
- **Death and Infection Rates:** Comparing total cases to deaths and analyzing infection rates relative to population.
- **Global & Continental Trends:** Aggregating data to provide insights at a global and continental level.
- **Vaccination Rollout:** Calculating rolling totals and percentages of vaccinations relative to population using window functions, CTEs, and temporary tables.
- **Visualization Preparation:** Creating a SQL view for streamlined data access when building Tableau dashboards.

---

## Data Sources

The project uses data from two primary tables:

- **CovidDeaths:** Contains daily records on COVID-19 cases, deaths, and population data.
- **CovidVaccinations:** Contains daily records on new vaccinations.

Both tables are part of the `PortfolioProject` database.

---

## SQL Analysis Details

### Data Retrieval

- **Basic Data Query:**  
  ```sql
  SELECT * 
  FROM PortfolioProject..CovidDeaths
  WHERE continent IS NOT NULL
  ORDER BY 3, 4;
