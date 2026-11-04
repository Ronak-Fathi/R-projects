
# Mental Health Trends and Demographic Disparities During and After the COVID-19 Pandemic

## Project Overview

This project examines how symptoms consistent with anxiety and depression changed among U.S. adults between April 2020 and September 2024, with particular attention to differences across age and racial/ethnic groups.

Using publicly available estimates from the **U.S. Census Bureau Household Pulse Survey**, disseminated by the National Center for Health Statistics (NCHS), the analysis investigates whether demographic disparities in mental health symptoms changed over time, rather than simply describing overall pandemic-era trends.

The primary outcome is the percentage of adults reporting symptoms of anxiety or depressive disorders. Anxiety and depressive symptoms are also examined separately as secondary outcomes.

## Research Questions

1. How did the prevalence of anxiety or depressive symptoms evolve among U.S. adults between 2020 and 2024?
2. How did differences in symptom prevalence across age groups change over this period?
3. How did differences across racial and ethnic groups evolve?
4. Were the observed disparity patterns approximately linear, nonlinear, or potentially characterized by changes in level or trend?
5. Were the main conclusions robust to alternative reference groups, outcome definitions, and modelling approaches?

## Data

The analysis uses repeated cross-sectional estimates from the Household Pulse Survey, covering April 2020 to September 2024.

The dataset includes:
- Estimates of anxiety disorder symptoms.
- Estimates of depressive disorder symptoms.
- Estimates of combined anxiety or depressive disorder symptoms.
- Demographic breakdowns, including age and race/Hispanic ethnicity.
- Survey-period dates and published confidence intervals.

The study uses published aggregate estimates rather than individual-level respondent records. Consequently, the analysis focuses on population-level patterns and does not examine individual changes over time.

## Statistical Methods

The analysis follows a structured approach, combining descriptive analysis, disparity measurement, and statistical model comparison.

**1. Data preparation and assessment**
- Data cleaning, date parsing, and consistency checks.
- Examination of missing estimates, survey-period coverage, and subgroup completeness.
- Assessment of the temporal structure and irregular spacing of survey observations.

**2. Descriptive analysis**
- Visualization of national trends in combined anxiety and depressive symptoms.
- Separate examination of anxiety and depressive symptoms.
- Comparison of temporal patterns across age and racial/ethnic groups.

**3. Disparity measurement**

For each demographic group, disparities are measured relative to a reference group using two complementary measures:

- **Absolute disparity:** difference in prevalence, expressed in percentage points.
- **Relative disparity:** prevalence ratio between the group and its reference group.

The provisional reference groups are adults aged 60–69 years and non-Hispanic White adults.

**4. Statistical modelling and model comparison**

Several candidate approaches are considered for modelling changes in disparity over time:

- Linear regression to assess average linear trends.
- Generalized additive models (GAMs) to capture potentially nonlinear temporal patterns.
- Interrupted time-series models, conditional on identifying a defensible survey-related or methodological break point.
- GAMs with continuous-time correlation structures to account for temporal dependence where supported by diagnostics.

Model selection considers goodness of fit, residual diagnostics, temporal dependence, interpretability, and model complexity rather than relying on statistical significance alone.

**5. Robustness and sensitivity analyses**
- Alternative reference groups.
- Absolute versus relative disparity measures.
- Separate anxiety and depressive symptom outcomes.
- Alternative modelling specifications.
- Assessment of subgroup coverage and estimate precision.

## Interpretation and Limitations

This is an observational analysis of repeated cross-sectional, published survey estimates. It does not establish causal relationships between the pandemic, public-health policies, and mental health outcomes.

Reported symptoms are not equivalent to clinical diagnoses. In addition, the published subgroup estimates do not provide all the information needed to calculate design-based uncertainty for differences between groups. In particular, covariance between subgroup estimates may be unavailable.

Survey design and methodological changes across collection periods also require careful assessment before interpreting long-term trends as directly comparable.

## Tools

- **R:** data preparation, statistical analysis, modelling, and visualization.
- **tidyverse:** data manipulation and visualization.
- **mgcv:** generalized additive models.
- **nlme:** temporal correlation structures and mixed modelling.
- **lubridate:** date handling.
- **knitr:** reproducible reporting.

## Project Status

The project is undergoing statistical analysis and methodological refinement. Model comparison, diagnostic assessment, and sensitivity analyses are being used to determine which conclusions are adequately supported by the data.

## Data Source

U.S. Census Bureau, Household Pulse Survey, with estimates disseminated by the National Center for Health Statistics (NCHS).

The dataset is publicly available through the [CDC/NCHS Household Pulse Survey](https://www.cdc.gov/nchs/covid19/pulse/).




