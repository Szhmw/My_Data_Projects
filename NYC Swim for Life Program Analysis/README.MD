# NYC Swim for Life Program Analysis

A dashboard to monitor Swim for Life program offered in New York City and a data story to advocate for affordable swimming education. Interactive Tableau dashboard can be found [here](https://public.tableau.com/shared/6GR6ZR3MQ?:display_count=n&:origin=viz_share_link).

### Background
#
According to CDC (Centers for Disease Control and Prevention), drowning is the second leading cause of unintentional injury death among children aged 5-14, after motor vehicle crashes. [Source](https://www.cdc.gov/drowning/data-research/facts/?CDC_AAref_Val=https://www.cdc.gov/drowning/facts/index.html)

In 2023, NYC Council passed bills requiring the Department of Parks and Recreation to provide free swimming lessons and water safety instruction to NYC public school second graders. [Source](https://legistar.council.nyc.gov/LegislationDetail.aspx?ID=5871055&GUID=BDDE92D1-845D-44FB-ABD0-93F64E8D1832&Options=ID%7CText%7C&Search=swim+lessons)

However, due to budget cuts, NYC could only offer 2,000 students to participate in the free program even with private funding in 2024. [Source](https://www.nytimes.com/2024/01/15/nyregion/swim-lessons-children-nyc.html)

**_Swim for Life_**, offered by NYC Parks, has been in place even before the new bills. The public dataset contains attendance information from 2016 to 2021.

**More details about the program:**
- Three 10-week sessions per year (October through June). 
- Second grade students come as a class one hour per week. 
- Classes are held 5 days per week during the hours of 10a.m.-1p.m.
- It previously cost $100 per child.

[Information about Swim for Life Program](https://www.nycgovparks.org/opportunities/support/swim-for-life)

### Dashboard:
#

![Alt text](https://github.com/Szhmw/My_Data_Projects/blob/6da5034f8a3292cacf5716a4fe6dc5268cf03688/NYC%20Swim%20for%20Life%20Program%20Analysis/dashboard.png)

### Key Metrics and Dimensions:
#
- **Number of Sessions Attended:** How many sessions a student completed.
- **Attended or Not:** If the session is attended or not.
- **Attendance Rate:** The percentage of students signed up who actually attended the trainings.
- **Enrollment Number:** The number of students who enrolled in the program.
- **Training Site Geo Location:** The Geo info of the training site across NYC.
- **Gender:** Female, Male, Unknown.
- **School Year:** 2016-2017 to 2021-2022.
- **Borough:** Manhattan, Brooklyn, Bronx, Queens.
- **School:** The participating schools in NYC.

### Conclusions:
#

- Attendance: Close to 16,000 students enrolled in the program. On average 91% of them attended at least one session. 

- Gender comparison: The total signup numbers, total sessions attendance, and attendance rates are pretty balanced among genders.

- Borough comparison: Although there are more training sites in Manhattan, students attended more sessions at the training sites in Queens. 
    To improve attendance, it's worth investigating factors like pool facilities and staff training across different training sites.

    It could also indicate a gap among students in different boroughs in terms of swimming ability. This disparity could be due to socioeconomic factors. Students and parents with fewer resources might be more motivated to participate in the program to bridge learning gaps.

- Pool use: Swim for Life takes place mostly in public park pools along with a few other partners. There's only a small portion of public pools that are available in the progrom. Might consider expanding the program to include more public pools and offering weekend classes could increase accessibility.

### Future Research ideas:
#

- Get more info about attendees' pre and post program swimming ability comparison to better measure the quality of the program.

- According to NYC Youth Risk Behavior Survey from 2017, there's a huge gap in race when it comes to swimming ability. The report should include more details on race. [NYC Youth Risk Behavior Survey](https://a816-health.nyc.gov/hdi/epiquery/visualizations?PageType=ts&PopulationSource=YRBS&Topic=5&Subtopic=35&DisplayViz=Main&MainDashboard=View%20Indicator%20Quick%20Look&MainCustomView=https%3A%2F%2Fa816-healthtableau.nyc.gov%2Ft%2FHDI-EPIQUERY%2Fviews%2FHDISurveyModules_YRBS%2FViewIndicatorQuickLook%2FHDI_Publicprdsvc%2Fcv1658417047751PS&SAIDashboard=See%20Available%20Indicators&SAICustomView=https%3A%2F%2Fa816-healthtableau.nyc.gov%2Ft%2FHDI-EPIQUERY%2Fviews%2FHDISurveyModules_YRBS_SAIOnly%2FSeeAvailableIndicators%2FHDI_Publicprdsvc%2Fcv1658417047751SAIPS)

### Data Sources and Notes:
#
1. [**Swim for Life**](https://data.cityofnewyork.us/Recreation/Swim-for-Life/mtt6-ywt4/about_data)
from NYC OpenData, lasted updated: November 29, 2022

      _Notes:_
          - The program was not offered in 2022
          - Gender column has some unknown values
          - [Data cleaning change log link](https://github.com/Szhmw/My_Data_Projects/blob/81d2baa9b6ce123447d6b5c4e5ffe54d3b7c23ab/NYC%20Swim%20for%20Life%20Program%20Analysis/Change%20Log.md)

2. [**NYC Parks Pools**](https://data.cityofnewyork.us/Recreation/NYC-Parks-Pools/y5rm-wagw/about_data)
from NYC OpenData, lasted updated: May 1, 2024

