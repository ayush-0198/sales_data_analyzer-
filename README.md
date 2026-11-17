# Sales Data Analyzer

A Python console application to analyze sales transaction data from CSV files using Pandas and Matplotlib.

> **Course Project:** BCA 3rd Semester — Python Lab (Problem Statement No. 9)

---

## About the Project

This project processes retail sales records from a CSV file (`sales.csv`), handles data cleaning, and computes key sales metrics using **Pandas**. It also provides visual graphs using **Matplotlib**.

The application runs directly in the terminal through an interactive menu and includes:
- Data validation to skip corrupted records (e.g. non-numeric amounts) and remove duplicate entries.
- Calculations for total revenue, total transactions, and total units sold.
- Multi-dimensional grouping by Product and Region using `groupby()`.
- Identification of the top 5 best-selling products.
- Export of a Region-wise Sales Bar Chart and a Daily Sales Trend Line Chart.

---

## Dataset Format

The program processes a CSV file (`sales.csv`) with the following column structure:
- **Date**: Transaction date (`YYYY-MM-DD`)
- **Product**: Item name (e.g. `Laptop`, `Mouse`)
- **Region**: Sales region (`North`, `South`, `East`, `West`)
- **Quantity**: Units sold (integer)
- **Amount**: Total transaction value in INR (numeric)

---

## Requirements & Setup

Make sure you have Python 3 installed, along with the required libraries:

```bash
pip install pandas matplotlib
