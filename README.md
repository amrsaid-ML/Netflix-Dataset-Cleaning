# Netflix Movies & TV Shows Data Cleaning Project

An end-to-end Python and Pandas project demonstrating real-world data cleaning, missing value imputation, type casting, and feature extraction on the Kaggle Netflix Movies and TV Shows dataset.

## 📌 Project Overview
Real-world datasets rarely arrive ready for modeling or dashboarding. The raw Netflix dataset contains missing values, mixed-type columns, misplaced data entries, and unparsed date strings.

This project focuses on making **deliberate, context-aware decisions** for every column rather than naively dropping missing data.

## 🛠️ Key Data Cleaning Steps Applied

1. **Missing Value Imputation**:
   - `director`, `cast`, `country`: High missing percentages (~30%, ~9%, ~9%). Imputed as `"Unknown"` to preserve valuable titles.
   - `rating`: Imputed missing values with `"Unavailable"`.
   - `date_added`: Dropped a negligible number of missing rows (~0.1%).

2. **Fixing Mixed-Type & Misplaced Data**:
   - Identified and fixed entries where duration values (e.g., `"74 min"`) were incorrectly placed under the `rating` column.
   - Extracted numerical durations (`duration_num`) and normalized duration unit types (`Minutes` vs. `Seasons`).

3. **Date Parsing & Feature Engineering**:
   - Parsed raw string dates (`"September 24, 2022"`) into native datetime objects.
   - Extracted dedicated features: `year_added`, `month_added` (name), and `month_added_num` (integer 1–12).

4. **Whitespace & String Sanitization**:
   - Stripped leading/trailing whitespaces and standard string representation artifacts.

## 📂 Repository Structure
```text
├── netflix_data_cleaning.ipynb   # Jupyter Notebook containing the code & step-by-step analysis
├── netflix_titles.csv            # Original raw dataset from Kaggle
├── netflix_titles_cleaned.csv    # Exported cleaned dataset
└── README.md                     # Project documentation
```

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/netflix-data-cleaning.git
   cd netflix-data-cleaning
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy jupyter
   ```

3. Launch Jupyter Notebook and run `netflix_data_cleaning.ipynb`:
   ```bash
   jupyter notebook netflix_data_cleaning.ipynb
   ```

## 📊 Technologies Used
- **Language**: Python 3.x
- **Data Manipulation**: Pandas, NumPy
- **Environment**: Jupyter Notebook

project URL: https://roadmap.sh/projects/cleaning-netflix-dataset
