# 📦 Impact of COVID-19 on ABC Company's Parcel Delivery Business

> Data Science Case Study | AI and Data Analysis Program | Saskatchewan Polytechnic

---

## 📌 Project Overview

This case study analyzes the **impact of the COVID-19 pandemic** on a parcel delivery company (ABC Company) by examining weekly shipment volumes, customer behavior, and revenue across 2019 and 2020.

Using real-world-style business data, the analysis uncovers how pandemic-driven disruptions reshaped customer segments, delivery volumes, and overall business performance — providing actionable insights for business decision-making.

---

## 👥 Authors

**Irorere Osaheni & Nadeem Baasil**
Post-Graduate Diploma in AI and Data Analysis
Saskatchewan Polytechnic | Regina, SK, Canada

- GitHub: [github.com/Malcolm-28](https://github.com/Malcolm-28)
- LinkedIn: [linkedin.com/in/osaheni-irorere-368b52362](https://linkedin.com/in/osaheni-irorere-368b52362)

---

## 🎯 Key Business Questions Answered

1. When and how did COVID-19 first impact parcel volumes?
2. How did COVID-19 affect the peak season in 2020 compared to 2019?
3. How were different customer segments (Enterprise, Large, Medium, Small) affected?
4. What percentage of each customer group was growing, declining, or moderately growing?
5. What percentage of customers were new or lost during the COVID observation period?
6. What was the overall impact on volumes and revenue by customer group?

---

## 📁 Dataset

**File:** `COVID_Parcel_Business.csv`

| Column | Description |
|--------|-------------|
| `THE_WEEK` | Week number of the year |
| `THE_YEAR` | Year (2019 or 2020) |
| `VOLUME` | Total parcel volume shipped |
| `FakeCustomerID` | Anonymized unique customer identifier |

**Generated Output:** `UpdatedDF.csv` — customer volume summary with assigned business categories

**Customer Segments Defined:**

| Category | Annual Volume |
|----------|--------------|
| Enterprise | > 500,000 parcels |
| Large | 200,000 – 499,999 parcels |
| Medium | 10,000 – 199,999 parcels |
| Small | 1,000 – 9,999 parcels |
| Lesser than 1K | < 1,000 parcels |

---

## 🧰 Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python 3 | Core programming language |
| Pandas | Data manipulation and aggregation |
| NumPy | Numerical computations |
| Matplotlib | Charts and visualizations |
| Seaborn | Statistical plots |
| Google Colab | Development environment |

---

## 🔬 Methodology & Analysis

### 1. Data Loading & Exploration
- Loaded `COVID_Parcel_Business.csv` and performed initial exploration using `head()`, `tail()`, `describe()`, `info()`, and `isnull().sum()`
- Confirmed no null values in the dataset

### 2. Weekly Volume Analysis (2019 vs 2020)
- Aggregated weekly parcel volumes by year using `groupby()`
- Plotted line graphs to compare 2019 and 2020 volume trends side by side
- Identified **Week 12 (mid-March 2020)** as the point where COVID impact began

### 3. COVID Timeline Analysis
- Annotated the chart to mark the COVID impact start point
- Mapped volume changes to real-world COVID events in Canada:
  - **Week 11–12**: WHO declared pandemic; lockdowns began
  - **Week 12–13**: Business closures reduced commercial shipping
  - **Week 15+**: E-commerce surge began offsetting B2B declines

### 4. Peak Season Analysis
- Compared the 2019 and 2020 peak seasons using a continuous weekly index
- Found the 2020 peak started **earlier** and reached **higher volumes** than 2019 due to increased e-commerce demand

### 5. Customer Segmentation
- Grouped customers by total annual volume into 5 categories
- Compared customer counts and volumes across 2019 and 2020 per segment
- Visualized distribution using **grouped bar charts** and **pie charts**

### 6. Growth Classification
- Calculated growth rate per customer category using ISGR formula:

```
ISGR (%) = (Volume_2020 - Volume_2019) / Volume_2019 × 100
```

- Classified each segment as: **Growing** (>10%), **Moderately Growing** (0–10%), or **Declining** (<0%)

### 7. New & Lost Customer Analysis
- Identified new customers in 2020 (not present in 2019)
- Calculated percentage of 2019 customers lost per segment

### 8. Revenue Impact Analysis
- Estimated revenue using a base cost of **$22 per parcel**
- Calculated revenue change in absolute ($) and percentage (%) terms per customer group
- Visualized volume and revenue comparisons using grouped bar charts

---

## 📊 Key Findings

- COVID-19 impact on parcel volumes began at **Week 12 of 2020** (mid-March)
- **Enterprise and Large customers** experienced the strongest growth during COVID, driven by e-commerce
- **Small customers** saw a contraction in volumes and some churn
- The 2020 peak season started **earlier and lasted longer** than 2019
- **No new customers** were acquired during the COVID observation period in 2020
- Small segment lost **1.63%** of customers; Medium lost **0.57%**; Enterprise and Large lost **none**
- Overall business volumes and revenue **increased** in 2020, concentrated among high-volume customer groups

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)
1. Upload `COVID_Parcel_Business.csv` to your Colab session files
2. Open `Covid_19_Case_Study.ipynb` in Google Colab
3. Run all cells from top to bottom

### Option 2 — Local Jupyter Notebook
1. Clone this repository:
```bash
git clone https://github.com/Malcolm-28/covid19-business-impact.git
cd covid19-business-impact
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Launch Jupyter:
```bash
jupyter notebook
```

4. Open `Covid_19_Case_Study.ipynb` and run all cells

---

## 📂 Repository Structure

```
covid19-business-impact/
│
├── Covid_19_Case_Study.ipynb     # Main analysis notebook
├── COVID_Parcel_Business.csv     # Raw dataset
├── UpdatedDF.csv                 # Generated customer summary file
├── installation.ipynb            # Library installation notebook
└── README.md                     # Project documentation
```

---

## 📚 References

- [Pandas Indexing Documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy)
- [Week Number Reference](http://www.whatweekisit.org/)
- Saskatchewan Polytechnic — AI and Data Analysis Program

---

*Irorere Osaheni & Nadeem Baasil — Saskatchewan Polytechnic | AI and Data Analysis Program*
