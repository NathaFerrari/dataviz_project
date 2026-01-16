# Dataset Metadata



##### Overview

This dataset contains normalized well-being indicators for different countries, years, and well-being domains.

Each row represents an observation for a specific country, year, and metric.



The dataset includes 6776 observations and 5 features.



##### Variables

* Reference area (string): country or geographical area name.
* TIME\_PERIOD (integer): year of observation.
* Metric (string): name of the well-being metric (normalized).
* Value (float): normalized value of the selected well-being metric
* Domain (string): well-being domain to which the metric belongs (e.g., Housing, Health, Safety, etc.)



##### Metric Descriptions



* life\_exp\_norm: normalized life expectancy at birth. Measures the average number of years a newborn is expected to live.
* diff\_ends\_norm: normalized percentage of population reporting difficulty in making ends meet. Higher values indicate greater financial difficulty.
* earnings\_norm: normalized average annual gross earnings (PPP adjusted). Measures income from employment.
* disp\_income\_norm: normalized net adjusted disposable income of households. Represents the income available for spending and saving after taxes and transfers.
* employment\_norm: normalized employment rate. Percentage of working-age population that is employed.
* long\_unemp\_norm: normalized long-term unemployment rate. Percentage of the labor force unemployed for a prolonged period.
* safe\_norm: normalized percentage of population feeling safe when walking alone at night.
* housing\_cost\_norm: normalized housing cost burden / affordability indicator. Higher values generally indicate higher housing costs relative to income.
* life\_sat\_norm: normalized average life satisfaction score (originally measured on a 0–10 scale).
* support\_norm: normalized percentage of population reporting having someone to rely on in times of need (social support).
* reading\_norm: normalized student reading performance score, measuring educational achievement.



