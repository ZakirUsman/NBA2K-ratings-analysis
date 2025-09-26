# NBA2K-ratings-analysis

Overview:

This project explores whether NBA 2k25 overall ratings accurately reflect real-world player performance. Working in a team of three for my Data Science course. We built machine learning models to compare NBA 2K game ratings to player's current season statistics, pulling data from official sources.

We found that while NBA 2K ratings generally correlate with real-world performance, external factors such as media hype, legacy, and market size strongly influence the ratings of certain players. Our project was able to highlight Overrated and Underrated players through this process. 


Dataset:
  Data was gathered and merged from the following sources:
    nba_api - player statistics
    basketball-reference.com - advanced statistics and traditional stats
    2kratings.com - official NBA 2K25 ratings
    rapidfuzz - matched player names across datasets

  Key Statistics:
    Traditional Stats - PPG, RPG, APG, FG%, 3P%, FT%
    Advanced Stats - PER, Win Shares, BPM, TS%
    Playing Time - MPG, SPG, BPG, TPG

Technologies and Tools:
  Python
  Pandas, Numpy - data cleaning and preprocessing
  scikit-learn - Linear Regression, Randome Forest Regressor, evaluation
  Matplotlib, Seaborn - visualization of results and feature importance
  Jupyter Notebooks - reproducible workflow

Models:
  Linear Regression:
    Target - NBA 2K Overall Rating (OVR)
    Features - Win Shares (WS), Box Plus/Minus (BPM), Points Per Game (PPG)
    Results - RMSE = 2.37

  Random Forest Regressor:
    Target - NBA 2K Overall Rating (OVR)
    Features - Expanded feature set (PER, RPG, APG, FG%, 3P%, TS%, MPG, SPG, BPG, TPG
    Results - 
      Cross-validation RMSE = 2.8
      R^2 Score = .775

  Takeaway - The Random Forest model captured a broader picture and provided more insight whcih allowed us to understand the non-linear relationships better, outperforming the Linear Regression model

Key Insights:
  Lebron James - Consistently rated higher in NBA 2K that predicted. Why? Because Lebron James is the most popular and controversial player in the league leading to rating being skewed by fans perception,     legacy, media influence, and market value from a large team (Los Angeles Lakers)

  Tyrese Haliburton - Aligned closely with statistical predictions but showed evidence of small market bias in perceptions.

  Overall, the ratings showed a moderate-to-strong correlation with performance while also having certain outliers and recognizable deviations.

Results and Visualization:
  Feature importance plots identified which stats influenced model predictions most.
  
  Error analysis highlighted players who were significantly overrated or underrated.

  Case studies demonstrated how non-statistical factors impact ratings.
