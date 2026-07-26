# 📊 Funnel Drop-off Analysis

## 📌 Project Overview

This project analyzes a user conversion funnel using event-level data from a website signup and checkout process. The objective is to measure user progression through each stage, calculate conversion rates, identify the largest drop-off point, and provide actionable business recommendations.

This type of analysis is commonly used by Product, Growth, and Marketing teams to identify friction points in user journeys and improve conversion rates.

---

## 🎯 Objectives

- Count unique users at each funnel stage.
- Calculate stage-to-stage conversion rates.
- Identify the biggest funnel drop-off.
- Visualize the funnel.
- Calculate average time between consecutive stages.
- Generate business recommendations based on the analysis.

---

## 🛠️ Technologies Used

- Python 3.x
- Pandas
- NumPy
- Matplotlib

---

## 📂 Dataset

The dataset contains user events from a signup funnel.

### Columns

| Column | Description |
|---------|-------------|
| user_id | Unique identifier for each user |
| step | Funnel stage reached by the user |
| timestamp | Event timestamp |

### Funnel Order

```
Visited Site
      ↓
Signup Started
      ↓
Details Filled
      ↓
Email Verified
      ↓
Purchase Completed
```

---

## 📊 Analysis Performed

### 1. Data Loading

- Loaded CSV using Pandas
- Converted timestamps into datetime format

---

### 2. Data Cleaning

- Counted only unique users per stage.
- Used the first occurrence of each event.
- Preserved the predefined funnel order.
- Considered duplicate events while counting users.
- Documented handling of skipped stages to maintain funnel integrity.

---

### 3. Funnel Metrics

Calculated:

- Unique users at each stage
- Conversion rate
- User drop-off
- Drop-off percentage

Formula:

```
Conversion Rate =
(Current Stage Users / Previous Stage Users) × 100
```

---

### 4. Biggest Drop-off

Automatically identified the stage where the maximum number of users abandoned the funnel.

---

### 5. Time-to-Convert

Calculated the average time users spent moving between consecutive funnel stages.

---

### 6. Visualization

Created a funnel bar chart showing:

- Number of users at each stage
- Funnel progression
- User drop-off

---

## 📈 Results

| Stage | Users | Conversion |
|--------|------:|-----------:|
| Visited Site | 200 | 100% |
| Signup Started | 150 | 75% |
| Details Filled | 96 | 64% |
| Email Verified | 52 | 54.17% |
| Purchase Completed | 44 | 84.62% |

### Biggest Drop-off

**Signup Started → Details Filled**

- Users Lost: **54**
- Drop-off: **36%**

---

## 💡 Business Recommendations

The highest user loss occurs between **Signup Started** and **Details Filled**, indicating that users abandon the signup process before completing their details.

Recommended improvements:

- Reduce the number of required fields.
- Simplify the signup form.
- Add a progress indicator.
- Enable auto-save for partially completed forms.
- Improve mobile responsiveness.
- Conduct A/B testing to optimize form design.

---

## ▶️ How to Run

### Clone Repository

```bash
git clone https://github.com/your-username/funnel-dropoff-analysis.git
```

### Move into Project

```bash
cd funnel-dropoff-analysis
```

### Install Dependencies

```bash
pip install pandas matplotlib numpy
```

### Run

```bash
python funnel_analysis.py
```

or

Open the Jupyter Notebook:

```bash
jupyter notebook funnel_analysis.ipynb
```

---

## 📷 Sample Output

### Funnel Summary

| Stage | Users | Conversion | Drop-off |
|--------|------:|-----------:|----------:|
| Visited Site | 200 | 100% | - |
| Signup Started | 150 | 75% | 50 |
| Details Filled | 96 | 64% | 54 |
| Email Verified | 52 | 54.17% | 44 |
| Purchase Completed | 44 | 84.62% | 8 |

---

## 📌 Key Learnings

- Funnel Analysis
- Product Analytics
- User Conversion Metrics
- Drop-off Analysis
- Time-to-Convert Analysis
- Data Aggregation using Pandas
- Business Insight Generation
- Data Visualization

---

## 🚀 Future Improvements

- Interactive Plotly Funnel Chart
- Dashboard using Streamlit
- Segment-wise Funnel Analysis
- Cohort-based Funnel Analysis
- SQL Implementation
- Power BI Dashboard
- Automated Reporting

---

## 👨‍💻 Author

**Kunjeti Venkata Nanda Kumar**

MCA Graduate | Aspiring Data Analyst | Python | SQL | Power BI | Machine Learning

---

## ⭐ If you found this project useful

Please consider giving the repository a ⭐ on GitHub.
