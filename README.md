# 🎓 Pluto Academy — Data Analytics Internship
### Laxman | Intern Projects Portfolio

> **Program:** Pluto Academy — Data Analytics Internship 2026
> **Tools:** Python · Pandas · Matplotlib · Seaborn · Numpy
> **Platform:** [plutoacademy.in](https://plutoacademy.in)

---

## 📁 Projects in This Repository

| # | Project | Dataset | GitHub |
|---|---|---|---|
| 01 | E-Commerce Sales Analysis | Olist Brazilian E-Commerce (Kaggle) | [plutoProject-1-Ecommerce](https://github.com/laxman243ops/plutoProject-1-Ecommerce.git) |
| 02 | Student Performance Analysis | Students Performance in Exams (Kaggle) | [plutoProject2-Student-performance](https://github.com/laxman243ops/plutoProject2-Student-performance.git) |

---

---

# 📦 Project 01 — E-Commerce Sales Analysis

🔗 **GitHub Repository:** https://github.com/laxman243ops/plutoProject-1-Ecommerce.git

## Overview

This project performs a full exploratory data analysis (EDA) on the **Olist Brazilian E-Commerce dataset** — a real-world dataset from Brazil's largest e-commerce marketplace. The goal was to uncover actionable business insights about revenue trends, product performance, regional distribution, customer reviews, and order value patterns across 23 months of transactional data.

---

## 📊 Dataset

**Source:** [Olist Brazilian E-Commerce — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

| File | Description |
|---|---|
| `olist_orders_dataset.csv` | Order status, timestamps |
| `olist_order_items_dataset.csv` | Items per order, prices, freight |
| `olist_products_dataset.csv` | Product categories |
| `olist_order_reviews_dataset.csv` | Customer review scores |
| `olist_customers_dataset.csv` | Customer location data |
| `product_category_name_translation.csv` | Portuguese → English category names |

---

## 🧹 Data Cleaning Summary

| Step | Action | Result |
|---|---|---|
| Date columns | Converted 5 columns to datetime | Fixed for trend analysis |
| Order filter | Kept only `delivered` status orders | Removed cancelled/pending |
| Null values | Filled unknown categories with `'Unknown'` | No data loss |
| Table merge | Merged 6 CSVs into one master dataframe | Ready for analysis |
| Duplicates | Removed all duplicate rows | Clean dataset |

---

## 📈 KPI Summary

| KPI | Value |
|---|---|
| 💰 Total Revenue | **R$ 1,829,209.53** |
| 📦 Total Orders | **13,339** |
| 🏆 Top Category | **beleza_saude** (R$ 1,47,980.12) |
| 📅 Peak Month | **April 2018** |
| 🏙️ Best State | **SP — São Paulo** (R$ 19,302.56) |
| ⭐ 5-Star Reviews | **56.4%** |
| 🚨 1-Star Reviews | **13.8%** |

---

## 🔍 5 Questions Answered

**Q1. Which product category has the highest revenue?**

`beleza_saude` (Beauty & Health) leads all categories with **R$ 1,47,980.12** — outperforming #2 by over 11%.

| Rank | Category | Revenue |
|---|---|---|
| 1 | beleza_saude | R$ 1,47,980.12 |
| 2 | relogios_presentes | R$ 1,32,362.31 |
| 3 | cama_mesa_banho | R$ 1,13,063.84 |
| 4 | esporte_lazer | R$ 1,12,500.21 |
| 5 | informatica_acessorios | R$ 1,10,155.85 |

---

**Q2. Which month had peak sales?**

**April 2018** — Revenue ~R$ 17,000. Monthly revenue grew **17× in 23 months** (from ~R$ 1,000 in Oct 2016). Q2 (April–June) consistently outperforms all other quarters in both 2017 and 2018.

---

**Q3. Which region performs best?**

**SP (São Paulo)** dominates at R$ 19,302.56 — nearly **3× more than #2 RJ** (R$ 7,080.74).

| State | Revenue |
|---|---|
| SP — São Paulo | R$ 19,302.56 |
| RJ — Rio de Janeiro | R$ 7,080.74 |
| SC — Santa Catarina | R$ 6,531.87 |
| MG — Minas Gerais | R$ 4,408.29 |

---

**Q4. What is the average order value (AOV) trend?**

AOV declined from **R$ 253.30** (Oct 2016) to **R$ 89.41** (Apr 2017) — a **65% drop** — before stabilising. This reflects market maturation and increased price competition as the platform scaled. The majority of orders fall below R$ 300, with a sharp concentration under R$ 100.

---

**Q5. What is the customer review score distribution?**

| Stars | Percentage | Count |
|---|---|---|
| ⭐⭐⭐⭐⭐ 5 stars | 56.4% | 1,236 |
| ⭐⭐⭐⭐ 4 stars | 17.7% | 388 |
| ⭐ 1 star | 13.8% | 302 |
| ⭐⭐⭐ 3 stars | 8.3% | 181 |
| ⭐⭐ 2 stars | 3.9% | 86 |

---

## 📉 Visualisations

| # | Chart Type | What It Shows |
|---|---|---|
| Chart 1 | Horizontal Bar | Top 10 Categories by Total Revenue |
| Chart 2 | Line + Bar (dual axis) | Monthly Revenue Trend + Order Volume |
| Chart 3 | Horizontal Bar | Top 10 States by Revenue |
| Chart 4 | Histogram | Distribution of Order Values |
| Chart 5 | Pie Chart | Customer Review Score Breakdown |
| Chart 6 | Heatmap | Revenue per Category per Month |
| Dashboard | KPI Cards | 6 Key Business Metrics |

All charts include titles, axis labels, and legends.

---

## 💡 Business Insights

### Insight 1 — Beauty & Health is the Undisputed Revenue Leader
`beleza_saude` generated R$ 1,47,980.12 — the highest of all categories. The heatmap confirms consistent monthly sales across all 23 months; this is not a seasonal spike but a year-round revenue engine.

**Recommendation:** Increase inventory depth and allocate 20–25% more marketing budget to beauty and health products year-round. Introduce a loyalty rewards program for repeat buyers to reduce churn and increase customer lifetime value.

---

### Insight 2 — Revenue Grew 17× in 2 Years with Clear Seasonal Peaks
Monthly revenue grew from ~R$ 1,000 (Oct 2016) to ~R$ 17,000 (Apr 2018). Q2 (April–June) consistently outperforms all other quarters in both years, indicating a seasonal demand cycle.

**Recommendation:** Launch targeted promotional campaigns in February–March to pre-load Q2 demand. Ramp up logistics capacity and seller stock requirements before April each year to prevent supply-side shortfalls during peak traffic.

---

### Insight 3 — São Paulo Dominance Creates Regional Concentration Risk
SP generated R$ 19,302.56 — nearly 3× more than #2 RJ. This extreme geographic concentration means the business is disproportionately exposed to disruptions in a single state.

**Recommendation:** Dedicate campaign budgets for underperforming states — CE, PB, SE, PR, RS, and BA. Set a target of 10% regional revenue diversification within 12 months through state-specific promotions and faster delivery options.

---

### Insight 4 — 1-Star Reviews Are the Second Most Common Rating
Despite 56.4% five-star ratings, the 1-star rating at 13.8% is the second most frequent — surpassing both 2-star (3.9%) and 3-star (8.3%). This bimodal distribution signals specific, addressable product or delivery failures.

**Recommendation:** Cross-reference 1-star reviews with product category and delivery time data. Implement minimum seller quality standards in high-revenue categories. Target a 50% reduction in 1-star reviews within two quarters through direct seller performance monitoring.

---

### Insight 5 — Average Order Value is Declining and Most Orders Are Below R$ 300
The order value histogram shows extreme right-skew with a peak under R$ 100. AOV dropped 65% from Oct 2016 to Apr 2017 before stabilising.

**Recommendation:** Introduce bundle offers and a minimum-spend incentive (e.g. "Spend R$ 300, get free delivery + 10% off"). Create curated product combinations in the top 3 categories to encourage larger basket sizes. Track AOV monthly as a leading indicator of revenue health.

---

### 🔍 Most Surprising Finding
`fashion_roupa_masculina` (men's clothing) and `papelaria` (stationery) show extreme isolated revenue spikes in just one or two months on the heatmap — then essentially disappear for the rest of the year. Despite these dramatic spikes, neither category appears in the top 10 by total annual revenue. Consistent performers like `beleza_saude` generate far more cumulative value than one-time viral moments.

---

## 🚀 How to Run — Project 01

```bash
# Clone the repository
git clone https://github.com/laxman243ops/plutoProject-1-Ecommerce.git
cd plutoProject-1-Ecommerce

# Install dependencies
pip install pandas matplotlib seaborn numpy

# Run the analysis
python project01_ecommerce.py
```

> Place all Olist CSV files in the same directory before running.

---

## 📁 Output Files — Project 01

```
project01_outputs/
├── chart1_revenue_by_category.png
├── chart2_monthly_trend.png
├── chart3_regional_sales.png
├── chart4_order_value_histogram.png
├── chart5_review_scores_pie.png
├── chart6_category_month_heatmap.png
└── dashboard_kpi.png
```

---
---

# 🎓 Project 02 — Student Performance Analysis

🔗 **GitHub Repository:** https://github.com/laxman243ops/plutoProject2-Student-performance.git

## Overview

This project performs a full exploratory data analysis (EDA) and student segmentation on the **Students Performance in Exams dataset** from Kaggle. The goal was to identify the key factors affecting student scores — parental education, test preparation, gender, and socioeconomic status — and to produce a Principal's Report with actionable recommendations for improving student outcomes.

---

## 📊 Dataset

**Source:** [Students Performance in Exams — Kaggle](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)

File used: `StudentsPerformance.csv`

| Property | Value |
|---|---|
| Rows | 1,000 |
| Columns | 8 |
| Missing Values | 0 |
| Duplicates | 0 |

---

## 🧹 Data Exploration & Cleaning

1. **Total students:** 1,000
2. **Gender split:** Female 518 · Male 482
3. **Average scores:** Math 66.1 · Reading 69.2 · Writing 68.1
4. **Parental education levels:** 6 unique categories
5. **Test prep completion:** Completed 358 · None 642

**Cleaning steps performed:**
- Renamed columns for clarity (removed spaces, standardised format)
- Added derived columns: `total_score` and `average_score`
- Confirmed zero null values — no imputation required
- Confirmed zero duplicate rows — no removal needed
- Reordered parental education levels from lowest to highest for analysis

---

## 📈 KPI Summary

| KPI | Value |
|---|---|
| 👨‍🎓 Total Students | **1,000** |
| 📐 Avg Math Score | **66.1 / 100** |
| 📖 Avg Reading Score | **69.2 / 100** |
| ✍️ Avg Writing Score | **68.1 / 100** |
| 📊 Avg Total Score | **203.3 / 300** |
| ⚠️ At-Risk Students | **188 (18.8%)** |
| 🏆 High Performers (250+) | **139 students** |
| 📉 Low Scorers (below 150) | **103 students** |

---

## 🔍 5 Questions Answered

**Q1. Does parental education level affect scores?**

Yes — significantly. Scores improve consistently with higher parental education across all three subjects.

| Parental Education | Math | Reading | Writing | Count |
|---|---|---|---|---|
| some high school | 63.5 | 66.9 | 64.9 | 179 |
| high school | 62.1 | 64.7 | 62.4 | 196 |
| some college | 67.1 | 69.5 | 68.8 | 226 |
| associate's degree | 67.9 | 70.9 | 69.9 | 222 |
| bachelor's degree | 69.4 | 73.0 | 73.4 | 118 |
| master's degree | 69.7 | 75.4 | 75.7 | 59 |

**Math gap from lowest to highest parental education: +6.2 points**

---

**Q2. Do students who complete test prep score higher?**

Yes — across all three subjects, test prep students consistently outperform those without.

| Test Prep | Math | Reading | Writing | Students |
|---|---|---|---|---|
| Completed | 69.7 | 73.9 | 74.4 | 358 |
| None | 64.1 | 66.5 | 64.5 | 642 |

**Test prep improvement: +5.6 Math · +7.4 Reading · +9.9 Writing**

---

**Q3. What is the correlation between subjects?**

| | Math | Reading | Writing |
|---|---|---|---|
| Math | 1.000 | 0.818 | 0.803 |
| Reading | 0.818 | 1.000 | 0.955 |
| Writing | 0.803 | 0.955 | 1.000 |

Reading and Writing are near-perfectly correlated (r = 0.955). A student who struggles in one will almost certainly struggle in both — allowing the school to address both with a single combined literacy intervention.

---

**Q4. Which gender performs better in which subject?**

| Gender | Math | Reading | Writing | Count |
|---|---|---|---|---|
| Female | 63.6 | 72.6 | 72.5 | 518 |
| Male | 68.7 | 65.5 | 63.3 | 482 |

- **Math:** Male leads by +5.1 points
- **Reading:** Female leads by +7.1 points
- **Writing:** Female leads by +9.2 points

---

**Q5. What is the distribution of total scores?**

| Statistic | Value |
|---|---|
| Mean | 203.3 |
| Median | 205.0 |
| Std Dev | 42.8 |
| Min | 27 |
| Max | 300 |
| 25th Percentile | 175 |
| 75th Percentile | 233 |
| High performers (250+) | 139 students |
| Low scorers (below 150) | 103 students |

---

## 📉 Visualisations

| # | Chart Type | What It Shows |
|---|---|---|
| Chart 1 | Box Plot (3 panels) | Score distribution by parental education level |
| Chart 2 | Grouped Bar | Test prep completed vs not — across all 3 subjects |
| Chart 3 | Correlation Heatmap | Pearson r between all 3 subjects |
| Chart 4 | Grouped Bar | Gender vs subject performance comparison |
| Chart 5 | Histogram | Total score distribution with mean, median, at-risk line |
| Chart 6 | Scatter Plot | Reading vs Math scores coloured by gender + trend line |
| At-Risk | Bar Chart | At-risk % broken down by parental education level |

All charts include titles, axis labels, and legends.

---

## ⚠️ At-Risk Student Segmentation

> **Definition:** A student is classified as **at-risk** if they score **below 50 in any one subject** (Math, Reading, or Writing).

### Overall Summary

| | Count | Percentage |
|---|---|---|
| **Total Students** | 1,000 | 100% |
| **At-Risk Students** | **188** | **18.8%** |
| Safe Students | 812 | 81.2% |

---

### By Parental Education

| Parental Education | At-Risk | Total | At-Risk % | Risk Level |
|---|---|---|---|---|
| some high school | 46 | 179 | **25.7%** | 🔴 High |
| high school | 49 | 196 | **25.0%** | 🔴 High |
| some college | 38 | 226 | 16.8% | 🟠 Medium |
| associate's degree | 33 | 222 | 14.9% | 🟠 Medium |
| bachelor's degree | 16 | 118 | 13.6% | 🟢 Low |
| master's degree | 6 | 59 | **10.2%** | 🟢 Low |

Students with parents who only completed high school have **2.5× the at-risk rate** of students whose parents hold a master's degree.

---

### By Gender

| Gender | At-Risk | Total | At-Risk % |
|---|---|---|---|
| Male | 99 | 482 | **20.5%** |
| Female | 89 | 518 | 17.2% |

---

### By Test Prep

| Test Prep | At-Risk | Total | At-Risk % |
|---|---|---|---|
| None | 152 | 642 | **23.7%** |
| Completed | 36 | 358 | **10.1%** |

Completing test prep **more than halves** the probability of being at-risk. Of the 188 at-risk students, **152 (80.9%)** did not complete test prep.

---

### By Lunch Type (Socioeconomic Indicator)

| Lunch Type | At-Risk | Total | At-Risk % |
|---|---|---|---|
| Free / Reduced | 111 | 355 | **31.3%** |
| Standard | 77 | 645 | **11.9%** |

Students on free/reduced lunch are **2.6× more likely to be at-risk** — the strongest single predictor of academic risk in the entire dataset.

---

## 📄 Principal's Report — Key Findings & Recommendations

### Finding 1 — Test Prep Has a Proven, Measurable Impact
Students who completed test prep scored +5.6 points higher in Math, +7.4 in Reading, and +9.9 in Writing. Yet only **358 of 1,000 students (35.8%)** completed it — leaving 64.2% of the student body without this proven academic advantage.

### Finding 2 — Parental Education Consistently Predicts Academic Performance
Writing shows the sharpest gap: 62.4 (high school parents) vs 75.7 (master's degree parents) — a **13.3-point difference**. Students from lower parental education backgrounds likely have less support at home, not less ability.

### Finding 3 — Reading and Writing Are Inseparably Linked (r = 0.955)
The near-perfect correlation means the school can address both verbal skills simultaneously with a single combined literacy program — maximising efficiency of resources.

### Finding 4 — Male Students Underperform in Verbal Subjects
Male students lead in Math (+5.1 pts) but fall behind in Reading (−7.1 pts) and Writing (−9.2 pts). Their at-risk rate (20.5%) is higher than females (17.2%).

### Finding 5 — Socioeconomic Status is the Strongest At-Risk Predictor
Students on free/reduced lunch have a 31.3% at-risk rate — **2.6× higher** than students on standard lunch (11.9%). This is the single strongest group-level predictor of academic risk, surpassing gender, parental education, and test prep status.

---

### ✅ 3 Actionable Recommendations

**Recommendation 1 — Make Test Prep Mandatory for All Students**
Test prep reduces at-risk rates from 23.7% to 10.1%. Making it compulsory and offering after-school/online sessions could reduce at-risk students from 188 to approximately 100 — a ~47% reduction.

**Recommendation 2 — Launch a Targeted At-Risk Intervention Program** *(Most Impactful)*
Identify all 188 at-risk students immediately. Assign each a dedicated faculty mentor. Run bi-weekly academic check-ins and subject-specific support. Prioritise students from low parental education backgrounds (25.7% at-risk) and free/reduced lunch households (31.3% at-risk).

**Recommendation 3 — Introduce a Reading & Writing Program for Male Students**
The 7.1-point reading gap and 9.2-point writing gap are systemic. A structured reading enrichment program — book clubs, paired reading, writing workshops — targeting male students can close this gap and reduce the overall male at-risk rate.

---

## 🚀 How to Run — Project 02

```bash
# Clone the repository
git clone https://github.com/laxman243ops/plutoProject2-Student-performance.git
cd plutoProject2-Student-performance

# Install dependencies
pip install pandas matplotlib seaborn numpy

# Run the analysis
python project02_student.py
```

> Or open in [Google Colab](https://colab.research.google.com) — the script includes an automatic file upload prompt.

---

## 📁 Output Files — Project 02

```
project02_outputs/
├── chart1_parental_education_boxplot.png
├── chart2_test_prep_comparison.png
├── chart3_correlation_heatmap.png
├── chart4_gender_subject.png
├── chart5_total_score_histogram.png
├── chart6_scatter_reading_math.png
└── at_risk_segmentation.png
```

---

## 👤 About the Intern

| Field | Details |
|---|---|
| **Name** | Laxman |
| **Program** | Pluto Academy — Data Analytics Internship 2026 |
| **GitHub** | [laxman243ops](https://github.com/laxman243ops) |
| **Platform** | [plutoacademy.in](https://plutoacademy.in) |

---

*Pluto Academy Data Analytics Internship 2026 · plutoacademy.in*
