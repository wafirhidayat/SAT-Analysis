# Project 1: Standardized Test Analysis


## Project Statement

This project aims to examine trends in the participation rates of SAT from 2018 to 2021 and whether COVID-19 had a significant impact on the participation rates in the peri-COVID-19 era (2020 to 2021).

## Executive Summary

For many years, standardised test scores have been used as a benchmark for college admissions in the USA, where high school students are required to partake in a 3-hour examination based on various knowledge. However, due to the emergence of COVID-19 in [early 2020](https://pubmed.ncbi.nlm.nih.gov/32191675/), several [restrictions](https://blogs.worldbank.org/education/high-stakes-school-exams-during-covid-19-coronavirus-what-best-approach), such as postponment of examination dates, were imposed to restrict the spread of the virus which impacted the participation rates of these standardised test. 

## Datasets

Chosen CSV datasets provided for this project:
* [sat_2018.csv](https://git.generalassemb.ly/wafirhidayat/projects/blob/master/project_1/data/sat_2018.csv): 2018 SAT Scores by State ([source](https://reports.collegeboard.org/media/pdf/2020-total-group-sat-suite-assessments-annual-report.pdf))
* [sat_2019.csv](https://git.generalassemb.ly/wafirhidayat/projects/blob/master/project_1/data/sat_2019.csv): 2019 SAT Scores by State ([source](https://reports.collegeboard.org/media/2022-04/2021-total-group-sat-suite-of-assessments-annual-report%20%281%29.pdf))
* [sat_act_by_college.csv](https://git.generalassemb.ly/wafirhidayat/projects/blob/master/project_1/data/sat_2019_by_intended_college_major.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges ([source](https://www.compassprep.com/college-profiles/))

Additional CSV datasets:
* [sat_state_2020.csv](https://git.generalassemb.ly/wafirhidayat/projects/blob/master/project_1/data/sat_state_2020.csv): 2020 SAT Scores by State ([source](https://blog.prepscholar.com/what-is-the-average-sat-score))
* [sat_state_2021.csv](https://git.generalassemb.ly/wafirhidayat/projects/blob/master/project_1/data/sat_state_2021.csv): 2021 SAT Scores by State ([source](https://soflotutors.com/blog/sat-scores-by-state/))
* [United_States_COVID-19_Cases_and_Deaths_by_State_over_Time.csv](https://git.generalassemb.ly/wafirhidayat/projects/blob/master/project_1/data/United_States_COVID-19_Cases_and_Deaths_by_State_over_Time.csv): COVID-19 Cases by State over Time ([source](https://data.cdc.gov/Case-Surveillance/United-States-COVID-19-Cases-and-Deaths-by-State-o/9mfq-cb36/data))
* [participation rate by state - absolute](https://git.generalassemb.ly/wafirhidayat/projects/blob/master/project_1/data/United_States_COVID-19_Cases_and_Deaths_by_State_over_Time.csv): Absolute SAT Participation ([source](https://reports.collegeboard.org/sat-suite-program-results))

## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state_name|object|sat_df, total_cases, sat_par_abs|Name of the state in the US from which data was collected|
|state|object|sat_df, total_cases, sat_par_abs|Abbreviation of USA State|
|20xx_participation|float|sat_df|State's eligible population's participation in taking the SAT for indicated year |
|20xx_ebrw|integer|sat_df|State's average grade on the Evidence-Based Reading and Writing section of the SAT for indicated year  (Between 200-800)|
|20xx_math|integer|sat_df|State's average grade on the Math section of the SAT for indicated year  (Between 200-800)
|20xx_total_score|integer|sat_df|State's average total grade on the SAT for the indicated year (Between 400-1600)|
|submission_date|datetime|total_cases|Date of submission of COVID-19 cases|
|20xx_tot_cases|integer|total_cases|Total number of COVID-19 cases for the indicated year|
|school|object|test_req_df|Name of College/University|
|test_optional|boolean|test_req_df|Admission requirement for SAT/ACT|
|optional_in_2021|object|test_req_df|Shows if school allows SAT/ACT to be optional for admission to class of 2021|
|applies_class_year|object|test_req_df|Year of admission in which SAT is optional|
|test_takers_20xx|integer|sat_par_abs|Number of students taking SAT for the indicated year|
|num_grads_20xx|integer|sat_par_abs|Number of graduating students taking SAT for the indicated year|


## Exploratory Analysis 
After cleaning & combining our datasets, we carry out an initial exploratory analysis to identify some information markers from the data. Some trends can be observed in this step as well. 

## Data Visualisation
To further expound on the Exploratory Data Analysis, by creating various plots and graphs, it can help us visualise the data better and better find trends and correlations. Comparisons across certain factors such as time and participation can also be easily made to help make conclusions and recommendations.

## Conclusions and Recommendations
Although there is a correlation between number of COVID-19 cases and SAT Participation, with the decreased numbers seen with high COVID-19 cases, it could still not explain the drastic decrease in numbers from 2020 to 2021. Especially when studying the top 3 states that had the highest overall COVID-19 cases recorded from 2020 to 2021, it can be concluded that there may be another underlying reason.

From the data retrieved from universities requirement in SAT/ACT in their admission policies, about [93%](#Other-Factor(s)-That-Could-Affect-Participation-Rate) of the universities have made the test optional in their admission requirement. This could have contributed to the sharp decline in SAT participation in 2021, even though there was an uptick in the numbers from 2018 to 2019. Therefore, COVID-19 could be the catalyst in the decrease in participation during the peri-Covid-19 period. Furthermore, there was a higher number of COVID-19 cases recorded in 2021 which could compel students to forgo partaking in SAT/ACT test for the college/university admission, especially since most schools have made it optional as well.

Additional research shows that COVID-19 has a bigger effect on those [aged 30 and above](https://www.cdc.gov/coronavirus/2019-ncov/covid-data/investigations-discovery/hospitalization-death-by-age.html). The COVID numbers that we have may be skewed towards the higher age group resulting in no clear relationships observed.

Thus, we recommend future research should take into consideration the influence of other these other factors. Furthermore, this project is limited by the sample size, with only 3 years of study since COVID-19 is a relatively new phenomenon. Further research should be done in the following years in which COVID-19 is still prevalent, especially when the end of COVID-19 is still unknown even in an endemic period.