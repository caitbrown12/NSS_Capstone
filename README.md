# Public K-12 School its Effect on the Funding Landscape
Capstone project - Nashville Software School Data Analytics cohort DA6.
## Contents
* [Motivation](#Motivation)
* [Data Sources & Tools](#Data-Sources-&-Tools)
* [Process](#Process)
* [Challenges](#Challenges)
* [Conclusions](#Conclusions)
* [Use Cases](#Use-Cases)
* [Credits](#Credits)

## Motivation
The entirety of my career has been focused on supporting K-12 education. First as a member of the education team at a children’s museum and most recently as a CatchOn Senior Customer Success Manager at [Education Networks of America](https://www.ena.com/) (ENA). [CatchOn](https://www.lightspeedsystems.com/solutions/lightspeed-analytics/) is a learning analytics platform that is designed to help district leaders make data-driven decisions regarding technology adoption, support, and integration into the classroom. Many of my customers cite the necessity of Return on Investment metrics as a primary reason for using CatchOn. School districts are no stranger to budget cuts, but significant enrollment declines brought about by COVID-19 have the potential to irrevocably change the way that public school districts operate due to the potential amount of funding that will be lost alongside these declines. My goal with this project was to understand where enrollment changes are occurring most drastically and follow the potential impact that has on a district’s budget. Given my role in EdTech, my perspective for this project has been through a vendor's point of view.

If you're interested in reading more about enrollment changes related to COVID-19, I'd like to recommend the following articles as a starting point:
* [Headcounts are down at public schools. Now budgets are too.](https://apnews.com/article/covid-health-business-race-and-ethnicity-oakland-5d8956fa47149651dc09c506627c8bab)
* ['Those Kids Did Not Come Back': Exclusive Enrollment Data Shows Students Continue to Flee Urban Districts as Boom Town Schools and Virtual Academies Thrive](https://www.the74million.org/article/covid-school-enrollment-students-move-away-from-urban-districts-virtual/)
* [New Federal Data Confirms Pandemic's Blow to K-12 Enrollment, With Drop of 1.5 Million Students; Pre-K Experiences 22 Percent Decline](https://www.the74million.org/article/public-school-enrollment-down-3-percent-worst-century/)
* [As the Pandemic Set In, Charter SChools Saw Their Highest Enrollment Growth Since 2015, 42-State Analysis Shows](https://www.the74million.org/as-the-pandemic-set-in-charter-schools-saw-their-highest-enrollment-growth-since-2015-42-state-analysis-shows/)

Back to [contents](#Contents)

## Data Sources & Tools
### Data Sources
* Education Commission of the States (ECS)
    * [K-12 and Special Education Funding 2021](https://reports.ecs.org/comparisons/k-12-and-special-education-funding-2021)
* National Center for Education Statistics (NCES)
    * [Elementary/Secondary Information System](https://nces.ed.gov/ccd/elsi/)
### Tools
* Python
* Jupyter Notebooks
* Power BI

Back to [contents](#Contents)

## Process
For my data analysis, I started by evaluating the enrollment data and details provided by NCES, the Universal Services Administrative Company (USAC), and the US Census. After looking at the available years and differing levels of granularity, I determined that NCES would provide the information to best suit my needs. I then used the ElSi tool from NCES to build 8 identical tables providing information about enrollments for school years between 2013-2014 and 2020-2021. Years in my project are in reference to the year of the fall semester.

I used pd.read_html to webscrape the 50-State Comparison of state funding details provided by the ECS to analyze the different funding models used by each state. 

I decided to filter the NCES data to focus on Agency Type 1 - a designation reserved for "regular school district not part of a supervisory union" in order to make sure I was comparing districts that were most alike. I also focused primarily on states that have a base amount of funding per student as that was the most straightforward path to illustrate the relationship between enrollment and state-based funding.

Back to [contents](#Contents)

## Challenges
My biggest challenge was creating a for loop designed to calculate enrollment changes year over year per school district. The difficulty of this task was exacerbated by several components including an inconsistent number of years in operation for all districts and the fact that several school districts in different states all have the same name.

Back to [contents](#Contents)

## Conclusions
For states that use a base funding amount, enrollment can be a great indicator of changes in purchase power in future budget cycles. From a vendor point of view, knowing that these changes are coming can help a sales representative identify appropriate products or licensing quantities to best meet a district's needs with respect to their budgeting constraints. From a district's perspective, staying abreast of upcoming budget changes can help inform conversations with vendors and guide current purchasing decisions. 

While base funding amounts are a great starting place, they represent just one piece of the complex matrix that makes up K-12 funding. In light of the difficulties that COVID-19 has caused for education, several states have enacted hold harmless clauses in response to enrollment decreases - though not all of them are likely to remain in effect long-term. It is also important to consider the other factors that affect funding, especially those driven by a district's locale and student demographics factors. 

While enrollment data should not be an EdTech vendor's lone sales enablement strategy, it is a strong starting point and does provide relevant and actionable information. 

Back to [contents](#Contents)

## Use Cases

I created this [conceptual dashboard](https://app.powerbi.com/groups/me/reports/628ebe50-8199-4c6d-8ce1-8cfd177cfba7/ReportSection920f2b3bcb75ba7040e8) to show how enrollment and financial changes would be just two parts of a comprehensive sales enablement resource. Read below to see how sales professionals and sales operations teams would use a resource like this one.

### Sales Professionals
A sales professional has recently transitioned to a new territory at work and is not yet familiar with many of the school districts or regional leaders that she'll be working with. She does know that her company's newest managed cybersecurity service is a great resource for districts with fewer than 10,000 as most district's of that size have a relatively small technology team. Using the sales enablement dashboard, she can quickly filter for states in her territory and then assess individual district size to see which schools may be the optimal candidates for this new service. 

### Sales Operations
The sales operations team recently met and determined their top two goals for the coming year - increasing cross-functional collaboration and using sales data to drive their decisions. They have decided to centralize their efforts around the sales enablement dashboard as it will provide the majority of the information they need in one space. They will focus on the location of a school district, its size, and the number of support tickets submitted in the last quarter. By focusing on these metrics, they are hoping to identify correlations between types of support cases as they relate to a school's geographic location or size and will share this data with the support and networking teams.

Back to [contents](#Contents)

## Credits
I would also like to thank several people for their contributions to this project. 
* **Wade Sims**, Senior BI Engineer at ENA - Thank you for being a great sounding board and encourager in the early days of this project and for your insight into the many ways that school enrollment data is collected.
* **Amanda Partlow**, **Teresa Whitesell**, and **Taryn Patterson**, DA6 Instructors at Nashville Software School - Your motivational talks and guidance have not gone unnoticed. Thank you for providing insight and assistance at various points in this project.
* **ENA Leadership** - Thank you for supporting my desire to upskill and take a deeper dive into the world of data analytics.

Back to [contents](#Contents)
