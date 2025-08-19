# Analyzing U.S. COVID-19 Data


## Analytical Components

### 1. Exploratory Data Analysis (EDA)

The EDA examines:
- Temporal variation in COVID-19 hospitalizations and deaths
- Demographic distributions of cases, hospitalizations, and mortalities by sex, race, age, and state
- Hospitalization and mortality rates across different states and demographic subgroups
- Association between ICU admissions, age, and comorbidity prevalence
- Distribution and impact of expected employment loss and delayed medical treatment, stratified by employment sector and household income

**Key Results:**
- Hospitalizations peaked in January 2021
- Males experienced higher mortality rates than females
- Over 90% of deaths occurred in individuals aged 65 and above
- Substantial interstate variation in hospitalization and death rates, with Virginia among the highest
- ICU admission and mortality rates increased strongly with age and the presence of underlying health conditions

### 2. Statistical Hypothesis Testing

Two primary research hypotheses were investigated:
- **Association between patient demographic factors and COVID-19 mortality:** Evaluated using logistic regression, with significant associations found for sex, race, and ethnicity at the alpha = 0.05 level, though not all variables reached significance.
- **Association between underlying medical conditions and mortality:** Addressed using the Chi-square test of independence, with the null hypothesis strongly rejected (p-value ≪ 0.05), confirming a robust relationship.

### 3. Regression and Machine Learning Modeling

- **Ordinary Least Squares (OLS) Regression**: Modeled death as a function of multiple demographic and clinical predictors.
  - Model  R^2 ranged from 0.689 to 0.82 after introducing higher-order terms and controlling for outliers
  - Significant predictors included sex, certain age groups, and ICU admission status
- **Random Forest Classifier**: Implemented for mortality prediction, achieving approximately 97% classification accuracy, with notably high precision for survival prediction

### 4. Targeted Epidemiological and Socioeconomic Questions

This section extends the analysis to answer focused questions, including:
- The influence of exposure, symptom status, and comorbidities on hospitalization and death
- Impact of the pandemic on employment loss and stimulus payments across the states
- Correlation of household income with delays in medical treatment
- Temporal and seasonal patterns in case identification and clinical processes

## Principal Findings and Implications

- **Age** is the dominant determinant of mortality and severity
- **Male sex** and certain races/ethnicities are associated with worse outcomes
- **Presence of comorbidities** is a significant risk factor for severe disease and death
- **Geographic and socioeconomic disparities** are evident in outcomes and health system impact
- **Delayed or forgone medical care** disproportionately affects lower-income groups, compounding risks during the pandemic

These insights have direct relevance for public health planning, healthcare resource allocation, policy formulation, and the design of future epidemiological monitoring systems.

## Data Sources

- COVID-19 Case Surveillance Public Use Data (CDC, United States)
- U.S. Census Bureau Household Pulse Survey

**Time Frame Analyzed:** March 2020 to January 2022
