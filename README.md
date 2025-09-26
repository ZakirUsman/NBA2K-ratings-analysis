# 🏀 NBA2K Ratings Analysis  

## 📌 Overview  
This project explores whether **NBA 2K25 overall ratings** accurately reflect real-world player performance. Working in a team of three for my Data Science course, we built machine learning models to compare NBA 2K ratings to player statistics from the current season, pulling data from official sources.  

We found that while NBA 2K ratings generally correlate with real-world performance, **external factors** such as media hype, legacy, and market size strongly influence the ratings of certain players. Our project highlighted both overrated and underrated players through this process.  

---

## 📊 Dataset  
Data was gathered and merged from the following sources:  
- **nba_api** → Player statistics  
- **basketball-reference.com** → Advanced and traditional stats  
- **2kratings.com** → Official NBA 2K25 ratings  
- **rapidfuzz** → Matched player names across datasets  

**Key Statistics:**  
- **Traditional Stats** → PPG, RPG, APG, FG%, 3P%, FT%  
- **Advanced Stats** → PER, Win Shares, BPM, TS%  
- **Playing Time** → MPG, SPG, BPG, TPG  

---

## 🛠️ Technologies and Tools  
- **Python**  
- **Pandas, NumPy** → Data cleaning and preprocessing  
- **scikit-learn** → Linear Regression, Random Forest Regressor, evaluation  
- **Matplotlib, Seaborn** → Visualization of results and feature importance  
- **Jupyter Notebooks** → Reproducible workflow  

---

## 🤖 Models  

### Linear Regression (Baseline)  
- **Target:** NBA 2K Overall Rating (OVR)  
- **Features:** Win Shares (WS), Box Plus/Minus (BPM), Points Per Game (PPG)  
- **Results:** RMSE = **2.37**  

### Random Forest Regressor (Ensemble)  
- **Target:** NBA 2K Overall Rating (OVR)  
- **Features:** Expanded set (PER, RPG, APG, FG%, 3P%, TS%, MPG, SPG, BPG, TPG)  
- **Results:**  
  - Cross-validation RMSE = **2.8**  
  - R² Score = **0.775**  

**Takeaway:** The Random Forest model captured non-linear relationships better and outperformed the Linear Regression baseline.  

---

## 🔍 Key Insights  
- **LeBron James** → Consistently rated higher in NBA 2K than predicted. Likely due to legacy, media hype, and market influence from playing on the Los Angeles Lakers.  
- **Tyrese Haliburton** → Aligned closely with statistical predictions but highlighted potential small-market perception bias.  
- **Overall** → Ratings showed a moderate-to-strong correlation with performance, but with clear understandable outliers.  

---

## 📈 Results and Visualization  
- Feature importance plots identified which stats influenced model predictions most.  
- Error analysis highlighted players who were significantly overrated or underrated.  
- Case studies demonstrated how **non-statistical factors** can impact ratings.  
