#  Task 1 - Data Cleaning & Preprocessing
# Titanic Dataset

Clean and preprocess the Titanic dataset to prepare it for machine learning. This includes:

- Handling missing values
- Encoding categorical variables
- Normalizing numerical features
- Removing outliers

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn

#  Steps Performed
1. **Loaded the dataset** using Pandas.
2. **Explored basic statistics** and checked for missing values.
3. **Imputed missing values** using:
   - Median for `Age`
   - Mode for `Embarked`
4. **Dropped irrelevant columns** like `Cabin`, `Name`, and `Ticket`.
5. **Encoded categorical columns**:
   - `Sex` mapped to 0 (male) and 1 (female)
   - One-hot encoding applied to `Embarked`
6. **Standardized** numerical features using `StandardScaler`.
7. **Visualized outliers** using boxplots for `Age` and `Fare`.


