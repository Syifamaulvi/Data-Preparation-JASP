# Data
There 77 row and 51 coloumn in the file. 
The columns include information such as gender, faed, maed, alg1, grades, mathach, ethnic, religion, competence, motivation, etc.

Many numeric values are still stored as strings with commas as decimals (e.g., 1,0 instead of 1.0). These need to be cleaned before processing.

## Data Cleaning
in this process we needs to replace commas , with dots . and convert to numeric data types, Remove irrelevant columns (e.g., No Data), Check for missing values and decide on a strategy (drop rows, impute with mean/median for numeric or mode for categorical).

## Data Cleaning in JASP

### Open your Dataset
- Open JASP → File → Open → select your CSV file
- Make sure the delimiter is set to Tab (TSV) if columns don’t look separated correctly.
heres the example:

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/6ddc5324-78fd-4ffc-86d6-a00bcc829faa" />

## Check for Missing Values
- Go to Descriptives → Descriptive Statistics.
- Drag important variables (e.g., gender, faed, maed, mathach, satm) into the analysis pane.
- Under “Statistics”, tick:
    N valid (number of valid cases)
    Missing values
- This shows which variables have missing data.

By using the six variables below, the number of missing data points for each variable was obtained.

  <img width="576" height="191" alt="image" src="https://github.com/user-attachments/assets/e1f3d583-5a48-47eb-aff5-3a2f4ce1a4ea" />

## Handle Missing Data
Options you can choose:
- Remove rows with too many missing values:
- Use the filter icon in the data grid to exclude rows where % Missing Data is above a threshold.

heres the threshold for missing data:
- There is no single agreed threshold for handling missing data. In general:
- Less than 5% → usually safe, multiple imputation (MI) offers little benefit.
- Around 5–10% → still analyzable, but imputation is recommended.
- More than 10% → analyses are prone to bias.
- More than 40% missing in key variables → results should be treated as exploratory or hypothesis-generating only.
reference: https://doi.org/10.1016/j.jclinepi.2019.02.016 
