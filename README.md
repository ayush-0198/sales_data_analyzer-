# Sales Data Analyzer (Problem Statement No. 9)

**Bachelor of Computer Applications (BCA)**  
*Third Semester — Python Programming / Data Analytics Lab Project*

---

## 📌 Project Overview
**Sales Data Analyzer** is a Python 3 console-based analytics application designed to process retail sales transaction data from CSV files. It leverages **Pandas** for robust data cleaning, validation, and aggregations (`groupby()`), and **Matplotlib** for interactive visualization.

---

## 🚀 Key Features & Bare Minimum Requirements Satisfied
1. **Single `.py` Script:** Entire project solution is cleanly contained in `sales_analyzer.py` and executed directly from the terminal/console.
2. **Data Cleaning & Validation:**
   - Detects CSV headers automatically or handles headerless files.
   - Validates numeric columns (`Amount` and `Quantity`).
   - Identifies and skips invalid records (e.g. `Row 2 skipped: invalid Amount 'abc'`).
   - Cleans duplicate rows.
3. **Data Aggregations using `groupby()`:**
   - **Product-wise Total Sales**
   - **Region-wise Total Sales**
4. **Top 5 Best-Selling Products:**
   - Displays rank, product name, units sold, and total revenue.
5. **Data Visualizations (Matplotlib):**
   - **Bar Chart:** Region-wise sales comparison (`Region-wise Sales`).
   - **Line Chart:** Daily sales revenue trend over time (`Daily Sales Trend`).

---

## 📁 Repository Structure
```
sales_data_analyzer/
│
├── sales_analyzer.py                # Main Python application (single .py file)
├── sales.csv                        # Sales transaction dataset
│
├── region_wise_sales_bar_chart.png  # Generated Region-wise bar chart
├── sales_trend_line_chart.png       # Generated Sales trend line chart
├── README.md                        # Project documentation
└── PROJECT_REPORT.md                # Academic project report
```

---

## ⚙️ Installation & Prerequisites

1. **Python 3.8+**
2. Install required packages:
```bash
pip install pandas matplotlib
```

---

## 💻 How to Run

### Interactive Console Menu:
```bash
python sales_analyzer.py
```

### Menu Options:
```
==================================================
         SALES DATA ANALYZER (PS No: 9)
==================================================
1. Summary (Total Revenue, Transactions, Units)
2. Group by Product & Region (with Bar Chart)
3. Show Top 5 Best-Selling Products
4. Plot Sales Trend (Line Chart)
5. Load Different CSV File
6. Exit
==================================================
```

### Direct Command-Line Arguments (Optional):
```bash
# Run Option 1 (Summary) on a specific CSV
python sales_analyzer.py --csv sales.csv --option 1

# Run Option 2 (Product & Region Grouping)
python sales_analyzer.py --csv sales.csv --option 2

# Run Option 3 (Top 5 Best-Selling Products)
python sales_analyzer.py --csv sales.csv --option 3

# Run Option 4 (Sales Trend Line Chart)
python sales_analyzer.py --csv sales.csv --option 4
```

---

## 🧪 Test Cases Verification

Run the application using Python console:
```bash
python sales_analyzer.py
```

### Test Case Results:

| Test Case | Scenario | Expected Output | Status |
|:---|:---|:---|:---:|
| **Case 1** | Normal Input (Option 1) | `Total Revenue: 155000 \| Transactions: 3 \| Units sold: 13` | ✅ PASS |
| **Case 2** | Boundary / 1 Row (Option 1) | `Total Revenue: 500 \| Transactions: 1 \| Top product: Mouse` | ✅ PASS |
| **Case 3** | Invalid Input (`Amount='abc'`) | `Row 2 skipped: invalid Amount 'abc'`<br>`Total Revenue: 150000 \| Transactions: 2` | ✅ PASS |
| **Case 4** | Grouping & Chart (Option 2) | `Laptop: 150000 \| Mouse: 5000`<br>`North: 100000 \| South: 55000`<br>`Bar chart 'Region-wise Sales' displayed` | ✅ PASS |

---

## 📊 Visualizations
* **Bar Chart (`region_wise_sales_bar_chart.png`)**: Compares total sales revenue across North, South, East, and West regions.
* **Line Chart (`sales_trend_line_chart.png`)**: Illustrates chronological revenue performance over time.
