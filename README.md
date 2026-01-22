# Optimizing-IT-Support-Team-Performance-Using-Analytics
# Cleaning + Dashboard

## 1) Problem Statement
The main goal of this project is to clean a raw customer call list dataset and prepare it for analysis and reporting.
The dataset contains customer contact details, but it has many issues like mixed phone number formats, unwanted symbols, and inconsistent Yes/No values.

After cleaning, a final call-ready dataset is created and used for visualization in Power BI.

---

## 2) Dataset Description
- File type: Excel (.xlsx)
- Dataset name: Customer Call List
- Raw file: `2_Data/raw/Customer Call List.xlsx`

The dataset contains the following columns:
- CustomerID
- First_Name
- Last_Name
- Phone_Number
- Address
- Paying Customer
- Do_Not_Contact

---

## 3) KPIs / Metrics Used
- Total Customers
- Total Paying Customers
- Total Do Not Contact Customers
- Total Contactable Customers
- Valid Phone Numbers Count
- Invalid / Missing Phone Numbers Count
- Duplicate Phone Numbers Count (removed in final call list)

---

## 4) Dashboard Details (Power BI)
The dashboard shows:
- Overall customer summary
- Paying vs Non-paying customers
- Contactable vs Do-not-contact customers
- Data quality issues (invalid phones / missing values)

## 5) Key Insights (From Data Cleaning)
1. Phone numbers were stored in different formats (example: `123-545-5421`, `123/643/9775`, `876|678|3469`).
2. Some name fields contained unwanted characters (example: `/White`).
3. The Yes/No columns had inconsistent values like `Yes`, `No`, `Y`, `N`, and blanks.
4. Some phone numbers were missing or invalid, so those rows were removed from the final call-ready list.

## 6) Recommendations (Optional)
1. The dataset should follow a standard input format while entering new customer data.
2. Phone numbers should always be stored in a fixed format (example: `123-456-7890`).
3. A simple ETL process can be followed for future updates:
   - Extract: Load raw Excel file
   - Transform: Clean the dataset using Python
   - Load: Export cleaned file for Power BI reporting

## 7) Tools Used
### Python
- pandas: Used to load, clean, and process the dataset.
- regex (re): Used to remove unwanted characters and format phone numbers.
- openpyxl: Used for reading and writing Excel files.

### Power BI
- Used to create dashboards and visualize KPIs.

### GitHub
- Used to organize and upload all project files, including code, data, and screenshots.
