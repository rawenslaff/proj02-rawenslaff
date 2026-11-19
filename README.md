# Project 02 Proposal: The Value of a Bachelor's Degree

**Team members:** Rafael Wenslaff

See the [Project 02 instructions](https://data385.github.io/project/proj02_wholegame.html) for what goes in each section. Bullet points are great. Put any images in an `img/` folder.

## 1. Problem statement

College enrollment and degree attainment in the United States have increased over the past several decades. However, with this increase also comes an increase in the cost of said enrollment. This raises questions about whether a college degree provides a clear economic benefit or if the financial burden of attending college has made it more of a gamble. Through this project, I plan to analyze how the economic value of a bachelor's degree has changed over time by considering degree attainment along with major-related employment, inflation, and cost of enrollment overtime and comparing these factors against high-school graduates. My expectations are that the financial viability of obtaining a college degree will still be higher than that of solely obtaining a high-school diploma, but it will be proportionally less than it had once been following an increase in enrollment costs.

## 2. Research question

To what extent is the rising cost of attending college in the United States (predictor) associated with the financial advantage of obtaining a bachelor's degree (response) compared to high school graduates?

## 3. Data acquisition

I intended to collect data on cost of enrollment over time by downloading the data directly from the [NCES website](https://nces.ed.gov/programs/digest/d24/tables/dt24_330.10.asp). I intend to collect data on the percentage of people who have completed a high school or college degree as well as the mean earnings of workers by education attainment by downloading the data directly from the [United States Census website](https://www.census.gov/data/tables/time-series/demo/educational-attainment/cps-historical-time-series.html).

### a. Confirm viability

[NCES Data on Cost of College Enrollment from 1963-2024](https://nces.ed.gov/programs/digest/d24/tables/dt24_330.10.asp)

- **Citation:** National Center for Education Statistics. (2024). *Digest of Education Statistics, 2024, Table 330.10: Average undergraduate tuition and fees and room and board rates charged for full-time students in degree-granting postsecondary institutions, by level and control of institution: Selected academic years, 1963–64 through 2023–24.* U.S. Department of Education. https://nces.ed.gov/programs/digest/d24/tables/dt24_330.10.asp
  
- **Documentation:** https://nces.ed.gov/ipeds/survey-components/ipeds-survey-methodology
  
- **Collection Method:** Data was obtained through the Higher Education General Information Survey (HEGIS), as well as the Integrated Postsecondary Education Data System (IPEDS).

[United States Census Data on high school/college completion and earnings by education attainment](https://www.census.gov/data/tables/time-series/demo/educational-attainment/cps-historical-time-series.html)

- **Citation:** U.S. Census Bureau. (2026). *Current Population Survey historical time series tables: Table A-2, Percent of People 25 Years and Over Who Have Completed High School or College, by Race, Hispanic Origin and Sex, 1940–2025; and Table A-3, Mean Earnings of Workers 18 Years and Over, by Educational Attainment, Race, Hispanic Origin, and Sex, 1975–2024.* U.S. Department of Commerce. https://www.census.gov/data/tables/time-series/demo/educational-attainment/cps-historical-time-series.html
  
- **Documentation:** https://www2.census.gov/programs-surveys/cps/techdocs/cpsmar26.pdf
  
- **Collection Method:** Data was obtained through the Current Population Survey (CPS), a monthly survey sponsored by the Bureau of Labor Statistics and conduced by the U.S. Census Bureau involving telephone and in-person interviews.

### b. Variables of interest

- **year (numeric):** The calendar year associated with the data
- **enrollment_cost (numeric):** Average annual cost of attending college
- **enrollment_cost_constant (numeric):** Average annual cost of attending college, adjusted for inflation
- **highschool_grads (numeric):** Percentage of U.S. population aged 25+ who have completed 4 or more years of high school
- **bachelors (numeric):** Percentage of U.S. population aged 25+ who have completed 4 or more years of college
- **earnings_highschool (numeric):** Mean annual earnings of high school graduates aged 18+
- **earnings_bachelors (numeric):** Mean annual earnings of college graduates aged 18+

## 4. Data example

[Data Example with glimpse()](data_management.pdf)

## 5. EDA

- Import: using `read_xlsx()` to import data into R
- Cleaning and Wrangling: using `select()`, `rename()`, and `mutate()` to keep relevant columns, change column names, and convert values into appropriate data types
- Joining: using `left_join()` to combine datasets via year (will have to account for year vs. academic year data when cleaning)
- Calculating Variables: using `mutate()` to calculate the percentage earnings of those with bachelor's degrees vs. high school graduates
- Summarizing Data: using `group_by()` and `summarize()` to analyze changes in enrollment cost, degree attainment, and earnings over time
- Visualizing Data: using `ggplot()` to create graphs illustrating the change in financial advantage of having a bachelor's degree over time and as enrollment costs change

## 6. Modeling

_The models you plan to use, your response and predictor variables, and why the models fit your research question._
- My response variable (y) will be a calculated earnings difference for people with a bachelor's degrees compared to people who only graduated high school
- My predictor variable (x) will be enrollment costs
- I plan to use a linear regression model to analyze how enrollment costs compare to the financial advantage of obtaining a bachelor's degree and determine whether or not there is a relationship between a higher cost of enrollment and greater financial viability for those with a Bachelor's degree.

## 7. Communicate

I plan on presenting my results through a Quarto website.

## 8. LLM disclaimer

I do not plan on using LLMs.

