
# 📊 AI-Powered Financial Chatbot Data Analysis Report

## 🧾 Project Overview

The objective of this project is to manually extract financial data from 10-K filings of three major companies — **Apple**, **Tesla**, and **Microsoft** — and analyze this data using Python and pandas in a Jupyter Notebook. This analysis simulates a component of an AI-powered financial chatbot that can interpret financial reports and present key trends to users.

---

## 🧩 Project Tasks

### 🔍 Step 1: Data Extraction

- Navigate to the SEC's EDGAR database.
- Locate the **10-K filings** for the past **three fiscal years** of:
  - Apple
  - Tesla
  - Microsoft
- Manually extract the following financial figures:
  - Total Revenue
  - Net Income
  - Total Assets
  - Total Liabilities
  - Operating Cash Flow

### 📊 Step 2: Organize and Load the Data

- Store the extracted data in an **Excel** or **CSV** file.
- Convert it to a **pandas DataFrame**.
- Prepare the data for analysis.

### 📈 Step 3: Python Analysis in Jupyter Notebook

- Use **pandas** to calculate year-over-year percentage growth:
  - Revenue Growth
  - Net Income Growth
  - Asset Growth
  - Liabilities Growth
  - Operating Cash Flow Growth
- Use `groupby()` and `pct_change()` functions.
- Add new columns for each growth metric.
- Use **markdown cells** to describe trends and summarize findings.

### 📝 Step 4: Documentation and Export

- Use markdown to explain your analysis and conclusions.
- Export the notebook as **.ipynb**, **.py**, and **.pdf** or **.html** for submission.

---

## ✅ My Response (Code Summary)

```python
import pandas as pd

# Load the data
df = pd.read_csv('last_3_Years_Apple_Tesla.csv')
df.columns = df.columns.str.strip()
df['Year'] = df['Year'].astype(int)
df = df.sort_values(by=['Company', 'Year'])

# Convert string numbers with commas to proper float
for col in ['Total Revenue ($B)', 'Net Income ($B)', 'Total Assets ($B)', 'Total Liabilities ($B)', 'Operating Cash Flow ($B)']:
    df[col] = df[col].astype(str).str.replace(',', '.', regex=False)
    df[col] = pd.to_numeric(df[col])

# Calculate YoY growth
df['Revenue Growth (%)'] = df.groupby('Company')['Total Revenue ($B)'].pct_change() * 100
df['Net Income Growth (%)'] = df.groupby('Company')['Net Income ($B)'].pct_change() * 100
df['Asset Growth (%)'] = df.groupby('Company')['Total Assets ($B)'].pct_change() * 100
df['Liabilities Growth (%)'] = df.groupby('Company')['Total Liabilities ($B)'].pct_change() * 100
df['Cash Flow Growth (%)'] = df.groupby('Company')['Operating Cash Flow ($B)'].pct_change() * 100

# Display the final data
df.fillna(0, inplace=True)
print(df)
```

### 🧠 My Key Findings (Summarized in Markdown)

- **Apple** shows steady revenue and net income growth, especially in FY2021.
- **Tesla** experienced rapid growth, with high revenue increases, but some volatility in net income.
- **Microsoft** remains financially strong with consistent cash flows and solid margins.

---

## 📝 Suggested Sample Response (from project)

```python
import pandas as pd

# Load the data from the Excel spreadsheet
file_path = 'path_to_your_excel_file.xlsx'
df = pd.read_excel(file_path)

# Calculate year-over-year growth rates for Total Revenue and Net Income
df['Revenue Growth (%)'] = df.groupby('Company Name')['Total Revenue'].pct_change() * 100
df['Net Income Growth (%)'] = df.groupby('Company Name')['Net Income'].pct_change() * 100

# Fill NA values that result from pct_change calculations with 0 or an appropriate value
df.fillna(0, inplace=True)

# Display the dataframe to verify the calculations
print(df)

# Optionally, summarize findings
summary = df.groupby('Company Name').agg({
    'Revenue Growth (%)': 'mean',
    'Net Income Growth (%)': 'mean'
}).reset_index()

print("\nYear-over-Year Average Growth Rates (%):")
print(summary)
```

---

## 📦 Output Formats

- **Notebook File:** `Data_analysis.ipynb`
- **PDF Report:** `Data_analysis.pdf`
- **HTML Version:** `Data_analysis.html`
