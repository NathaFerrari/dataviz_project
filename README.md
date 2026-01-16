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

[https://data-explorer.oecd.org/vis?lc=en&df%5Bid%5D=DSD_HSL%40DF_HSL_CWB](https://data-explorer.oecd.org/vis?lc=en&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_HSL%40DF_HSL_CWB&df[ag]=OECD.WISE.WDP&dq=AUS%2BAUT%2BBEL%2BCAN%2BCHL%2BCOL%2BCRI%2BCZE%2BDNK%2BEST%2BFIN%2BFRA%2BDEU%2BGRC%2BHUN%2BISL%2BIRL%2BISR%2BITA%2BJPN%2BKOR%2BLVA%2BLTU%2BLUX%2BMEX%2BNLD%2BNZL%2BNOR%2BPOL%2BPRT%2BSVK%2BSVN%2BESP%2BSWE%2BTUR%2BGBR%2BUSA%2BARG%2BBRA%2BBGR%2BHRV%2BIDN%2BPER%2BROU%2BZAF%2BTHA%2BCHE.1_1%2B1_5%2B2_3%2B5_1%2B5_4%2B6_1%2B7_1%2B6_5%2B2_1%2B2_8%2B3_2%2B7_4%2B8_1%2B10_2%2B11_1.Y%2BUSD_PPP%2BUSD_PPP_PS%2BPT_POP_Y_GE15%2BPT_POP_Y_GE16%2BPT_POP_Y16T65%2BPT_POP_Y25T64%2BPT_LF%2BPT_B7G_S14%2B0_TO_10%2BPO._T._T._T.HSL_1%2BHSL_2%2BHSL_3%2BHSL_4%2BHSL_5%2BHSL_6%2BHSL_7%2BHSL_8%2BHSL_9%2BHSL_10%2BHSL_11&pd=2004%2C2025&to[TIME_PERIOD]=false&vw=ov&lb=nm
)

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
## Data visualizations

### European well-being map
**What it shows**  
An interactive map displaying the Aggregate Well-Being Index for European countries from 2006 to 2022, navigable via a time slider. Countries are color-coded from blue (higher well-being) to lighter shades (lower well-being).

**Why it matters**  
The map reveals clear geographical patterns showing how Scandinavia and Central Europe maintain the highest well-being scores, while the Balkans and Eastern Europe show lower scores but the greatest improvements. It highlights how different regions respond to major shocks, with visible drops in well-being during 2009–2010, 2019–2020, and 2021–2022, distinguishing between temporary drops and structural vulnerabilities like Greece's prolonged crisis.

---

### Radial chart of well-being indicators per country
**What it shows**  
An interactive radial (spider) chart displaying 10 normalized well-being indicators (life expectancy, housing affordability, difficulty making ends meet, disposable income, reading skills, feeling safe, social support, gross earnings, employment rate, long-term unemployment) for each European country from 2006 to 2024. Indicators are color-coded by their position in Maslow's hierarchy of needs.

**Why it matters**  
This visualization allows granular analysis of which specific well-being dimensions are affected during each crisis. It reveals patterns such as France's housing cost drop after 2008, Greece's multi-dimensional collapse, COVID-19's impact on life expectancy in Austria and Italy, and the subtle effects of the Ukraine war on housing costs and energy prices across Europe.

---

### Switzerland dynamic indexes plot
**What it shows**  
A multi-line time series chart showing the evolution of all 11 well-being indicators for Switzerland from 2006 to 2024, with each metric displayed as a separate line.

**Why it matters**  
This visualization demonstrates Switzerland's remarkable stability compared to other European countries, with only mild deviations during crisis periods. It highlights unique patterns like the counter-intuitive behavior of long-term unemployment (dropping during crises due to the Kurzarbeit short-time work scheme), the COVID-19 impact on gross earnings and life expectancy, and the overall resilience of Swiss social and economic indicators.

---

### CPI Switzerland vs EU comparison
**What it shows**  
An animated bar chart race comparing the Consumer Price Index (CPI) between Switzerland and European countries over time, showing Switzerland consistently maintaining lower inflation rates than the EU average.

**Why it matters**  
This demonstrates one of the key economic foundations of Switzerland's stability—consistent price stability that preserves purchasing power and contributes to overall well-being, even during crisis periods when other European countries experience higher inflation.

---

### GDP per capita Switzerland vs EU comparison
**What it shows**  
An animated bar chart race displaying GDP per capita for Switzerland compared to European countries over time, showing Switzerland's significantly higher economic output per person.

**Why it matters**  
This visualization reveals the strong economic foundation underlying Switzerland's well-being stability. The higher GDP per capita provides resources for robust social services, infrastructure, and quality of life, enabling better crisis resilience.

---

### Unemployment rate Switzerland vs EU comparison
**What it shows**  
An animated line chart comparing unemployment rates between Switzerland and the European average over time, showing Switzerland's consistently lower unemployment rate.

**Why it matters**  
Low unemployment is crucial for well-being as it ensures stable income and employment opportunities. Switzerland's persistently low unemployment rate demonstrates labor market resilience that contributes to maintaining well-being during economic downturns.

---

### CHF/EUR exchange rate
**What it shows**  
A line chart showing the Swiss Franc to Euro exchange rate over time, demonstrating how the CHF strengthens relative to the EUR during crisis periods.

**Why it matters**  
This visualization illustrates Switzerland's role as a safe-haven economy. The strengthening of the Swiss franc during crises reflects international trust and capital flows into Switzerland during periods of instability, reinforcing its economic stability and explaining why Swiss well-being remains resilient when other countries struggle.

---

### Crisis comparison map
**What it shows**  
An interactive choropleth map with a dropdown menu allowing users to select between three crises (2008 Financial Crisis, COVID-19, Ukraine War). The map displays the change in well-being index during each crisis period, with red indicating regression and blue indicating improvement.

**Why it matters**  
This visualization enables direct comparison of how different types of crises affect European well-being differently. It shows that the 2008 financial crisis had the most significant and widespread negative impact (especially on Spain, Greece, Ireland, Italy, and Portugal), COVID-19 had lighter but more uniform effects, and the Ukraine war produced highly diverse outcomes tied to each nation's specific circumstances and resource dependencies.

## Next steps
To proceed with the project, it would be interesting to complete the analysis of the war in Ukraine. This would require finding data covering both Russia and Ukraine, from which it would be possible to create a well-being index comparable to the one developed using our data.
