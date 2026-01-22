# Python-Basics-Reading-Data-Simple-Cleaning-Pandas-

## Data Cleaning Summary – Titanic Dataset

The following data cleaning steps were applied to prepare the dataset for analysis and modeling:

### 1. Missing Value Identification
Missing values were identified using `.isnull().sum()` to determine which columns required cleaning.

### 2. Handling Missing Values
Using the null function creating the using .isnull().sum() and making the changes to the values. 
- **Age:** Missing values were filled using the median (and group-wise median based on Pclass and Sex) to avoid distortion from outliers.
- **Embarked:** Missing categorical values were filled using the mode (most frequent value).
- **Cabin:** The column was dropped due to excessive missing values, making it unreliable for modeling.

### 3. Removing Duplicate Records
- Duplicate rows were checked and removed using `.drop_duplicates()` to ensure data quality and prevent biased learning.

### 4. Datatype Conversion
- Converted columns like `Survived`, `Pclass`, and `Sex` into appropriate datatypes using `.astype()` to enable correct calculations and efficient memory usage.

### 5. Creating New Columns (Titanic Dataset)
- Created new features such as `AgeGroup`, `FareBand`, `FamilySize`, and `IsAlone` to improve data interpretability and enhance predictive modeling performance.

### 6. Final Dataset Saving
- The cleaned and transformed dataset was saved using `.to_csv()` for reproducibility and further analysis.

**Conclusion:**  
These preprocessing steps improved data quality, reduced noise, and prepared the dataset for accurate analysis and machine learning modeling.

