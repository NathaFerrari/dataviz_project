SUPSI 2025–26  
Data Visualization course, C-D3202E  
Teacher: Giovanni Profeta  

# Well-being evolution during crisis

Authors:  
Sasha Bravo, Nathan Ferrari, Andrea Frati, Manuel Grosso  

Project website:  
https://nathaferrari.github.io/dataviz_project/

---

## Abstract

This project provides an in-depth analysis of the evolution of well-being in European countries between 2006 and 2024, with the aim of understanding how major economic, health, and geopolitical crises have affected people’s quality of life.

Over the last two decades, Europe has experienced several historical shocks, including the 2008 global financial crisis, the sovereign debt crisis, the COVID-19 pandemic, the post-pandemic inflation surge, and the war in Ukraine. These events have put economic, social, and institutional systems under significant pressure.

To analyse these phenomena in a structured way, an Aggregate Well-Being Index was constructed by combining economic, social, and stability-related variables, offering a multidimensional perspective on well-being. Through interactive visualizations—especially maps and time series—the project highlights territorial differences, convergence and divergence dynamics, and the impact of major crises across Europe.

Special attention is devoted to Switzerland, which emerges as a particularly resilient case, showing high and stable well-being levels throughout the entire period. The comparison with the rest of Europe helps identify structural factors contributing to long-term resilience.

---

## Introduction

In recent decades, the concept of well-being has become increasingly central in economic, political, and social debates, moving beyond GDP growth as the sole indicator of a country’s progress. Quality of life, economic security, social cohesion, access to services, and institutional stability are now considered essential dimensions for understanding societal development.

Europe represents a particularly relevant context for this analysis, as it includes countries with heterogeneous welfare models, economic structures, and institutional settings. Between 2000 and 2024, the continent faced a sequence of major crises that affected countries in markedly different ways.

Within this complex scenario, this project aims to reconstruct the evolution of well-being in Europe using a comparative, data-driven approach. This is achieved through the construction of an Aggregate Well-Being Index that integrates economic, social, and stability dimensions into a single synthetic indicator.

Interactive visualizations—specifically a dynamic map with a time slider and temporal charts—allow users to explore both the geographical distribution and the temporal evolution of well-being, highlighting phases of growth, crisis, and recovery. A central focus is placed on Switzerland, which appears as a “stability haven” compared to many EU countries, offering insights into the determinants of long-term resilience.

---

## Data sources

### Main datasource

OECD – *How’s Life? / Current Well-Being* (DSD_HSL_CWB), accessed through the OECD Data Explorer.

https://data-explorer.oecd.org/vis?lc=en&df%5Bid%5D=DSD_HSL%40DF_HSL_CWB

### Data provenance

The data are produced by the OECD (Organisation for Economic Co-operation and Development) within the WISE programme (Well-Being, Inclusion, Sustainability and Equal Opportunity). The indicators are based on official statistics provided by member and partner countries, ensuring high reliability, international comparability, and regular updates.

### Motivation for the choice

The OECD dataset was selected because:

- it is explicitly designed to measure well-being beyond GDP  
- it offers long time coverage, enabling pre- and post-crisis analysis  
- it allows harmonised international comparisons  
- it includes inequality and vulnerability dimensions crucial for crisis analysis  

### Main variables

The dataset contains more than 80 indicators grouped into 11 well-being dimensions, including income and wealth, housing conditions, job security, health, education and skills, environmental quality, personal safety, life satisfaction, work-life balance, social connections, and civic engagement.

A subset of indicators was selected to build the Aggregate Well-Being Index, including disposable income, difficulty making ends meet, employment rate, long-term unemployment, life expectancy, social support, perceived safety, reading proficiency, and housing cost burden.

---

## Data pre-processing

To ensure comparability across countries and years, several pre-processing steps were applied:

- **Cleaning and filtering**: selection of European countries (including Switzerland) and observations between 2000 and 2024  
- **Handling missing values**: interpolation or forward/backward filling for limited missingness; exclusion of indicators with insufficient coverage  
- **Indicator normalisation**: rescaling all variables to a 0–1 range; reversal of negative indicators  
- **Index construction**:
  - normalised indicator scores  
  - dimension-level scores computed as weighted averages  
  - Aggregate Well-Being Index obtained by combining dimension scores  

The weighting scheme is inspired by Maslow’s hierarchy of needs, giving more importance to basic dimensions such as income security, health, and safety.

Example of initial data inspection:

```python
import pandas as pd

df = pd.read_csv("file.tsv", sep="\t")
print(df.columns)
````
