# 🏢 Layoffs Data Cleaning Project  

## 📌 About  
This project focuses on cleaning and preprocessing the `layoffs.csv` dataset, which contains layoff data from various companies. The cleaning steps include removing duplicates, standardizing data, handling missing values, and ensuring consistency in the dataset.  

---

## 📂 Dataset  
- **File Name**: `layoffs.csv`  
- **Columns Included**:  
  - `company` - Name of the company  
  - `location` - Office location  
  - `industry` - Industry type  
  - `total_laid_off` - Number of employees laid off  
  - `percentage_laid_off` - Percentage of employees affected  
  - `date` - Layoff date  
  - `stage` - Company funding stage  
  - `country` - Country where layoffs happened  
  - `funds_raised_millions` - Amount raised by the company (in millions)  

---

## 🔍 Data Cleaning Steps  

### ✅ 1. Remove Duplicates  
Used `ROW_NUMBER()` to identify and remove duplicate records.  

### ✅ 2. Standardize Data  
- Trimmed leading and trailing spaces.  
- Fixed inconsistent values (e.g., `Crypto` vs `Cryptocurrency`).  
- Corrected country name formatting (`United States.` → `United States`).  

### ✅ 3. Convert Data Types  
- Converted `date` from `TEXT` to `DATE` format using `STR_TO_DATE()`.  

### ✅ 4. Handle NULL and Blank Values  
- Replaced empty `industry` values by inferring from other company records.  
- Deleted records where `total_laid_off` and `percentage_laid_off` were both `NULL`.  

### ✅ 5. Final Cleanup  
- Removed the extra `row_num` column used for duplicate removal.  

---

## ⚡ How to Use  
1️⃣ Run the SQL script `layoffs_data_cleaning.sql` in your MySQL environment.  
2️⃣ Verify that the cleaned data is stored in `layoffs_staging2`.  
3️⃣ Use the clean dataset for further analysis or visualization.  

---

## 📈 Key Insights  
After cleaning, the dataset is structured and reliable for further data analysis, helping to identify trends and patterns in corporate layoffs.  

---

## 👩‍💻 Author  
**Ghizlane ENNAH**  
Data Analyst | SQL Enthusiast | Business Intelligence Specialist  


