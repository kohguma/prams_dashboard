# PRAMS Multivitamin Intake Dashboard

> Graph and table of maternal characteristics and the trends of multivitamin intake among pregnant women

During my ORISE fellowship with the CDC, I was the primary data analyst for the PRAMS project. PRAMS, also known as [Pregnancy Risk Assessment Monitoring System](https://www.cdc.gov/prams/php/methodology/index.html), is an annual population-based surveillance system that surveys a random sample of pregnant women picked from all the live birth certificates available. Currently there are 9 phases ranging from years 1988 to current, while this specific project consisted of the datasets from phase 8 (2017 - 2022), containing observations from states:"AL", "CO", "DE", "KS", "ME", "MA", "MI", "MO", "MT","NJ", "NM", "YC", "ND", "PA", "PR", "SD", "UT", "VT","VA", "WA", "WI", "WY" and 249970 observations with 486 variables.

Extensive research for over 30 years show that daily intake of 400mcgs of Folic Acid can help prevent birth defects. Our objective for this project was to examine state-level proportions and associations of exposures that could potentially impact adverse birth outcomes. Specific exposures include: prepregnancy diabetes, vitamin intake (folic acid, multivitamin, prenatal), substance use, obesity, smoking, race/ethnicity, SES (income, education), maternal age, and geographic area of resident.

## Methods

The Phase 8 surveys were distributed through a telephone/mail methodology consisting of either a telephone interview, and/or questionnaire packet. These surveys were sent out to the chosen women (randomly selected from recent birth certificates) in batches every month, 2-4 months after their birth and were asked to answer questions about preconception, prenatal, and postpartum care; obstetric history; maternal substance use; physical abuse; contraception; economic status; maternal stressors; and early infant development and health status.

The dataset itself is weighted by each site rather than entirely as a whole. For all our analysis we used R and SAS for comparison. First we found the weighted and unweighted proportion(%) of each exposure of interest stratified by year and created a descriptive table to summarize the findings. Then to measure the associations, we found the crude OR's with Vitamin No-intake as reference and used chi-square test statistics to select the variables/exposures of interest we would fit into our adjusted OR model. For our regression model, we utilized a survey-weighted multinomial regression to see if there may be a relationship between Vitamin intake and different exposure variables such as `BMI`, `PREGNANCY_INTENT`, `EDUCATION`, `RACE/ETHNICITY`, `SMOKING`, `DRINKING`, and `DEPRESSION`.

## Importance of project

This dashboard provides critical insight into trends in multivitamin intake among women across U.S. states from 2017 to 2022, revealing persistent low intake and identifying regions with improving habits. By combining intake trends with demographic and behavioral characteristics, this tool helps public health professionals identify key populations for targeted nutritional interventions and education.
