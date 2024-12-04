# **Sales Dashboard Project**

## **Overview**
This project involves creating a Power BI dashboard to analyze sales data, providing key insights such as total sales, profit, customer performance, and regional trends. The data was cleaned, transformed, and visualized using **Power Query** and **Power BI**.

---

## **Key Features**
- **KPIs**: Total Sales, Cost, Profit.
- **Filters**: Date range, Ship mode, Region.
- **Visualizations**:
  - Map showing sales by city.
  - Bar chart for sales by sub-category.
  - Pie chart for quantity sold by region.
  - Line chart for orders by quantity and ship mode.
  - Table showing top customers by sales, cost, and profit.
- **Interactivity**: Slicers and drill-through filters to enhance analysis.

---

## **Steps Involved**

### **1. Data Cleaning and Preparation**
The dataset was cleaned and transformed in **Power Query** using the following steps:
1. **Data Import**:
   - Loaded data from Excel/CSV files or a SQL database.
   - Imported tables such as `Orders`, `Sales`, and `Customers`.

2. **Remove Duplicates**:
   - Ensured no duplicate rows existed in any table.

3. **Handle Missing Data**:
   - Replaced null or missing values in critical columns (e.g., `Region`, `Sales`) or removed incomplete rows.

4. **Data Type Corrections**:
   - Converted `Order Date` to the date format.
   - Ensured numeric columns like `Sales`, `Cost`, and `Profit` were in decimal format.

5. **Calculated Columns**:
   - Added new columns:
     - **Profit Margin** = `Profit / Sales`.
     - Extracted `Year` and `Month` from `Order Date`.

6. **Column Renaming**:
   - Renamed columns for better readability (e.g., `billing_country` to `Country`).

7. **Data Merging**:
   - Joined tables (e.g., `Orders` with `Customers`) to create a unified dataset.

---

### **2. Dashboard Creation**
1. **KPIs**:
   - Created card visuals to display total **Sales**, **Cost**, and **Profit**.

2. **Filters**:
   - Added slicers for:
     - Date range (`Order Date`).
     - Ship mode.
     - Regions.

3. **Visualizations**:
   - **Map**: Sales by city.
   - **Bar Chart**: Count of sales by sub-category.
   - **Pie Chart**: Quantity sold by region.
   - **Line Chart**: Total orders by quantity and ship mode.
   - **Table**: Top customers by sales, cost, and profit.

4. **Interactivity**:
   - Linked slicers to filter data across all visuals.
   - Enabled drill-through filters for detailed analysis of specific regions or sub-categories.

5. **Design and Formatting**:
   - Used a consistent purple theme for visuals.
   - Added tooltips, titles, and data labels to improve clarity.

---

## **Tools Used**
- **Power Query**: For data cleaning and transformation.
- **Power BI**: For data visualization and dashboard creation.

---

## **Project Folder Structure**
```
/SalesDashboardProject
├── Data/
│   ├── Orders.csv
│   ├── Sales.csv
│   ├── Customers.csv
├── Dashboard/
│   ├── SalesDashboard.pbix
│   ├── Screenshots/
│       ├── Dashboard.png
├── README.md
```

---

## **How to Use**
1. Clone the repository:
   ```bash
   git clone https://github.com/pranavp48/SalesDashboardProject.git
   ```
2. Open the `SalesDashboard.pbix` file in Power BI Desktop.
3. Adjust the dataset path in Power Query if using local files.
4. Publish the dashboard to Power BI Service for sharing.

---

## **Data Cleaning and Organization Steps**

### **Step 1: Data Import**
- Import data files into Power BI using **Get Data**.
- Load tables like `Orders`, `Sales`, and `Customers`.

### **Step 2: Remove Unnecessary Columns**
- Remove irrelevant columns such as `Order Notes` or `Unused IDs` to improve performance.

### **Step 3: Handle Duplicates**
- Remove duplicate rows in Power Query:
  - Go to **Home > Remove Duplicates**.

### **Step 4: Handle Missing Data**
- Use **Transform > Replace Values** or **Remove Rows** for handling missing values:
  - Replace null values in `Region` with "Unknown".
  - Remove rows with null `Sales` values.

### **Step 5: Format Data Types**
- Convert:
  - Dates (`Order Date`) to the **Date** format.
  - Numeric values (e.g., `Sales`, `Profit`) to **Decimal**.

### **Step 6: Create Calculated Columns**
- Use DAX to add custom metrics:
  - Profit Margin:
    ```DAX
    Profit Margin = DIVIDE([Profit], [Sales])
    ```

### **Step 7: Merge and Append Tables**
- Use **Merge Queries** to combine tables (e.g., join `Orders` and `Customers` on `Customer ID`).
- Use **Append Queries** to stack data (if working with multiple datasets).

### **Step 8: Sort and Filter Data**
- Sort rows by:
  - `Order Date` for chronological analysis.
  - `Sales` to highlight top transactions.
- Filter out irrelevant rows (e.g., `Order Status = Canceled`).

### **Step 9: Add Relationships**
- Define relationships between tables in the Power BI **Model View**:
  - Link `Orders` with `Customers` using `Customer ID`.
  - Link `Orders` with `Sales` using `Order ID`.

---

## **Future Enhancements**
- Add predictive analysis using Power BI's AI visuals.
- Integrate live data sources for real-time insights.
- Add region-specific drill-through pages.

---

## **Contributors**
- **Your Name** - [GitHub Profile](https://github.com/pranavp48)

