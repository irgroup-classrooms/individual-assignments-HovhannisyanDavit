# Data Cleaning and Analysis Documentation

## Cleaning Steps
1. Loaded the dataset `lotr_characters.csv`.
2. Inspected the dataset for missing or inconsistent data.
3. Removed rows with missing values in critical columns: `birth`, `death`, `gender`, `name`, `race`.
4. Standardized the `name` column by stripping whitespace and converting to title case.
5. Cleaned other columns (`birth`, `death`, `gender`, `race`, `realm`, `spouse`) by removing non-alphanumeric characters and leading/trailing whitespace.
6. Saved the cleaned dataset as `lotr_characters_cleaned.csv`.

## Analysis Results
### Total Rows in Dataset
- 548

### Total Unique Names
- 548

### Gender Distribution
gender
Male                469
Female               76
Males                 1
Most likely male      1
male                  1

### Top 5 Most Common Races
race
Men        316
Hobbits     83
Elves       49
Dwarves     34
Ainur       21

