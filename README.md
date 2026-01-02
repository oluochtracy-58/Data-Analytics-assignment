# Data-Analytics-assignment
Setup → Extraction → Analysis → Sentiment → Visualization.

##Problem Identification & Data Collection

###Problem: 

A YouTuber (Infoods Special) wants to know if longer videos lead to higher engagement or if there is a "sweet spot" for video duration that maximizes Likes and Shares.
         •	Dataset: youtube_video_data.csv (Simulated via Python code).
         •	Variables: Video_ID, Title, Duration_Minutes, Views, Likes, Comments.
         •	Source: YouTube Data API.

Exploratory Data Analysis (EDA)
Using the summary statistics generated, we look for the "Average" performance:
               •	Mean Engagement Rate: If the mean is 5%, we use this as a benchmark.
               •	Standard Deviation: Shows if video performance is consistent or fluctuates wildly.
               
Visualization & Interpretation
•	Regression Plot: The line of best fit in the Duration vs Engagement plot tells us the trend. If the line slopes upward, longer videos are better. If it’s flat, duration doesn't matter.

•	Heatmap: This identifies "hidden" drivers. For example, if Comments have a higher correlation with Views than Likes do, the creator should focus on "call-to-action" questions in their scripts.
         
