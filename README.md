# Employees_tableau

Explore 300 employees across five Indian cities: pay by city and department, remote work, performance ratings, and salary vs age. Pay differs about 8% between the highest and lowest cities, and age has almost no relationship with salary.

# Employee Compensation & Workforce Dashboard (Tableau)

**Live interactive dashboard:** [https://public.tableau.com/app/profile/tanatswa.chiwara/viz/EmployeeCompensationWorkforce/EmployeeCompensationWorkforceDashboard?publish=yes]

## Overview
An interactive Tableau dashboard of 300 employees across five Indian cities, 
covering pay by city and department, remote work, performance ratings, and the 
relationship between age and salary.

## Business Questions
1. Where are employees located, and does pay differ by city?
2. Which departments pay the most and least?
3. How many employees work remotely?
4. How are performance ratings distributed?
5. Does pay increase with age?

## Dataset
Employee dataset (`Employees_raw_data.csv`), 308 rows and 8 columns: name, 
department, join date, salary, age, performance rating, city, and remote work status. 
Salary currency is not specified in the source.

## Data Cleaning
- Removed 8 exact duplicate rows (308 to 300 employees).
- Standardized department names (e.g. ENGINEERING and Engineering became Engineering).
- Standardized remote work to Yes/No (e.g. yes, YES, and Yes became Yes).
- Converted join date from a timestamp to a plain date.
- Left genuinely missing values blank instead of guessing: 13 departments, 26 remote 
  work values, 15 salaries, 10 ages, and 16 ratings. Tableau leaves these out of the 
  charts that use them.

## Dashboard Views
| View | Question answered |
|---|---|
| Salary & Headcount by City | Where staff are based and how pay compares |
| Salary by Department | Which departments pay the most |
| Remote Work Split | Share of remote vs on-site staff |
| Performance Rating Distribution | How ratings are spread |
| Salary vs Age | Whether pay rises with age |

## Key Findings
- **Pune has the most employees (74)** and Mumbai the fewest (50), but **Mumbai pays 
  the most** (average 61,936) and **Delhi the least** (57,305), an 8% gap.
- **Sales pays the least** (average 56,722) despite being the second-largest team 
  (83 people). HR pays the most (61,699), a gap of about 9%.
- **More employees work on-site than remotely:** 151 (55%) vs 123 (45%), among the 
  274 with a recorded status.
- **Ratings skew positive.** Of 284 rated employees, 59.5% received a 4 or 5 and only 
  15.8% received a 1 or 2. A rating of 4 was the most common (39.4%).
- **Age has almost no relationship with salary** (correlation 0.05), so pay in this 
  data isn't explained by age.

## Recommendations
- **Check whether Sales pay is competitive** before concluding it is low, since the 
  department's role mix isn't in this data. It is the second-largest team and the 
  lowest paid.
- **Check the Mumbai-Delhi pay gap against cost of living and role mix** before 
  making any adjustment.
- **Review how ratings are calibrated.** When 60% of ratings are 4 or 5, it becomes 
  harder to tell strong performers apart.
- **Look at factors beyond age to explain pay,** such as role, tenure, and 
  department. Age alone does not.
- **Record remote work status consistently.** 26 employees (9%) have none.
- **Fix missing data at the source** (departments, salaries, ages, ratings).

## Limitations
- Small dataset (300 employees), likely anonymized or synthetic.
- Missing values are excluded from the charts that use them, so the figures cover 
  only employees with recorded data.
- One salary (about 1.7K) is far below all others (the next lowest is about 18.6K). 
  I left it unchanged, and it has minimal effect on the averages.
- Findings are correlations, not causes.

## Tools Used
Tableau Public
