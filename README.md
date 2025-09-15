# 🎬 Movie Dataset Analysis (Python / Pandas / Seaborn)

This project analyzes a dataset of movies using **Python**, **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**.  
It explores relationships between features such as **budget, gross earnings, votes, runtime, and ratings**, and visualizes correlations between them.

---

## 📂 Dataset
The dataset (`movies.csv`) contains movie-related features such as:
- **Name** – Movie title  
- **Rating** – MPAA rating (e.g., PG, R)  
- **Genre** – Genre classification  
- **Year** – Release year  
- **Released** – Release date string  
- **Score** – IMDb-like rating  
- **Votes** – Number of votes  
- **Director** – Director name  
- **Writer** – Writer name  
- **Star** – Lead actor/actress  
- **Country** – Country of origin  
- **Budget** – Production budget  
- **Gross** – Box office gross earnings  
- **Company** – Production company  
- **Runtime** – Runtime (minutes)  
- **Correct Year** – Extracted from `released` column for consistency  

---

## 🔍 Steps & Analysis

### 1. Data Cleaning
- Checked for **missing values** in each column.  
- Replaced missing `votes`, `budget`, and `gross` values with **0**.  
- Converted `votes`, `budget`, and `gross` to **int64** datatypes.  
- Extracted a `Correct Year` column from the `released` field.  

### 2. Exploratory Data Analysis (EDA)
- Sorted movies by **gross earnings** (highest-grossing at the top).  
- Visualized **Budget vs Gross** using:
  - **Scatter plots**
  - **Regression plots (Seaborn)**  

### 3. Correlation Analysis
- Computed **Pearson correlation coefficients** between numerical features:
  - `budget`, `gross`, `votes`, `runtime`, `score`, `year`
- Generated a **heatmap** to highlight strong/weak correlations.  
- Extracted **high-correlation feature pairs** (above 0.5).  

---

## 📊 Key Findings
- **Budget and Gross Earnings** are strongly correlated (~0.75).  
- **Votes and Gross Earnings** also show a strong correlation (~0.63).  
- **Runtime and Score** have moderate positive correlations.  
- Categorical variables (like `genre` and `company`) show little to no correlation with gross earnings.  

---

## 🚀 How to Run
1. Clone the repository and navigate into the project folder.  
2. Install dependencies (preferably in a virtual environment):  
   ```bash
   pip install pandas numpy matplotlib seaborn
