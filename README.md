# Kickstarting with Excel

## Overview of Project
Louise, a playwright, is examining a tabular dataset of past crowdfunding projects on Excel to successfully lead a fundraiser for a play. 
### Purpose
This project examines how different kickstarter campaigns fared in relation  to their launch dates and their funding goals. Creating visualizations of this relationship is paramount to identifying certain points-of-interest to effectively execute the next round of play-focused kickstarters. Moreover, the purpose of this project is to exercise the user's ability to use Excel as an analytical tool to reveal interesting insights and relevant attributes for what is important for the success of future projects. Inversely, these insights will assist in finding why certain projects failed. Technically, this project's purpose served the user in:
- converting **Unix Timestamps** into the mm/dd/yyyy format
- creating **Pivot Tables** to quickly summarize data
- deriving **Pivot Charts** from Pivot Tables to visualize summaries of outcomes
- using certain **Excel Functions** (COUNTIF(), YEAR(), etc.)

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Understanding theater outcomes by launch date entailed organizing the successes, failures, and cancellations by the months at which they were implemented. With the module completion setting up the foundation for this work, the **Unix Timestamp** conversion simply required me to follow directions from the module. Now that I had my dates, Excel could now identify the timeline of kickstarter plays. The **Pivot Table** below is a tabular description of theatre outcomes throughout the year. It is filtered by Parent Category and Years with Columns of Outcomes, Rows of Date Creation, and a Count of Values. A linear, visual explanation of theatre outcomes (created from the **PivotChart** portion of excel) is secondly displayed.

<img width="323" alt="Theater Outcomes Table" src="https://user-images.githubusercontent.com/106895220/174009980-d2f17418-fa98-4cb4-9bd8-0373221c20a7.png">

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/106895220/174015166-e0a99d8b-148a-44c5-bfca-d08acaa421af.png)

### Analysis of Outcomes Based on Goals

We created our analysis of Outcomes by Launch Dates. Now, we must find more from Outcomes Based on (monetary) Goals. What Goal ranges displayed the most promise and failure? Manually creating a table with a numerical and percentage dissection of success, failure, and cancellation would help. After typing in my Goal ranges (in sections of 5000s), I first extrapolated the number of successes within the desired ranges using the **COUNTIFS()** function. Examples of the first two range inputs are below. 

<img width="579" alt="Less_Than_1000_Successful" src="https://user-images.githubusercontent.com/106895220/174018038-7715cda7-d7e6-4c88-9680-4ee906f777fc.png">

<img width="760" alt="1000_to_4999_Successful" src="https://user-images.githubusercontent.com/106895220/174018860-0ef39e92-1630-4bf8-8525-c0ed4dfba9f6.png">

I follwed suit for the remainder of my Outcomes and their ranges. I then used **SUM()** to total out my rows. Finally, I divided the relevant Outcomes by their totals to get my percentages (I formatted the cells as "Percentage" so as to retain the % sign). Note that, despite their failures, no plays were canceled.

<img width="997" alt="Goal Outcomes Table" src="https://user-images.githubusercontent.com/106895220/174019464-5bbc637c-4acc-47d3-9daa-0ef30f768d45.png">

Below is a line graph of this table (with percentages).

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/106895220/174031493-638bb6f6-1af5-4d36-a188-57a7a9408745.png)


### Challenges and Difficulties Encountered

The COUNTIFS() function was my first major challenge, for I did not know exactly how to order the logic for the middle ranges such as 5000 to 9999. However, watching the Hint video helped. My second challenge was identifying my word choice when writing my Deliverable 3. I did not want to oversimplify my language, but I also did not want to overcomplicate it. I can imagine in a real-world setting that decision makers want not convoluted walls of text but coherent, succinct (yet still complex) paragraphs that are to the point. My last challenge was to try not to overthink what I am doing and trust in what I’ve learned so far. Exercising the removal of looped overthought drastically increased my workflow. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The Summer is peak season for plays. However, there is a diminishing slope until August and September where it returns to early-year values. While they are less successful than the Summer, the months of February and October should not be ignored. Also, December is not viable at all for plays.

- What can you conclude about the Outcomes based on Goals?

Success heavily depends on the goal; the success-to-failure ratio equalizes at the 15000 to 19999 range. The 1000 to 4999 range is the most optimal. Risk of failure increases for every increasing range. While minimal, the positive success ratios of 35000 to 39999 and 40000 to 44999 are significant (massive audience undertakings - projects with high, perceived realistic potential/expectations?). 

- What are some limitations of this dataset?

The dataset does not consider geographic differences (does one country enjoy summer plays more than another?). Also, it does not consider the state of the world during this year. Could there possibly be any artistic trends that lead the audience towards trusting play kickstarters than other mediums? It could be that plays hold less risk than other subcategories (video games, television, etc.). I would like to see what the average donations are like for all outcomes and what kind of plays people are putting down money for (a genre column maybe?). 

- What are some other possible tables and/or graphs that we could create?

A box-and-whisker plot could identify whether outliers are influenced by other factors in the dataset. A bar chart comparing Goal and Pledged values could help one measure enthusiasm for a fundraiser (at least, it could help find the absolute best of the best).
