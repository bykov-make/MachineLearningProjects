# Data Preprocessing Toolkit 🔧📊

A comprehensive data preprocessing pipeline demonstrating essential data cleaning and preparation techniques for machine learning.

## ✨ Features

- **Complete Data Pipeline**: End-to-end data preprocessing workflow
- **Missing Value Handling**: Intelligent imputation strategies
- **Categorical Encoding**: One-hot and label encoding for different variable types
- **Dataset Splitting**: Proper train-test separation
- **Feature Scaling**: Standardization for model performance
- **Google Colab Integration**: Cloud-based execution support

## 🛠️ Processing Pipeline

### 1. **Data Import & Exploration**
```python
# Load dataset and separate features/target
dataset = pd.read_csv('Data.csv')
X = dataset.iloc[:, :-1].values  # Features
y = dataset.iloc[:, -1].values   # Target variable
```

### 2. **Missing Data Imputation**
- Uses `SimpleImputer` with mean strategy
- Handles NaN values in numerical columns
- Preserves data structure while filling gaps

### 3. **Categorical Data Encoding**
- **Independent Variables**: One-hot encoding for categorical features
- **Dependent Variables**: Label encoding for target classification
- Maintains data integrity through `ColumnTransformer`

### 4. **Dataset Splitting**
- 80-20 train-test split
- Random state for reproducibility
- Proper separation before feature scaling

### 5. **Feature Scaling**
- StandardScaler for normalization
- Applied only to numerical features
- Prevents feature domination in models

## 🚀 Quick Start

### Prerequisites
```bash
pip install numpy matplotlib pandas scikit-learn
```

### Running the Pipeline
1. Place your `Data.csv` file in the working directory
2. Run the script sequentially
3. For Google Colab: Mount drive and adjust file paths

### Google Colab Setup
```python
from google.colab import drive
drive.mount('/content/drive')
# Update file path to your dataset location
```

## 📊 Input/Output Examples

**Original Data:**
```
Country   Age   Salary   Purchased
France    44    72000    No
Spain     27    48000    Yes
Germany   30    54000    No
```

**Processed Features (X):**
```
[[1.0 0.0 0.0 44 72000]
 [0.0 0.0 1.0 27 48000]
 [0.0 1.0 0.0 30 54000]]
```

**Processed Target (y):**
```
[0 1 0]  # No=0, Yes=1
```

## 🎯 Use Cases

- **Machine Learning Preparation**: Clean data for model training
- **Data Analysis**: Standardized preprocessing for analytics
- **Educational Tool**: Learn data preprocessing fundamentals
- **Template Pipeline**: Adaptable code for different datasets

## 💡 Key Techniques Demonstrated

| Step | Technique | Library | Purpose |
|------|-----------|---------|---------|
| Data Loading | Pandas I/O | `pandas` | Read CSV files |
| Missing Values | Mean Imputation | `sklearn.impute` | Handle NaN values |
| Categorical Encoding | One-Hot & Label | `sklearn.preprocessing` | Convert text to numbers |
| Data Splitting | Train-Test Split | `sklearn.model_selection` | Model evaluation preparation |
| Feature Scaling | Standardization | `sklearn.preprocessing` | Normalize numerical features |

## 🔧 Customization

### For Your Dataset:
1. Update file path in `pd.read_csv()`
2. Adjust column indices in `iloc` statements
3. Modify categorical column indices in `ColumnTransformer`
4. Change test size in `train_test_split`

### Adding New Preprocessing:
- Outlier detection
- Feature engineering
- Dimensionality reduction
- Data validation

## 📈 Output Verification

The script includes `print()` statements at each stage to:
- Verify data loading
- Check missing value treatment
- Confirm encoding results
- Validate train-test splits
- Monitor scaling transformations

## 🎓 Learning Objectives

This project demonstrates:
- **Data Cleaning**: Handling real-world dataset imperfections
- **Preprocessing Pipeline**: Sequential data transformation steps
- **sklearn Integration**: Using scikit-learn preprocessing tools
- **Best Practices**: Proper order of operations in ML workflows
- **Debugging**: Verification at each processing stage

---

**💡 Pro Tip**: Use this as a template for any machine learning project! The modular structure makes it easy to adapt to different datasets and preprocessing requirements.

*Building better models starts with cleaner data!* 🚀
