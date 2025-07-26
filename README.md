# GenAI-job-simulation-(bcg-x-project-of-data-analysis)-
The objective of this project is to manually extract financial data from 10-K filings of three major companies and analyze this data using Python and pandas in a Jupyter Notebook. 

## 📝 Project Overview

This project involved extracting and analyzing financial data from the 10-K filings of **Microsoft**, **Tesla**, and **Apple** over the last three fiscal years. The goal was to identify key financial trends and insights that could support the development of an **AI-powered financial chatbot**.

---

## ✅ Task Instructions

### 🔍 Step 1: Data Extraction

1. **Source:**
   Navigate to the [SEC EDGAR Database](https://www.sec.gov/edgar/searchedgar/companysearch.html)

2. **Manual Extraction:**
   For each company (Microsoft, Tesla, Apple), retrieve the last **three years of 10-K filings** and extract the following financial figures:

   * Total Revenue
   * Net Income
   * Total Assets
   * Total Liabilities
   * Cash Flow from Operating Activities

3. **Organize Data:**
   Compile the extracted figures into an **Excel spreadsheet** for easy use during analysis.

---

### 💻 Step 2: Jupyter Notebook Setup

1. **Install Jupyter Notebook (if not installed):**

   ```bash
   pip install notebook
   ```

2. **Launch Jupyter Notebook:**

   ```bash
   jupyter notebook
   ```

3. **Create a New Notebook:**
   Inside Jupyter, start a new Python notebook to conduct your analysis.

---

### 🧮 Step 3: Python Analysis

1. **Import pandas:**

   ```python
   import pandas as pd
   ```

2. **Load the CSV Data:**
   Convert your Excel file to `.csv`, then read it into a DataFrame:

   ```python
   df = pd.read_csv('path_to_your_csv_file.csv')
   ```

3. **Analyze Year-over-Year Trends:**
   Use pandas to calculate the percentage change for key metrics:

   ```python
   df['Revenue Growth (%)'] = df.groupby('Company')['Total Revenue'].pct_change() * 100
   df['Net Income Growth (%)'] = df.groupby('Company')['Net Income'].pct_change() * 100
   ```

4. **Explore Further:**

   * Use `.groupby()`, `.mean()`, `.sum()`, etc., to aggregate and compare financials.
   * Visualize trends or distributions if needed.

---

### 🧾 Step 4: Documentation & Submission

1. **Document in Markdown:**
   Use markdown cells within the notebook to:

   * Explain your methodology
   * Highlight key insights and trends
   * Summarize findings

2. **Export Your Notebook:**
   Once complete, export your notebook for submission:

   * `File → Download as → PDF` or `HTML`

---

## 🎯 Outcome

By the end of this project, you will have:

* Practiced manual financial data extraction
* Used Python and pandas for trend analysis
* Created a clear and well-documented notebook for stakeholder presentation or integration into an AI chatbot pipeline

---

