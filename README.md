# ⚽ Premier League Football Club Investment Analysis

## 📌 Project Overview
A renowned investment firm is looking to invest in a top-tier sports team with high potential in the English Premier League (EPL). However, established "Big 6" clubs are already owned by competitors or are too expensive. 

**The Goal:** Use data analytics to identify a high-performing, mid-tier club that the firm can approach for a potentially profitable investment deal.

## 📂 Dataset
The dataset contains historical performance data for clubs that have participated in the Premier League.
*   **Source:** `Premier League Final Data.csv`
*   **Key Attributes:** Matches Played, Wins, Losses, Draws, Goals Scored, Clean Sheets, Team Launch Year, Titles Won, and Last Year Played.

## ⚙️ Methodology

### 1. Data Cleaning & Preprocessing
*   **Sanitization:** Removed numerical artifacts from Club names.
*   **Handling Nulls:** Imputed missing values for 'Winners' and 'Runners-up' columns.
*   **Formatting:** Converted 'TeamLaunch' to datetime format and extracted the year.
*   **Deriving Metrics:** Created normalized metrics such as *Winning Rate*, *Loss Rate*, *Draw Rate*, and *Clean Sheet Rate* to ensure fair comparison across teams with different match counts.

### 2. Exploratory Data Analysis (EDA)
*   **Filtering:** Excluded established clubs with >900 matches (e.g., Man Utd, Arsenal, Liverpool) to focus on potential growth targets.
*   **Outlier Detection:** Used Boxplots to identify clubs with exceptional winning rates and clean sheet records relative to their peers.
*   **Recency Bias:** Filtered for teams currently active or recently active (2021-2023) in the Premier League to ensure current form relevance.

### 3. Scoring System
A weighted scoring algorithm was developed to rank the clubs:
*   **+15 points:** High Winning Rate, Low Losing Rate, Past PL Winners, Currently Playing in 2023.
*   **+10 points:** High Experience (Matches Played), Low Draw Rate, High Clean Sheet Rate, Past Runners-up.

## 📊 Key Findings
*   **Initial Analysis:** *Blackburn Rovers* scored the highest based on historical data. However, secondary research and the `lastplayed_pl` column revealed they haven't played in the Premier League since 2012.
*   **Secondary Analysis:** *Leicester City* emerged as the next best candidate. They have a strong winning rate, won the title in 2016, and have consistently performed in the top tier in recent years (up to the dataset limit).

## 🏆 Final Recommendation
**Leicester City** is recommended for investment. 
They demonstrate the best balance of historical success, recent high-level performance, and future potential compared to other mid-tier clubs.

## 🛠️ Technologies Used
*   **Python**
*   **Pandas** (Data Manipulation)
*   **NumPy** (Numerical Analysis)
*   **Matplotlib** (Data Visualization)

## 🚀 How to Run
1.  Clone the repository.
2.  Install dependencies:
    ```bash
    pip install pandas numpy matplotlib
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook "Premier League Investment Analysis.ipynb"
    ```

---
*Note: This analysis is based on data updated as of March 2023.*
