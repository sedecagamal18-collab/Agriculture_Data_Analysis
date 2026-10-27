# Agriculture Data Analysis | Python

## Project Overview
This project explores agricultural data from 50 farms using Python (Pandas, NumPy, Matplotlib, and Seaborn) to understand how factors such as crop type, farm area, irrigation method, soil type, fertilizer and pesticide usage, and season relate to crop yield and water consumption.

The main goal is to analyze agricultural patterns, identify relationships between farming practices and productivity, and generate insights that can support more efficient and sustainable farming.

## Dataset Description
The dataset (`agriculture_dataset.csv`) contains **50 farm records and 10 columns**. Each row represents one farm.

| Column | Description |
|---|---|
| Farm_ID | Unique farm identifier |
| Crop_Type | Type of crop grown (10 crops) |
| Farm_Area(acres) | Farm size in acres |
| Irrigation_Type | Irrigation method (Drip, Flood, Sprinkler, Rain-fed, Manual) |
| Fertilizer_Used(tons) | Fertilizer used, in tons |
| Pesticide_Used(kg) | Pesticide used, in kilograms |
| Yield(tons) | Crop yield, in tons |
| Soil_Type | Soil type (Clay, Loamy, Sandy, Silty, Peaty) |
| Season | Agricultural season (Kharif, Rabi, Zaid) |
| Water_Usage(cubic meters) | Water consumption, in cubic meters |

## Tools Used
- Python
- Pandas and NumPy (data handling and analysis)
- Matplotlib and Seaborn (data visualization)
- Jupyter Notebook

## Project Workflow

### 1. Data Understanding
- Reviewed the dataset structure, column names, data types, and shape.
- Generated summary statistics for both numerical and categorical columns.

### 2. Data Cleaning
- **Missing values:** none found.
- **Duplicates:** none found.
- **Outliers:** checked all numerical columns using the IQR method (values outside Q1 − 1.5×IQR and Q3 + 1.5×IQR are capped). No outliers were detected, so no values were changed.

### 3. Exploratory Data Analysis (EDA)
The notebook includes 12 analysis and visualization steps:

| # | Analysis | Visualization |
|---|---|---|
| 3.1 | Crop type distribution | Count plot |
| 3.2 | Distribution of water usage (mean and median) | KDE plot |
| 3.3 | Distribution of irrigation types | Count plot |
| 3.4 | Distribution of soil types | Count plot |
| 3.5 | Distribution of agricultural seasons | Count plot |
| 3.6 | Farm area vs. crop yield | Scatter plot |
| 3.7 | Crop yield by irrigation type | Box plot |
| 3.8 | Average crop yield by crop type | Bar chart |
| 3.9 | Water use efficiency by crop type (tons of yield per 1,000 m³ of water) | Bar chart |
| 3.10 | Water usage vs. crop yield | Scatter plot |
| 3.11 | Fertilizer usage vs. crop yield | Scatter plot |
| 3.12 | Correlation between numerical variables | Heatmap |

## Key Findings

- **Crop performance:** Carrot has the highest average yield (about 36.6 tons), followed by Tomato (33.6) and Soybean (32.3). Maize has the lowest (about 20.2 tons), followed by Cotton (21.0). The overall average yield is about 27.1 tons per farm.
- **Water efficiency:** Soybean is the most water-efficient crop (about 0.56 tons of yield per 1,000 m³ of water), followed closely by Wheat (0.55) and Rice (0.50). Cotton is the least efficient (about 0.40).
- **Irrigation methods:** Drip irrigation is the most widely used method (15 farms), followed by Flood (13), Sprinkler (9), Rain-fed (7), and Manual (6). Manual irrigation has the highest median yield (about 38.5 tons), while Flood has the lowest (about 16.0 tons).
- **Agricultural patterns:** Cotton and Barley are the most frequent crops (7 farms each), Clay is the most common soil type (14 farms), and Zaid is the most frequent season (23 of 50 farms).
- **Correlation analysis:** Farm area (0.15), water usage (0.11), fertilizer usage (0.05), and pesticide usage (−0.09) all show weak linear correlations with crop yield.

*Note: The findings describe this dataset of 50 farms and should not be interpreted as general agricultural facts beyond its scope.*

## Limitations
- The dataset is small (50 farms), and each crop has only 3 to 7 farms, so crop-level averages can change easily with a few records.
- The Manual irrigation group has only 6 farms, so its high median yield should be treated with caution.
- Correlations are weak and do not establish causation. No statistical significance tests were applied.

## Business Value

This project demonstrates how Python can be used to:

- Compare crop productivity and water use efficiency across crop types.
- Understand how irrigation methods, soil types, and seasons are distributed across farms.
- Test whether farm size and input usage (water, fertilizer, pesticide) are linked to yield.
- Support more efficient, resource-aware farming decisions.

## Skills Demonstrated

- Data Cleaning (missing values, duplicates, outliers)
- Exploratory Data Analysis (EDA)
- Data Visualization (Matplotlib, Seaborn)
- Correlation Analysis
- Feature Engineering (water use efficiency)
- Insight Communication

## How to Run

1. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
2. Place `agriculture_dataset.csv` in the same folder as the notebook.
3. Open `Agriculture_Data_Analyst.ipynb` in Jupyter Notebook and run all cells.

## Project Files

- `agriculture_dataset.csv` — Original dataset (50 farms, 10 columns).
- `Agriculture_Data_Analyst.ipynb` — Jupyter Notebook containing the full cleaning, analysis, and visualizations.

## Conclusion

This project demonstrates the use of Python to clean, explore, and visualize agricultural data, highlighting differences in crop productivity and water use efficiency across crop types.

However, the dataset is relatively small and the observed relationships do not establish causation. Further analysis using larger datasets and additional agricultural factors could provide deeper insights into crop productivity and resource management.
