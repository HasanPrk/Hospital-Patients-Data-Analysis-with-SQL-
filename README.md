# Hospital-Patients-Data-Analysis
Hospital patient data analysis with SQL Server — data cleaning, NULL handling, string &amp; date functions, and precise data filtering with T-SQL

This project is a hospital patient data analysis built with **SQL Server**.
Beyond query writing, this project covers something every real-world analyst needs: **Data Cleaning**. Before any analysis, you have to deal with NULL values and incomplete data — and that's exactly what I practiced here.

---

##  Business Context

The dataset contains patient records from a hospital: demographic details (gender, birth date, city, province), medical info (allergies), and physical measurements (height, weight).

The goal was to answer operational questions like:

- How many male patients do we have, and what are their details?
- Which patients have no recorded allergies?
- Which patients fall within a specific weight range? (e.g., for nutrition programs)

---

##  Database Structure

The main table in this project is `patients`:

| Column | Description |
|---|---|
| `patient_id` | Patient identifier |
| `first_name`, `last_name` | Name & surname |
| `gender` | Gender |
| `birth_date` | Date of birth |
| `city`, `province_id` | City & province |
| `allergies` | Allergies (can be NULL) |
| `height`, `weight` | Height & weight |

---

##  Business Questions Answered

| # | Question | Technique |
|---|---|---|
| 1 | Male patients with their names and gender? | `WHERE` + `ORDER BY` |
| 2 | Patients with no recorded allergies? | `IS NULL` |
| 3 | Patients whose name starts with 'C'? | `LIKE 'C%'` |
| 4 | Replace NULL allergy values with 'NKA'? | `ISNULL` |
| 5 | Patients weighing between 100 and 120? | `BETWEEN` |
| 6 | Combine first & last name into one column? | `CONCAT` |
| 7 | Count of patients born in 2010? | `YEAR()` + `COUNT` |
| 8 | Full records for specific patient IDs? | `IN` |
| 9 | Patients taller than 160 and heavier than 70? | Compound conditions with `AND` |

---

##  Skills & Techniques Used

-  Filtering data with a variety of operators: `=`, `IS NULL`, `BETWEEN`, `IN`, `LIKE`
-  Data cleaning: handling NULL values with the `ISNULL` function
-  String functions like `CONCAT` to create new derived columns (e.g., Full Name)
-  Date functions like `YEAR()` for year-based analysis
-  Sorting results with `ORDER BY` and using readable column aliases
-  Combining multiple conditions with `AND` for precise filtering

---

##  The Point of This Project: Raw Data ≠ Analysis-Ready Data

In Question 4, I replaced the NULL values in the `allergies` column with `'NKA'` (No Known Allergies):

```sql
-- Clean incomplete data before analyzing
SELECT
    first_name AS 'First Name',
    ISNULL(allergies, 'NKA') AS 'Allergies'
FROM patients;
```

Why does this matter? If NULLs are left unhandled, later reports (like counting patients without allergies) become misleading. A data analyst doesn't just write queries — they also care about **data quality**.

---

## 🗂️ Repository Structure

```                   
 ┣ report/
 ┃ ┗ Hospital Patients Data Analysis.pdf
 ┣ Queries-And-Outputs.md 
 ┗ README.md
```

---


## 📬 How to  Contact!

-  **Data Analyst:** Mohammadhasan Pourkabgani
-  **LinkedIn** — [MohammadHasan Pourkabgani](https://www.linkedin.com/in/mohammadhasan-pourkabgani/)
-  **GitHub** — [Hasanprk](https://github.com/Hasanprk)
-  **Email** — mh.pourkabgani91@gmail.com

If you found this project useful or have any feedback, I'd genuinely love to hear it! 
