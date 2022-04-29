# Kickstarting with Excel

## Overview of Project

Louise is a playwright that is using Kickstarters to fund her theater projects. Using data pulled from the Kickstarter crowd-funding website, I provided advise to Louise on how to launch a Kickstarter for the highest chance of success. Following her Kickstarter, Louise was curious how different campaigns fared in relation to their launch dates and their funding goals.

### Purpose

The purpose of the first part of the project is to identify trends in Kickstarter outcome (success, canceled, or failed) compared to launch date. The purpose of the second part of the project is to identify trends in Kickstarter outcome (success, canceled, or failed) compared to the initial Kickstarter goal.

## Analysis and Challenges

### Part 1: Analysis of Outcomes Based on Launch Date

Theater Kickstarter Outcomes (successful/ failed/ canceled) versus Kickstarter Launch Date

![Theater Outcomes vs Launch](https://github.com/cewarkentin/kickstarter-analysis/blob/main/Theater%20Outcomes%20vs%20Launch.png)

The visual above was created using a Pivot Chart and Pivot Table. The data was filtered slightly to imitate Louise's projects; the provided graph shows results for all Kickstarter project categories in the parent category "Theater" in every year with provided data. The x-axis marks the month of initial launch of the Kickstarter, and the y-axis marks the raw count of Kickstarter projects described by their final outcome: successful (achieved or surpassed the project funding goal), failed (did not receive sufficient funding), or canceled (ended early by the Kickstarter creator). The highest number of total theater Kickstarters launched occured in May and the lowest number of total theater Kickstarters launched occured in December.

Based on the visual above, the number of canceled theater Kickstarter projects does not appear to depend on the month of initial Kickstarter launch. The largest number of canceled theater Kickstarter projects (7) were launched in January. There were 0 canceled theater Kickstarter projects launched in October-- all Kickstarters launched in October were either successful or failed.

The highest number of failed theater Kickstarter projects (52) were launched in May. Theater Kickstarters launched between November-April had the lowest numbers of failure.

The highest number of successful theater Kickstarter projects (111) were also launched in May. Theater Kickstarters launched between May-July had the highest numbers of success.

### Part 2: Analysis of Outcomes Based on Goals

Kickstarter Outcomes (successful/ failed/ canceled) versus Initial Kickstarter Goal

![Outcomes vs Goals](https://github.com/cewarkentin/kickstarter-analysis/blob/main/Outcomes%20vs%20Goals.png)

The data used to create the image above was not filtered; the provided graph shows results for all Kickstarter project categories in every year with provided data. The x-axis marks various increasing Kickstarter monetary goals, and the y-axis marks the percentage of Kickstarter projects described by their final outcome: successful, failed, or canceled.

The Outcome Based on Goals graph follows what can be logically expected--the cheapest Kickstarter goals also had the highest percentage of success (71%) and the most expensive Kickstarter goals had the lowest percentage of success (19%). Kickstarters that were not successful were more likely failed than canceled. Regardless of goal amount, the range of canceled Kickstarters was 18%. Regardless of goal amount, the range of failed Kickstarters was 33%.

Interestingly, there is a rise in percent success for Kickstarter goals $35,000-44,999. However, there is a higher percentage success for Kickstarter goals $0-14,999. Kickstarter goals higher than $44,999 quickly decline in percentage success and increase in both percent failed and canceled.

Kickstarter goals between $20,000-34,999 and $40,000+ were more likely to fail than to be successful.

### Challenges and Difficulties Encountered

One of the challenges of this project was making sure that every data point was accounted for only once. To ensure I wasn't missing or double-counting any data points, I created a table of reference values to check that my =COUNTIF() formulas were catching everything that I needed them to catch. 

![Reference table](https://github.com/cewarkentin/kickstarter-analysis/blob/main/Reference%20table.png)

Reference Table

Once I knew how many total Kickstarters there were for each outcome, I was able to use those references to ensure that the remainder of my Excel formulas were catching all the data that they needed to catch. The bottom row of the table is a sum of the columns, which I used to check against the Reference Table.

![Excel comparing to reference table](https://github.com/cewarkentin/kickstarter-analysis/blob/main/Excel%20comparing%20to%20reference%20table.png)

Final Table, checking totals against the Reference table to ensure formula accuracy.

The Reference Table was useful because I did need to adjust my formulas, and the references provided guidance on whether I was catching too few or too many pieces of data. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date? From the Outcomes based on Launch date, I can conclude that it is likely best to launch a theater Kickstarter project between May-August. Additionally, I would conclude that December is the worst month to launch a theater Kickstarter project. 

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create? Rather than creating a Pivot Table and Chart comparing raw counts of Theater Outcome versus Launch Date, I would like to look at the percentages of Outcome / Total Launched per each month. Rather than looking at raw counts of Outcome versus Launch Date, I think looking at percentages could give more insight as to which month is most likely to lead to a particular outcome. The data would look very similar, but I think it would provide an easier and more obvious interpretation of the data that I believe Louise is looking for. I believe it is harder to talk about likelihood for success when all you can say based on the table and chart created is "7 theater Kickstarter projects were canceled in January."
