# Wine Quality Classifier

Predicts wine quality scores from physicochemical properties using the UCI **Wine Quality** dataset (red and white wines combined).

## Approach

1. **Data preparation:** merged the red and white wine datasets, added wine type, checked for missing values
2. **Exploratory analysis:** distributions and relationships between quality and alcohol, density, pH, acidity and sulphur dioxide; correlation matrix
3. **Modelling:** train/test split with standard scaling, then compared four classifiers, tuning hyperparameters with `GridSearchCV`
4. **Evaluation:** accuracy, precision, recall, classification reports and confusion matrices

## Results

| Model | Test accuracy |
| :--- | :---: |
| Logistic Regression | 0.537 |
| Decision Tree | 0.595 |
| Gradient Boosting | 0.585 |
| **Random Forest** | **0.669** |

Random Forest performed best. Rare quality scores (for example 3 and 4) were hard to predict because they have very few samples, which is a clear direction for improvement (class rebalancing or grouping scores into low / medium / high).

## Files

| File | Description |
| :--- | :--- |
| `Wine Quality.ipynb` | Analysis and modelling notebook |
| `winequality-red.csv`, `winequality-white.csv` | Source data |

## Tech stack

`Python` · `pandas` · `scikit-learn` · `Matplotlib` · `Seaborn`

> Notebook section headings are in Turkish.
