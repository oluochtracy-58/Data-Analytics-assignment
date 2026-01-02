# Data-Analytics-assignment
Setup → Extraction → Analysis → Sentiment → Visualization.

__###Problem Identification & Data Collection__

__##Problem:__ 

A YouTuber (Infoods Special) wants to know if longer videos lead to higher engagement or if there is a "sweet spot" for video duration that maximizes Likes and Shares.
         •	Dataset: youtube_video_data.csv (Simulated via Python code).
         •	Variables: Video_ID, Title, Duration_Minutes, Views, Likes, Comments.
         •	Source: YouTube Data API.

__##Exploratory Data Analysis (EDA)__
Using the summary statistics generated, we look for the "Average" performance:
               •	Mean Engagement Rate: If the mean is 5%, we use this as a benchmark.
               •	Standard Deviation: Shows if video performance is consistent or fluctuates wildly.
               
__##Visualization & Interpretation__
•	Regression Plot: The line of best fit in the Duration vs Engagement plot tells us the trend. If the line slopes upward, longer videos are better. If it’s flat, duration doesn't matter.

•	Heatmap: This identifies "hidden" drivers. For example, if Comments have a higher correlation with Views than Likes do, the creator should focus on "call-to-action" questions in their scripts.

__##Mathematical Analysis__
We use the Engagement Rate formula to normalize the data across videos of different sizes:
$$Engagement\ Rate = \frac{Likes + Comments}{Views} \times 100$$

__##Linear regression analysis__ 
To predict 'Engagement_Rate' using 'Duration_Min' as the independent variable from the df DataFrame: Overlay the regression line on the existing scatter plot, add a legend to distinguish the regression line, and output the regression equation along with the R-squared value.

__##Prepare Data for Regression__
*Subtask*:
Select the 'Duration_Min' as the independent variable (X) and 'Engagement_Rate' as the dependent variable (y) for the regression analysis. 


**Reasoning**:
**The subtask requires selecting 'Duration_Min' as the independent variable (X) and 'Engagement_Rate' as the dependent variable (y) from the 'df' DataFrame, reshaping 'X' for scikit-learn compatibility**.


__Final Task__
*Subtask*:
Provide the regression equation and R-squared value to interpret the relationship between video duration and engagement rate.


__Insights & Recommendations__
•	Insight: If the correlation between duration and engagement is low (e.g., $0.15$), the audience likely values the topic more than how long the video is.

•	Insight: If engagement drops significantly after 15 minutes, the creator is likely "stretching" content too thin.

•	Recommendation: Based on the data, the creator should aim for a "Sweet Spot" duration (e.g., 10–12 minutes) and prioritize comment-driven interaction to boost the engagement algorithm.
•	The low R-squared value (\$0.11\$) suggests that 'Duration\_Min' alone is not a strong predictor of 'Engagement\_Rate'. Other factors likely influence engagement more significantly.
•	Future analysis should explore additional independent variables (e.g., video content, topic, thumbnail quality, audience demographics) and potentially more complex regression models to better predict and understand video engagement.

__Justification of Tools__
•	Pandas: The industry standard for data manipulation (calculating the Engagement Rate).
•	Seaborn/Matplotlib: These libraries translate raw numbers into visual trends that a non-technical creator can understand.
•	Correlation Coefficient: This provides a mathematical justification for the recommendations, moving beyond "gut feelings."

API Extraction	Used the YouTube Data API to ensure the data is objective and comes directly from the source.
Normalization	Calculated Engagement Rate as a percentage to fairly compare a video with 1M views to a video with 1k views.
NLP (Sentiment)	Used VADER Sentiment Analysis because it recognizes social media context (emojis/slang) better than a standard dictionary.
Visualizations	Used Box Plots to see the distribution of views across sentiment categories, identifying outliers

Summary:
•	The regression equation is `Engagement_Rate = -0.08 * Duration_Min + 4.19`.
•	The R-squared value is `0.11`.
Data Analysis Key Findings
•	A linear regression model was successfully fitted to predict 'Engagement\_Rate' using 'Duration\_Min'.
•	The regression equation derived is `Engagement_Rate = -0.08 * Duration_Min + 4.19`, indicating a slight negative relationship between video duration and engagement rate. For every one-minute increase in video duration, the engagement rate is predicted to decrease by 0.08 percentage points.
•	The R-squared value for the model is `0.11`, meaning that approximately 11% of the variance in 'Engagement\_Rate' can be explained by 'Duration\_Min'.
•	 A scatter plot visualizing 'Duration\_Min' vs. 'Engagement\_Rate' with the overlaid regression line was successfully generated and saved.


__##Summary:__
•	The regression equation is `Engagement_Rate = -0.08 * Duration_Min + 4.19`.
•	The R-squared value is `0.11`.
__Data Analysis Key Findings__
•	A linear regression model was successfully fitted to predict 'Engagement\_Rate' using 'Duration\_Min'.

•	The regression equation derived is `Engagement_Rate = -0.08 * Duration_Min + 4.19`, indicating a slight negative relationship between video duration and engagement rate. For every one-minute increase in video duration, the engagement rate is predicted to decrease by 0.08 percentage points.

•	The R-squared value for the model is `0.11`, meaning that approximately 11% of the variance in 'Engagement\_Rate' can be explained by 'Duration\_Min'.

•	 A scatter plot visualizing 'Duration\_Min' vs. 'Engagement\_Rate' with the overlaid regression line was successfully generated and saved.


         
