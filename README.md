# Customer Segmentation

Grouping mall customers into segments based on annual income and spending score using K-Means clustering.

## Dataset
[Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) (Kaggle): 200 customers, 5 columns, no missing values.

## Approach
1. Explored the data and visualized income vs. spending score
2. Scaled the features with StandardScaler
3. Chose the number of clusters using the Elbow method and the Silhouette score
4. Trained K-Means with k = 5 and visualized the clusters in 2D
5. Bonus: analyzed the average income and spending per cluster, and compared K-Means with DBSCAN

## Results
Both the Elbow method and the Silhouette score (about 0.55) pointed to k = 5.

| Segment | Avg. Income (k$) | Avg. Spending Score |
|---|---|---|
| Mid income, mid spending | 55.3 | 49.5 |
| High income, high spending | 86.5 | 82.1 |
| Low income, high spending | 25.7 | 79.4 |
| High income, low spending | 88.2 | 17.1 |
| Low income, low spending | 26.3 | 20.9 |

## Key Findings
- Customers form 5 clear segments.
- High-income, high-spending customers are the most valuable group.
- High-income, low-spending customers are a good target for marketing campaigns.
- DBSCAN found 4 clusters and flagged some outliers, but it merged several groups, so K-Means gave cleaner segments on this data.

## Tech Stack
Python, Pandas, Matplotlib, Scikit-learn

## How to Run
1. Clone the repo
2. Install dependencies: `pip install pandas matplotlib scikit-learn`
3. Open `customer_segmentation.ipynb` in Jupyter or Google Colab and run all cells
