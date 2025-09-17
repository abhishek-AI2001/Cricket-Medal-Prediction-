# Cricket Medal Prediction 🏏🥇🥈🥉

This project predicts the number of medals won by cricket-playing nations using historical team-level data and a **Linear Regression model**.  
It includes **Exploratory Data Analysis (EDA)**, model training, and evaluation.

---

## 📂 Project Structure
cricket-medal-prediction/
│── data/
│ └── teams.csv # dataset
│
│── notebooks/
│ └── cricket-medal-prediction.ipynb # Jupyter notebook with EDA + model
│
│── README.md
│── requirements.txt
│── LICENSE
│── src

---

## 📊 Dataset

The dataset (`teams.csv`) contains cricket team-level statistics such as:

| team | country     | year | events | athletes | age  | height | weight | medals | prev_medals | prev_3_medals |
|------|-------------|------|--------|----------|------|--------|--------|--------|-------------|---------------|
| AFG  | Afghanistan | 1964 | 8      | 8        | 22   | 161.0  | 64.2   | 0      | 0           | 0             |
| AFG  | Afghanistan | 2008 | 4      | 4        | 22.5 | 179.2  | 62.8   | 1      | 0           | 0             |
| AFG  | Afghanistan | 2012 | 6      | 6        | 24.8 | 171.7  | 60.8   | 1      | 1           | 0.3           |

---

## 🔍 Exploratory Data Analysis (EDA)

Some key EDA steps:
- Distribution of players, medals, and ages
- Correlation heatmaps
- Trends of medals across years
- Country-level comparisons (e.g., India vs. Afghanistan)

---

## 🤖 Model

We trained a **Linear Regression model** with predictors:

- `athletes`  
- `prev_medals`  

**Target variable:**  
- `medals`  

### Steps:
1. Split data into **Train (<2012)** and **Test (≥2012)**  
2. Train regression model  
3. Predict medal counts  
4. Post-process predictions (round, no negatives)  
5. Evaluate using **Mean Absolute Error (MAE)**  

---

## 📈 Results

- Metric used: **Mean Absolute Error (MAE)**  
- Predictions are reasonably accurate for major teams like **IND** and **AFG**  
- Error ratio also calculated per team  

---

📜 License

This project is licensed under the MIT License.

---



