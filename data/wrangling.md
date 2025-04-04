## 1. Handling Missing Values

- For the **merged dataset** (CO2 emissions + World Energy Consumption), all missing values were filled with the placeholder **'Unknown'** to ensure consistency and prevent issues during analysis.
- The **energy dataset** had no significant missing values that required handling.

## 2. Removing Duplicates

- Duplicates were removed from all datasets:
    - **Energy Dataset**: Removed duplicates to ensure data integrity.
    - **CO2 Emissions Dataset**: Duplicate records were identified and removed.
    - **World Energy Consumption Dataset**: Duplicate rows were removed.

## 3. Standardizing Formats

- **Column Names**: Standardized to lowercase with underscores (e.g., `installed_capacity_mw`).
- **Date Formats**:
    - In the CO2 dataset, the `date` column was converted to a consistent **datetime** format.
    - Invalid dates were identified and the corresponding rows were removed.
- **Categorical Columns**:
    - In the **energy dataset**, numerical codes for categorical columns were mapped to meaningful labels:
        - `type_of_renewable_energy` (e.g., Solar, Wind, Geothermal, etc.).
        - `grid_integration_level` (e.g., Fully Integrated, Isolated Microgrid).
        - `funding_sources` (e.g., Government, Private, Public-Private Partnership).

## 4. Filtering Unnecessary Columns or Rows

- In the **World Energy Consumption Dataset**, columns with over **50% missing values** were removed to reduce noise and improve clarity.

## 5. Joining Multiple Datasets

- The **CO2 Emissions** and **World Energy Consumption** datasets were merged using the `country` column into a new **World Energy Consumption and CO2 Emissions Dataset**.
- The **energy dataset** was kept separate due to the lack of overlapping columns for a meaningful merge.

## 6. Aggregations

- No aggregations were performed during this phase as the focus was on data preparation and standardization.

## 7. Pivoting

- No pivoting was necessary at this stage. Future visualizations may involve pivoting or aggregating data as needed.