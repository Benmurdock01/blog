---
layout: post
title:  "Finding the Winner"
author: Ben Murdock
description: Go Cougs
image: "/assets/images/post3cover.jpg"
---

# Exploring College Football Success

**Reading time:** ~5 minutes

---

## Introduction & Motivation

College football captivates millions each fall, and I am sure several people make and loss a collective million in sports betting. It seems that with vast array of data that predicting the winner should be much more robust than it is.

So what variables are most important to predicting the winner? Is it sheer volume of plays, total yardage, efficiency, or perhaps turnover management? To answer this, I’ve curated a season‑by‑season dataset of NCAA teams (2013–2020) and built an interactive **Streamlit** app that lets you explore the relationships between key statistics and wins.

---

## Key Insight: Offensive Yardage Correlates with Wins

Using exploratory data analysis (EDA), one standout finding emerged:

> **Teams that rack up more total offensive yards tend to win significantly more games.**  

- Across 970 team‑seasons, the **Pearson correlation** between **Total Offensive Yards** and **Wins** was **0.74**, indicating a strong positive relationship.  
- A secondary—but still substantial—correlation of **0.62** exists between **Yards per Offensive Play** and Wins, highlighting the importance of efficiency.

![Scatter plot of offensive yards vs wins](https://github.com/Benmurdock01/blog/blob/5081b0ff7a3599b7c98987e0c0c8b0c0af209762/_posts/image1post3.png)
*Figure 1: Scatter plot showing Total Offensive Yards vs. Wins (2013–2020)*

This isn’t surprising—moving the chains and controlling the clock often translates to points on the board. But visualizing it across **all** teams and seasons drives the point home, revealing outliers (e.g., high yardage with fewer wins due to turnovers or defensive lapses).

---

## Insight #2: Play Volume Matters Too

Beyond yardage, the **number of offensive plays** also correlates with success:

- **Offensive Plays** vs. **Wins** showed a correlation of **0.57**.  
- Teams running more plays generally sustain drives and keep their defense rested.

By focusing on these two metrics—**volume** (plays) and **efficiency** (yards/play)—we gain a more holistic view of offensive performance.

---

## Introducing the Streamlit Football EDA Dashboard

To make these insights accessible, I developed a **Streamlit** app that lets you:

1. **Filter** by one or more teams  
2. **Select** any season range (e.g., 2015–2019)  
3. **Choose** different metrics (Offensive Plays, Total Yards, Yards per Play, Turnovers Lost)  
4. **Switch** between line and bar charts  
5. **Drill down** into a single team’s trends over time  
6. **Access** usage tips via an expander  

![Sidebar filters in the Streamlit app](https://raw.githubusercontent.com/benmurdock01/blog/_posts/image2.3png)
*Figure 2: Sidebar widgets for filtering teams, seasons, metrics, and chart types*

### Interactive Features at a Glance

- **Multiselect Teams**: Compare up to 10 teams side‑by‑side.  
- **Season Slider**: Zoom in on any span—ideal for pre‑ and post‑ coach changes.  
- **Metric Selectbox**: Swap between different performance indicators.  
- **Plot Type Radio**: Toggle between line and bar charts for the clearest view.  
- **Expander**: Quick “How to use” guide keeps the interface clean.  
- **Tabs**:  
  - **Overview**: Season‑by‑season averages across all selected teams.  
  - **Team Analysis**: Deep dive into a single team’s trajectory.

---

## How to Explore & Gain Insights

1. **Start Broad**  
   - Compare 5–10 teams across multiple seasons in the **Overview** tab to spot league‑wide trends (e.g., rising yardage after rule changes).  
2. **Zoom In**  
   - Switch to the **Team Analysis** tab, pick a single team, and visualize how their offensive strategy evolved.  
3. **Experiment**  
   - Swap in **Yards per Play** to see if efficiency improved under different coordinators.   
4. **Draw Conclusions**  
   - Use the app to support hypotheses—e.g., “Did Team X’s new quarterback boost offensive efficiency in Year Y?”

---

## Live Demo & Code

- **Try it yourself:** [Live Dashboard on Streamlit Cloud](https://share.streamlit.io/your-username/football_app/main/football_app.py)  
- **Browse the code:** [GitHub Repository](https://github.com/your-username/football_app)

---

## Why This Matters

- **Fans & Analysts:** Quickly test “what if” scenarios without wrestling with raw CSVs.  
- **Coaches & Players:** Identify strengths and weaknesses in offensive schemes.  
- **Stat Students & Educators:** See how EDA and interactive visualization can turn data into actionable insight.

---

## Next Steps & Further Resources

- **Dive into Turnover Margin:** Integrate defensive metrics and special teams data.  
- **Advanced Modeling:** Add linear regression to predict wins from multiple variables.  
- **More Visuals:** Incorporate heatmaps, scatter matrix, and custom tooltips.

For foundational knowledge on sports analytics, check out:

- [_Moneyball_ by Michael Lewis](https://en.wikipedia.org/wiki/Moneyball)  
- [NCAA’s Official Stats Portal](https://stats.ncaa.org/)

---

## Conclusion

By focusing on **offensive production**—both the volume of plays and the yardage gained—we see a clear link to winning in college football. But this is just the beginning: **my Streamlit app** empowers you to explore countless other angles (special teams, defensive rankings, situational performance) with minimal coding.

---
