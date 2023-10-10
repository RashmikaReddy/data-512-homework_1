# data-512-homework_1
The goal of this assignment is to construct, analyze, and publish a dataset of monthly article traffic for a select set of pages from English Wikipedia from July 1, 2015 through September 30, 2023. 

Preliminaries: Read About Reproducibility
Review the chapters  "Assessing Reproducibility" and "The Basic Reproducible Workflow Template" from The Practice of Reproducible Research.
Rokem, Marwick, and Staneva. Assessing Reproducibility in Kitzes, J., Turek, D., & Deniz, F. (Eds.). (2018). The Practice of Reproducible Research: Case Studies and Lessons from the Data-Intensive Sciences. Oakland, CA: University of California Press.
Kitzes. The Basic Reproducible Workflow Template in Kitzes, J., Turek, D., & Deniz, F. (Eds.). (2018). The Practice of Reproducible Research: Case Studies and Lessons from the Data-Intensive Sciences. Oakland, CA: University of California Press.

# Step 1 Data Acquistion

The fetch_data function retrieves pageviews data for a list of article titles, separates it into mobile and desktop views, and saves the results as JSON files. It involves the following steps:

Initialize result lists for mobile, desktop, and cumulative views.
Loop through article titles and make API requests for each access type.
Handle API request errors and print error messages.
Extract and combine pageviews data from API responses.
Append data to respective result lists.
Save the collected data as JSON files.

# Step 2 Analysis
2.1 Figure showing Maximum Average and Minimum Average articles text
get_max_min_avg_articles(dataframe): This function takes a DataFrame with article views data, calculates the mean views for each article, and returns DataFrames for articles with the maximum and minimum average views.

article_grouped = dataframe.groupby('article')['views'].mean().reset_index(): Within the function, the DataFrame is grouped by the 'article' column, and mean views are calculated.

max_df and min_df: These DataFrames contain articles with the highest and lowest average views, respectively.

2.2 Showing Top 10 Peak Page Views
This code identifies the top 10 articles with the highest peak page views for both mobile and desktop access, and it generates corresponding line plots for visual analysis.

2.3 Figure showing articles with fewest months of Data
This code identifies the top 10 articles with the least number of views per month for both mobile and desktop access and generates corresponding line plots for visual analysis.

