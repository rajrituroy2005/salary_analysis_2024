# 📊 Salary Analysis 2024 — Data Analytics Project

## 📌 Overview
This project analyzes a dataset containing **16,534 salary records** from the year **2024**, covering different job titles, experience levels, employment types, locations, remote ratios, and company sizes.

The goal is to uncover insights such as:

- Which job titles earn the highest salaries  
- How salary changes with experience  
- Which locations pay the most  
- Whether employment type affects salary  
- Whether bigger companies pay more  

---

## 📁 Project Structure

salary_analysis_2024/
│
├── analysis.ipynb
├── README.md
├── salary_data.csv (optional)
└── images/
├── job_titles.png
├── experience_salary.png
├── location_salary.png
├── employment_type.png
└── company_size.png


---

## 🧹 Data Preparation

### ✔ Experience Level Mapping
EN → Entry-level
MI → Mid-level
SE → Senior-level
EX → Executive-level


### ✔ Employment Type Mapping

FT → Full-time
PT → Part-time
CT → Contract
FL → Freelance


### ✔ Company Size

S → Small
M → Medium
L → Large

### ✔ Cleaned Salary Column  
Converted to numeric for analysis.

---

# 📊 Analysis & Insights

---

## 1️⃣ Highest Paying Job Titles

### 🔎 Code
```python
df.groupby('job_title')['salary'].mean().sort_values(ascending=False).head(10)

📈 Visualization

📝 Insight

The highest-paying roles were in AI, Machine Learning, and Senior Data Engineering, with significantly higher average salaries.

##2️⃣ Salary vs Experience Level

###🔎 Code
df.groupby('experience_level')['salary'].mean()
📈 Visualization

📝 Insight

Salary increases consistently from Entry-level → Mid-level → Senior-level → Executive-level, showing a clear experience-to-salary growth pattern.
##3️⃣ Top Paying Locations

###🔎 Code
df.groupby('employee_residence')['salary'].mean().sort_values(ascending=False).head(10)
📈 Visualization

📝 Insight

Countries like Chile (CL), Hungary (HU), and Japan (JP) showed the highest average salaries in the dataset.
##4️⃣ Does Employment Type Affect Salary?

###🔎 Code
df.groupby('employment_type')['salary'].mean()

📈 Visualization

📝 Insight

Larger companies tend to offer higher salaries compared to medium and small companies, reflecting bigger budgets and stronger organizational structures.

##🏁 Conclusion
This analysis reveals clear patterns in 2024 salary data:

Job title strongly affects salary (AI & ML roles lead).

Experience level has a direct positive impact on salary.

Location plays a major role in compensation.

Employment type influences pay rates significantly.

Bigger companies generally pay higher salaries.

This makes the dataset extremely useful for career planning, salary benchmarking, and global compensation insights.
