# Crypto Clustering Analysis
This project performs a clustering analysis on cryptocurrency data to identify patterns and groupings using K-Means clustering. It utilizes data about various cryptocurrencies, including price changes and other metrics, and applies dimensionality reduction techniques like PCA to optimize clustering. The project uses the `crypto_market_data.csv` file to cluster cryptocurrencies based on several key features, with the clustering process evaluated using the elbow method to determine the optimal number of clusters (`k`). The data is then scaled, and PCA is applied to reduce the dimensions, allowing for further analysis and comparison of clustering results.
the dimensions, allowing for further analysis and comparison of clustering results.

## 📂 Folder Structure
```plaintext
/
├── Crypto_Clustering.ipynb          # Jupyter Notebook containing the clustering analysis
└── Resources/
    └── crypto_market_data.csv       # Dataset containing cryptocurrency data

```

## 🛠️ Dependencies
- pandas
- hvplot
- scikit-learn


## 📝 Project Flow

### 1. Data Loading and Preprocessing
The cryptocurrency data is loaded from `crypto_market_data.csv`. The data is then normalized using `StandardScaler` from `scikit-learn` to ensure consistency and improve clustering performance.

### 2. Elbow Method for Optimal Clusters
The elbow method is employed to determine the optimal number of clusters (`k`) for K-Means clustering. By visualizing the inertia values for different values of `k`, this method helps us identify the point at which increasing the number of clusters no longer significantly reduces inertia, indicating the best `k` for clustering.

### 3. K-Means Clustering
K-Means clustering is applied to the scaled data to group the cryptocurrencies into clusters based on features such as price changes and other metrics. The best `k` value identified in the previous step is used to perform the clustering.

### 4. Dimensionality Reduction (PCA)
Principal Component Analysis (PCA) is applied to reduce the number of features in the dataset to three principal components. This dimensionality reduction helps to simplify the dataset while retaining the most important information. The clustering process is then repeated using the PCA-reduced data for comparison.

### 5. Visualization
- **Elbow Curve Comparison:** The inertia values for both the original scaled data and the PCA-reduced data are plotted on an elbow curve to visually compare and identify the optimal `k` value.
- **Scatter Plots:** Scatter plots are generated to visualize the clusters formed using both the original scaled data and the PCA-reduced data. Hover functionality is added to the scatter plots, allowing users to identify each cryptocurrency within its respective cluster.


## 💻 How to Use
Ensure that you have access to the technologies mentioned above.

To get started with this project locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/crypto-clustering.git
   ```
2. Navigate to the project directory:
   ```bash
   cd crypto-clustering
   ```
3. Open the Jupyter Notebook and run it:
   ```bash
   jupyter notebook Crypto_Clustering.ipynb
   ```

