SUPSI 2025-26

Data Visualization course, C-D3202E

Teacher Giovanni Profeta


# Well being evolution during crisis
Authors: Sasha Bravo, Nathan Ferrari, Andrea Frati, Manuel Grosso
Project website: https://nathaferrari.github.io/dataviz_project/

​

Abstract
This project provides an in-depth analysis of the evolution of well-being in European countries between 2000 and 2024, with the goal of understanding how major economic, health, and geopolitical crises have affected people’s quality of life. Over the last two decades, Europe has experienced several historical shocks, such as the 2008 global financial crisis, the sovereign debt crisis, the COVID-19 pandemic, the strong inflation phase after the pandemic, and the war in Ukraine, all of which have put economic, social, and institutional systems under pressure.
​

To analyse these phenomena in a structured way, an Aggregate Well-Being Index was constructed by combining economic, social, and stability-related variables, in order to offer a multidimensional view of well-being. Using interactive visualizations, in particular maps and time series charts, the project highlights territorial differences between European countries, convergence and divergence dynamics over time, and the impact of historical shocks on different areas of the continent.
​

Special attention is devoted to Switzerland, which emerges as a particularly interesting case study due to its high and stable levels of well-being throughout the entire period. The comparison between Switzerland and the rest of Europe makes it possible to identify the resilience factors that characterise its economic and social system, offering a clear, accessible, and scientifically grounded reading of how well-being in Europe has changed over the last twenty-five years.
​

Introduction
In recent decades, the concept of well-being has taken on an increasingly central role in economic, political, and social debates, moving beyond GDP growth as the sole indicator of a country’s health. Factors such as quality of life, economic security, social cohesion, access to services, and institutional stability have become essential to understand the progress of contemporary societies.
​

Europe is a particularly relevant context for this type of analysis, as it brings together countries with very different levels of development, welfare models, and economic structures. Between 2000 and 2024, the continent faced a sequence of major crises: the 2008 global financial crisis, the sovereign debt crisis in Southern Europe, the COVID-19 pandemic, the post-pandemic inflation surge, and the war in Ukraine, each affecting territories in different ways.
​

Within this complex scenario, there is a need to examine how the well-being of European citizens has responded to these shocks and whether there are significant differences between the various areas of the continent. The goal of this project is to reconstruct the evolution of well-being in Europe using a comparative and data-driven approach, through the construction of an Aggregate Well-Being Index that combines economic, social, and stability dimensions into a single synthetic indicator.
​

The interactive visualizations developed in the project – in particular a dynamic map with a time slider and temporal charts – make it possible to intuitively explore both the geographical distribution of well-being and its evolution over time, highlighting phases of growth, crisis, and recovery. Users can identify territorial patterns, structural differences, and breaks associated with the main historical events.
​

A central element of the project is the focus on Switzerland, which displays high and relatively stable levels of well-being throughout the period, emerging as a kind of “stability heaven” compared to many EU countries. This comparison helps reveal which economic, institutional, and historical features contribute to long-term resilience, and how they are reflected in the trajectory of well-being captured by the data.
​

Data sources
List of datasets used
OECD – How’s Life? / Current Well-Being (DSD_HSL_CWB), accessible through the OECD Data Explorer platform.
​
Main datasource:
https://data-explorer.oecd.org/vis?lc=en&df%5Bds%5D=dsDisseminateFinalDMZ&df%5Bid%5D=DSD_HSL%40DF_HSL_CWB&df%5Bag%5D=OECD.WISE.WDP&dq=AUS%2BAUT%2BBEL%2BCAN%2BCHL%2BCOL%2BCRI%2BCZE%2BDNK%2BEST%2BFIN%2BFRA%2BDEU%2BGRC%2BHUN%2BISL%2BIRL%2BISR%2BITA%2BJPN%2BKOR%2BLVA%2BLTU%2BLUX%2BMEX%2BNLD%2BNZL%2BNOR%2BPOL%2BPRT%2BSVK%2BSVN%2BESP%2BSWE%2BTUR%2BGBR%2BUSA%2BARG%2BBRA%2BBGR%2BHRV%2BIDN%2BPER%2BROU%2BZAF%2BTHA%2BCHE...
​

Data provenance
The data are produced by the OECD (Organisation for Economic Co-operation and Development) within the WISE programme (Well-Being, Inclusion, Sustainability and Equal Opportunity), which collects official statistics provided by member and partner countries.
​
This ensures high reliability, international comparability, and regular updates, making the database suitable for longitudinal and cross-country comparisons of well-being.
​

Motivation for the choice
The OECD dataset was chosen because:

it is specifically designed to measure well-being beyond GDP, including economic, social, and quality-of-life dimensions

it offers an extended time coverage, allowing analysis of pre- and post-crisis periods (2008, 2010–2012, 2020, 2022)

it enables standardised international comparisons across European countries through harmonised indicators

it includes inequality, deprivation, and distributional measures of well-being, which are crucial to assess vulnerability to crises.
​

Main variables
The dataset contains more than 80 indicators grouped into 11 well-being dimensions, including income and wealth, housing conditions, job security, health, education and skills, environmental quality, personal safety, life satisfaction, work-life balance, social connections, and civic engagement.
​
In this project, a subset of indicators was selected to construct the Aggregate Well-Being Index, combining variables such as disposable income, difficulty making ends meet, employment rate, long-term unemployment, life expectancy, social support, perceived safety, reading proficiency, and housing cost.
​

Data pre-processing
To build a synthetic index that is comparable across countries and years, the OECD data underwent several pre-processing steps.
​

The main operations include:

Cleaning and filtering: selection of European countries (including Switzerland) and of observations between 2000 and 2024; removal of duplicated or clearly irrelevant variables with respect to the well-being dimensions defined in the project.
​

Handling missing values: for indicators with a small share of missing data, time-series techniques such as interpolation or forward/backward filling were applied; indicators with insufficient coverage were excluded from the index computation.
​

Indicator normalisation: all selected variables were rescaled to a 0–1 range, where 1 represents the best and 0 the worst condition; for “negative” indicators (e.g. long-term unemployment, difficulty making ends meet, housing cost overburden) the scale was reversed.
​

Creation of new fields:

a normalised score for each indicator

dimension-level scores (e.g. Income & wealth, Work & job quality, Housing, Health, Social connections, Safety) computed as weighted averages of their indicators

an overall Aggregate Well-Being Index for each country-year, obtained by combining the dimension scores.
​

Weighting inspired by Maslow’s hierarchy of needs: dimensions related to basic needs (e.g. minimum income, health, safety) receive higher weights than “higher-level” dimensions (e.g. life satisfaction), following psychological evidence summarised by McLeod (2025).
​

A minimal example of the initial data loading step is:

python
import pandas as pd

df = pd.read_csv("file.tsv", sep="\t")
print(df.columns)
This inspection helps identify available columns and select only those needed for index construction and subsequent visualizations.
​

Data visualizations
1. European well-being map
What it shows

An interactive map of European countries displaying the Aggregate Well-Being Index from 2000 to 2024, navigable through a time slider.
​

A colour scale where darker tones indicate higher well-being levels and lighter tones lower levels.
​

Why it matters

It reveals geographical patterns: Northern and some Central European countries tend to display higher and more persistent well-being, while Southern and Eastern Europe start from lower levels or show catching-up trajectories.
​

It highlights countries’ resilience during major shocks (2008 crisis, COVID-19, 2021–2023 inflation, war in Ukraine), making visible where drops are temporary and where vulnerabilities are more structural.
​

Internal repository link:
[Map of Europe](https://github.com/NathaFerrari/dataviz_project#1-mappa-europea-del-benessere)

2. Temporal evolution of European well-being
What it shows

A line chart representing the evolution of the average Aggregate Well-Being Index in Europe over time, computed by aggregating country-level scores.
​

The series shows how average well-being responds to key historical events, displaying both short-term drops and longer-term trends.
​

Why it matters

It makes long-run trends visible: despite shocks, many regions exhibit a gradual improvement in well-being, especially where welfare institutions are robust.
​

It helps distinguish between temporary crisis effects and structural changes by aligning turning points in the series with historical events such as the financial crisis, the pandemic, and the war in Ukraine.
​

Internal repository link:
[Temporal evolution](https://github.com/NathaFerrari/dataviz_project#2-evoluzione-temporale-del-benessere-in-europa)

3. Switzerland vs rest of Europe
What it shows

A bar or line chart comparing Switzerland’s Aggregate Well-Being Index to the European average and/or selected countries over the entire time horizon.
​

Switzerland’s trajectory appears at high levels and with limited volatility compared to most other series.
​

Why it matters

It highlights Switzerland as a positive outlier in terms of both level and stability of well-being, supporting the “stability heaven” narrative also suggested by macro indicators such as CPI, GDP per capita, unemployment, and CHF/EUR exchange rate.
​

It shows which countries are more exposed to shocks and which are more resilient, suggesting that strong institutions, high-quality public services, and social cohesion can mitigate the impact of crises on well-being.
​

Internal repository link:
[Switzerland vs Europe](https://github.com/NathaFerrari/dataviz_project#3-confronto-svizzera-vs-resto-deuropa)

Key findings
The data analysis and interactive visualizations reveal several key results about the evolution of well-being in Europe between 2000 and 2024.
​

Marked geographical differences

Northern and Central European countries consistently show higher well-being levels than many Southern and Eastern European economies, which start from lower values but often improve over time.
​

Countries such as Finland, Norway, and Switzerland rank among the highest across multiple dimensions, while some Southern and Eastern countries appear more sensitive to shocks and display larger index fluctuations.
​

Impact of historical shocks

The main crises (2008–2012, COVID-19, post-2021 inflation, war in Ukraine) leave visible marks in the index, with downturns of varying magnitude across countries.
​

The global financial crisis produces the strongest and most widespread contraction, while the pandemic generates a moderate but generalised impact; the effects of the war in Ukraine are more heterogeneous and depend on each country’s specific exposure.
​

Long-term trends

Despite shocks, many European regions show a generally upward trajectory in well-being, especially where welfare systems and labour markets are relatively robust.
​

Some countries gradually reduce internal gaps, while others exhibit stagnation or heightened vulnerability, with signs of polarisation in the most crisis-sensitive dimensions.
​

Resilience of Switzerland

Switzerland maintains a profile characterised by high levels and low volatility of the well-being index, with only mild and short-lived deviations during major crises, confirming the strength of its economic and social structure.
​

Indicators such as high income, low long-term unemployment, strong perceived safety, robust social support, and the stability of the Swiss franc contribute to cushioning the impact of shocks on well-being.
​

Patterns emerging from interactive visualizations

Maps and line charts make it easy to identify areas of recovery, zones of persistent vulnerability, and temporary divergences between countries, which can inform more targeted policies.
​

The time slider and crisis-focused views reveal that countries react differently to the same shock, suggesting that institutional, historical, and policy factors play a crucial role in shaping well-being dynamics.
​

Overall, the analysis confirms that European well-being results from the interaction between long-term structural factors and specific historical shocks, with Switzerland standing out as a resilient case from which important lessons for well-being-oriented policies can be drawn.
​

Next steps
Several extensions are planned to further develop the project.
​

Include countries directly involved in the Ukraine war
Collecting consistent data for Russia and Ukraine would allow the construction of a comparable well-being index and enable direct analysis of the conflict’s impact on the populations involved, beyond the indirect effects currently visible in other European countries.
​

Deepen the analysis of internal inequalities
Using the distributional dimensions of the OECD data (gender, age, education) would make it possible to study how crises affect specific groups within the same country, enriching the aggregate picture given by the overall index.
​

Expand interactive visualizations
Adding comparative views for clusters of countries (euro area, Nordics, Eastern Europe) and more advanced filtering tools would allow users to build custom comparisons across countries, well-being dimensions, and historical periods.
​

Link to policy and scenario analysis
Connecting the evolution of the index with specific public policies (e.g. anti-crisis measures, income support, labour market policies) could help identify which interventions are most effective in protecting well-being during shocks.
​

These developments would turn the project into an even more valuable tool for understanding and communicating well-being dynamics in Europe in a context of recurring crises.
