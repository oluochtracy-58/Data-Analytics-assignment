# Data-Analytics-assignment
Setup → Extraction → Analysis → Sentiment → Visualization.

###Problem Identification & Data Collection

##Problem: 

A YouTuber (Infoods Special) wants to know if longer videos lead to higher engagement or if there is a "sweet spot" for video duration that maximizes Likes and Shares.
         •	Dataset: youtube_video_data.csv (Simulated via Python code).
         •	Variables: Video_ID, Title, Duration_Minutes, Views, Likes, Comments.
         •	Source: YouTube Data API.

##Exploratory Data Analysis (EDA)
Using the summary statistics generated, we look for the "Average" performance:
               •	Mean Engagement Rate: If the mean is 5%, we use this as a benchmark.
               •	Standard Deviation: Shows if video performance is consistent or fluctuates wildly.
               
##Visualization & Interpretation
•	Regression Plot: The line of best fit in the Duration vs Engagement plot tells us the trend. If the line slopes upward, longer videos are better. If it’s flat, duration doesn't matter.

•	Heatmap: This identifies "hidden" drivers. For example, if Comments have a higher correlation with Views than Likes do, the creator should focus on "call-to-action" questions in their scripts.

##Mathematical Analysis
We use the Engagement Rate formula to normalize the data across videos of different sizes:
$$Engagement\ Rate = \frac{Likes + Comments}{Views} \times 100$$

##Linear regression analysis 
To predict 'Engagement_Rate' using 'Duration_Min' as the independent variable from the df DataFrame: Overlay the regression line on the existing scatter plot, add a legend to distinguish the regression line, and output the regression equation along with the R-squared value.
##Prepare Data for Regression
Subtask:
Select the 'Duration_Min' as the independent variable (X) and 'Engagement_Rate' as the dependent variable (y) for the regression analysis. 
**Reasoning**:
The subtask requires selecting 'Duration_Min' as the independent variable (X) and 'Engagement_Rate' as the dependent variable (y) from the 'df' DataFrame, reshaping 'X' for scikit-learn compatibility.


         
