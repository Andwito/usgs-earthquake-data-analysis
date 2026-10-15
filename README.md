# USGS Earthquake Data Analysis & Visualization

An academic Python data-analysis project using earthquake records from the **U.S. Geological Survey (USGS) Earthquake Catalog API**. The project explores trends and relationships in earthquake measurements and uses regression models to estimate an earthquake's USGS significance score.

## Project overview

- **Data source:** [USGS Earthquake Catalog API](https://earthquake.usgs.gov/fdsnws/event/1/)
- **Query period:** January 1 to February 1, 2026
- **Filter:** Minimum magnitude 4.0
- **Dataset size:** 1,248 earthquake records in the original analysis (API results may be revised over time)
- **Main tools:** Python, Requests, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn

## What the project does

1. Requests GeoJSON earthquake data from the USGS API and converts it into a Pandas DataFrame.
2. Cleans and transforms fields, including coordinates, timestamps, and missing values.
3. Explores distributions, outliers, correlations, and relationships between earthquake variables through visualizations.
4. Trains and evaluates individual-variable and multivariable linear regression models using a 70/30 train/test split.
5. Reports model metrics (R² and RMSE) and produces a dataset summary.

**Reported result from the original project:** The multivariable linear regression achieved a test R² of **0.9234** and RMSE of **17.6863** when predicting the USGS earthquake significance score. This is a result on one train/test split, not a claim of real-world forecasting accuracy.

## Run the project

Use Python 3. Install the dependencies:

```bash
pip install -r requirements.txt
```

Run the script:

```bash
python usgs_earthquake_data_analysis.py
```

An internet connection is required to retrieve records from the USGS API. The analysis and generated outputs depend on the data returned by the API.

## Outputs

The script saves the following files in the directory where you run it:

- `Yi_distributions.png` — variable distribution plots
- `Yi_boxplot.png` — significance-score box plot
- `Yi_correlation.png` — correlation heatmap
- `Yi_relationships.png` — variable relationship plots
- `Yi_multivariate.png` — actual-versus-predicted scatter plot
- `Yi_stats.txt` — descriptive statistics and project findings

After running the script, you can move selected PNG files into the `visualizations/` folder to display them in this repository.

## Notes

This is an **academic analysis**, not a live earthquake warning or forecasting system. The source data and USGS significance score are provided by USGS; the project uses those records to demonstrate data processing, visualization, and statistical modeling.
