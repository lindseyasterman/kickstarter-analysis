# Kickstarting with Excel

## Overview of Project

### We utilized kickstarter data to review the likelyhood of success or failure for proposed fundraising projects.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
#### We utilized the kickstarter data to create a pivot table that filtered on parent category and year of launch date.  The launch date was generated in the original kickstarter worksheet by using the Year() function. The date created conversion column was placed on the y axis and the outcomes was placed on the x axis.  We used this pivot chart to create a line graph that mapped the outcomes by launch date. ![Theater Outcomes Based on Launch Date](https://github.com/lindseyasterman/kickstarter-analysis/commit/59495c6d2d51186d5b1b73afb02ecf9dd0d9b665#diff-de24a82f3019a4edbdadd508dd42877ccdabe3dcc0de4b1d1ef754ba3ebd96d7)

### Analysis of Outcomes Based on Goals
#### For outcomes based on the goal amount, we created a new worksheet that filtered the kickstarter data based on goal amount; success,failure or canceled outcome of the fundraiser; and type of project to only include plays. After creating the coloumns and rows, I created a Countifs() funciton to sort the data into our new table.  `=COUNTIFS(kickstarter!F:F,"successful",kickstarter!D:D,"<1000",kickstarter!R:R,"plays")` This formula varied slighlty based on the information needed. I then created a pivot chart and line graph based on this data.  ![Outcomes vs Goals](https://github.com/lindseyasterman/kickstarter-analysis/commit/59495c6d2d51186d5b1b73afb02ecf9dd0d9b665#diff-0a6e3f4326491bcabef6721eea9629f44441166f5585dd3455b29bed61737449)

### Challenges and Difficulties Encountered
#### Challenges with this project began with formulating the nested countif statement. I started by trying to create one statement to select for the goal amount.  I soon realized this was more easily achieved by creating two nested statements to create the goal range. `=COUNTIFS(kickstarter!F:F,"successful",kickstarter!D:D,">=1000",kickstarter!D:D,"<=4999",kickstarter!R:R,"plays")` 

## Results

- Based on the launch date we can determine May to be the most succesful time to launch a kickstarter campaign.  We can also determine that the least number of successful campaigns were launced in December.  

- Based on campaign goals, we can determine that the highest percentage of successful campaigns kept theirs goals relatively low (under $5,000). 

- Some limitatiosns of the data set include being outdated to today's economy. This set of data averaged a start date of 2014, with the most recent date of 2017, this will not be able to account for a post-Covid economy. This data also used "pledged" donations to determine if the campaign was successful rather than actual received income. 

- Other tables and graphs that we could create include: average donation vs outcomes, number of backers vs outcomes, and length of campaign vs outcomes.
