# Data Science Pipeline: Retail Order Analysis

This project implements an advanced end-to-end Data Science pipeline for cleaning, analyzing, and engineering features from a retail dataset. The pipeline is designed to transform raw transaction data into a machine-learning-ready format, specifically optimized for predicting **Order Status**.

## 🚀 Features

- **Exploratory Data Analysis (EDA)**: Automated generation of distribution plots and correlation heatmaps.
- **Robust Data Cleaning**: 
    - Statistical imputation for missing values (Mean/Median/Mode).
    - Outlier neutralization using Winsorization (IQR-based clipping).
- **Advanced Feature Engineering**:
    - One-Hot Encoding for categorical variables.
    - Creation of derived features: `PricePerItem`, `LogTotalPrice`, and `CartEfficiency`.
- **Dimensionality Optimization**: Automated removal of highly collinear features to prevent model overfitting.
- **Data Validation**: Schema enforcement using `Pandera` to ensure data integrity.

## 📁 Project Structure

```text
├── data/
│   ├── dataset.csv            # Original dataset (Input)
│   └── clean_dataset.csv      # Processed dataset (Output)
├── plots/
│   ├── eda_distributions.png  # Numeric feature distributions
│   └── eda_correlation.png    # Feature correlation heatmap
├── src/
│   └── pipeline.py            # Main Python processing script
├── requirements.txt           # Project dependencies
└── README.md                  # Project documentation
```

## 🛠️ Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/retail-order-analysis.git
   cd retail-order-analysis
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the pipeline**:
   ```bash
   python src/pipeline.py
   ```

## 📊 Pipeline Results

The pipeline successfully processed the dataset with the following results:
- **Target Column**: `OrderStatus`
- **Feature Expansion**: Increased from original features to 23 clean, ML-ready features.
- **Outlier Treatment**: All numeric features neutralized via Winsorization.
- **Collinearity**: High-correlation features removed for model stability.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
