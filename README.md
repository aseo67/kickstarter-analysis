# Kickstarting with Excel
Module 1 Challenge
Data Analysis File (Excel) Link: 
![Screenshot](https://github.com/aseo67/kickstarter-analysis/blob/main/Kickstarter_Challenge.xlsx.zip)

## Overview of Project

### Background/Purpose
In preparation of the new play _Fever_, the playwright, Louise, currently estimates a needed budget of over $10,000. Prior to launching a crowdfunding campaign to help fund this budget, Louise would like to gain insight into how she can execute a successful campaign. This analysis explores historical Kickstarter campaigns and what factors drive those that have succeeded in reaching their goal. With these insights, Louise can determine the best path forward for her play's campaign in maximizing success potential.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
First, we explored theater campaign data to determine if the time of year when a campaign launches plays a role in a successful outcome. 
Using a pivot table, the campaign data - organized by launch date and their respective outcomes - was populated, filtered to focus on campaigns only from the theater category that were successful, failed or canceled. 
  ![Screenshot](https://github.com/aseo67/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
Next, we narrowed down to campaigns for plays, looking at the dollar amount goals vs. their outcomes to determine if there are any trends in what succeeds vs. fails depending on the goal amount a campaign initially set out to achieve. 
For this analysis, we utilized COUNTIF() functions to tally successful, failed and canceled campaigns across specified goal amount dollar-ranges. With this data, we then determined the % of success vs. fail vs. cancellations for each dollar range. 
  ![Screenshot](https://github.com/aseo67/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
The raw dataset initially posed some challenges, specifically in data set-up, that would potentially lead to analytical roadblocks if not addressed. 
- The "_launched at_" and "_deadline_" data were provided as Unix timestamps, necessitating a conversion to readable dates. These conversions have been added to the Kickstarter data sheet, in addition to a "_years_" categorization to help filter the data by launch year. 
  ![Screenshot](https://github.com/aseo67/kickstarter-analysis/blob/main/Screenshot_Data%20Cleaning_Time%20Conversion.png)
- Granular filtering was not initially feasible given the combined parent category and subcategory data in single cells. These have been split out into respective columns to enable ease of analysis at the parent category level (i.e. theater). 
  ![Screenshot](https://github.com/aseo67/kickstarter-analysis/blob/main/Screenshot_Data%20Cleaning_Category.png)
- Also note that some campaigns are categorized as "_live_". These have been excluded from the analysis as needed, to focus insights on completed programs and why they achieved, failed or canceled. 

## Results
### - What are two conclusions you can draw about the Outcomes based on Launch Date?  
   - The number of successful theater campaigns spike in the summer months, particularly May through July, with the biggest spike in May. 
   - However, these summer months also saw the highest levels of failed campaigns, as these peak May through August as well as in October. 
### - What can you conclude about the Outcomes based on Goals?
   - Majority of the campaigns had goals of $5,000 or less. The campaigns with these smaller goal amounts have a higher proportion of successful crowdsourcing. 
   - The higher the goal is, the more failure that is observed, as we see goals of $20,000 or greater tend to have more failures than successes. That said, it is also important to note that the base size of cases are very small as we narrow down to higher dollar amounts (e.g. only 62 out of the 1047 play campaigns have budgets of $20,000 or greater). 
   - Focusing on the budget range of interest ($10,000 to $14,999)- given Louise's expected budget of over $10,000 - we see that the percentage of successful campaigns (54%) is just about on par with failed campaigns (46%). This suggests there's some risk involved with a $10,000+ campaign. 
### - What are some limitations of this dataset?
   - This dataset lacks the most recent data, as it only contains campaigns launched through early 2017. Understanding the most recent years' dynamics is also important as there is a chance that external factors that can change year over year, such as the economy, can play a role in the success of a campaign. 
   - This data spans multiple countries, and thus various currencies. While we can hone in on specific countries for analyses, taking a global view of the data can be limited as we are looking at financial data where different currencies and exchange rates results in less apples-to-apples data. 
### - What are some other possible tables and/or graphs that we could create?
   - As mentioned above, there are fewer cases of higher budget campaigns. It may be good to gutcheck if the higher proportion of failures is observed in other categories as well - as that would indicate that a crowdsourcing campaign with a high goal poses risk of failure overall, and is not isolated to a certain category and how potential donors react to a certain category and its goal. 
   - We could also look into the average donation of a campaign vs. the launch date (to see if time of year for a campaign impacts how much people usually donate) or vs. the outcome (to see if successful campaigns tend to have larger or smaller contributions). 
   - Both analyses can be narrowed down to the country of interest, to see if certain countries observe more or less successful campaigns. 
   - A similar "Outcomes Based on Goals" analysis can be conducted at a more macro level for the theater category, to help determine if this is a dynamic unique to campaigns for plays, or is consistent throughout the theater category.
   - This dataset also includes "_Spotlight_" and "_Staff Pick_" data. The extra feature of having the campaign be spotlighted or having it labeled as a staff pick, can also play a role in the success. It would be worth exploring for relationships of these features vs. outcomes of campaigns. 


