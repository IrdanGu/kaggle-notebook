# 🍕 Restaurant Revenue Prediction

A Machine Learning project using **Multiple Linear Regression** to predict restaurant revenue based on various features such as meal price, seating capacity, cuisine type, and more.

---

## 📊 Dataset

- **Source:** [Kaggle - Restaurant Revenue Prediction Dataset](https://www.kaggle.com/datasets/anthonytherrien/restaurant-revenue-prediction-dataset)
- **Size:** 8,368 restaurants × 17 features
- **Target Variable:** `Revenue`

### Features Used
| Feature | Type | Description |
|--------|------|-------------|
| Rating | Numerical | Average restaurant rating |
| Seating Capacity | Numerical | Number of available seats |
| Average Meal Price | Numerical | Average price per meal |
| Marketing Budget | Numerical | Allocated marketing budget |
| Social Media Followers | Numerical | Number of social media followers |
| Chef Experience Years | Numerical | Years of experience of head chef |
| Number of Reviews | Numerical | Total number of reviews |
| Ambience Score | Numerical | Score representing restaurant ambience |
| Service Quality Score | Numerical | Score representing service quality |
| Weekend/Weekday Reservations | Numerical | Number of reservations |
| Location | Categorical | Rural, Downtown, Suburban |
| Cuisine | Categorical | Japanese, Mexican, Italian, Indian, French, American |
| Parking Availability | Categorical | Yes / No |

---

## 🛠️ Technologies Used

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-latest-green)
![NumPy](https://img.shields.io/badge/NumPy-latest-orange)
![Scikit-Learn](https://img.shields.io/badge/ScikitLearn-latest-red)

---

## 🔄 Project Workflow

1. **Data Loading** — Import dataset using Pandas
2. **Exploratory Data Analysis (EDA)** — Understand data shape, statistics, and missing values
3. **Preprocessing**
   - Drop irrelevant column (`Name`)
   - Encode categorical variables using **Dummy Variables** (OneHotEncoding with `drop_first=True`)
4. **Train/Test Split** — 80% training, 20% testing
5. **Model Training** — Multiple Linear Regression using Scikit-Learn
6. **Model Evaluation** — R² Score

---

## 📈 Model Performance

| Metric | Score |
|--------|-------|
| **R² Score** | **0.956 (95.6%)** |

> The model explains **95.6% of the variance** in restaurant revenue — indicating a strong predictive performance.

---

## 💡 Key Insights

From the coefficient analysis, the most influential features on revenue are:

| Feature | Coefficient | Interpretation |
|---------|-------------|----------------|
| Average Meal Price | +13,497 | Higher meal price = significantly more revenue |
| Seating Capacity | +10,597 | More seats = more customers = more revenue |
| Cuisine_Japanese | -10,522 | Japanese cuisine tends to generate lower revenue |
| Location_Suburban | +2,091 | Suburban locations perform better than Downtown |

### Surprising Findings 🤔
- **Marketing Budget** had almost **no impact** on revenue (coef: -2.4)
- **Social Media Followers** also had minimal influence (coef: 0.45)

> This suggests that **quality and capacity matter more than online popularity** in driving restaurant revenue.

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/yourusername/kaggle-notebook.git

# Install dependencies
pip install pandas numpy scikit-learn

# Run the notebook
jupyter notebook restaurant_revenue.ipynb
```

---

## 📚 Concepts Applied

- Multiple Linear Regression
- Dummy Variable Encoding
- Dummy Variable Trap (drop_first=True)
- Train/Test Split
- R² Score Evaluation
- Feature Coefficient Interpretation

---

## 👤 Author

Built while learning Machine Learning — inspired by hands-on practice and curiosity about real-world data! 🚀
