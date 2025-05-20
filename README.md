# Diabetes Prediction Project

This project is a data mining analysis focused on predicting diabetes based on a dataset obtained from Kaggle. The project walks through all essential stages of a typical data mining workflow including data understanding, preprocessing, clustering, and classification.

## Dataset

* **Name**: `diabetes_prediction_dataset`
* **Source**: [Kaggle](https://www.kaggle.com/)

The dataset contains information such as age, gender, BMI, HbA1c level, blood glucose level, and whether or not a patient has diabetes.

---

## Exercise 1: Data Understanding

* First 5 rows of the dataset were displayed.
* Data types were identified.
* Summary statistics (five-number summary) were computed using `.describe()`.
* Box plots and histograms were plotted to detect skewness and outliers.
* QQ plots showed the normality of numerical features.
* Scatter plots revealed correlations between features (e.g., age and BMI).
* Line plots supported deeper understanding of relationships.

### Insight:

Visualizations helped in exploring potential feature interactions and understanding distributions.

---

## Exercise 2: Data Preprocessing

* Checked for missing values → None were found.
* Validated categorical values → No typos or inconsistencies.
* Removed 3854 duplicate rows.
* Dropped less important columns: `gender` and `smoking_history`.
* Normalized numeric columns using Min-Max and Z-score methods.
* Removed 9054 additional duplicates post-normalization.
* Final preprocessed dataset saved as `preprocessed_diabetes.csv`.

### Result:

* Columns reduced from 9 to 7.
* Rows reduced from 100,000 to 87,092.

---

## Exercise 3: Clustering

* Performed clustering using **K-Means** and **DBSCAN**.
* Visualized clusters using various feature pairs.
* Calculated **Silhouette Score** to evaluate clustering quality.

### Conclusion:

* K-Means worked better on pairs like `(age, bmi)` and `(HbA1c_level, age)`.
* DBSCAN performed better on `(bmi, blood_glucose_level)`.

---

## Exercise 4: Classification

* Target variable: `diabetes`.
* Split data: 80% training, 20% testing.
* Applied classifiers:

  * **Decision Tree**
  * **Naive Bayes**
* Evaluated using:

  * Confusion Matrix
  * Accuracy
  * Precision
  * Recall

### Result:

* Decision Tree achieved better Accuracy, Precision, and Recall compared to Naive Bayes.

---

## How to Run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Run the code in any Python environment (Jupyter Notebook or `.py` file).

---

## Author

This project was developed as a part of a data mining course to practice end-to-end data analysis and machine learning using real-world healthcare data.

Feel free to fork, clone, or contribute!
