# Customer Segmentation for Online Retail

## Project Overview
This project focuses on a customer segmentation model for an online retail business using transactional purchase data. The objective is to identify the distinct customer groups based on purchasing behavior to support targeted marketing, customer retention strategies, and revenue optimization.

We summarize the customer behavior by using the RFM (Recency, Frequency, Monetary) Framework and segmented using K-means clustering. The final model identifies three meaningful customer segments that differ significantly in purchase recency, purchase frequency, and total spending.


## Dataset
- Source: Kaggle - Online Retail Data Set
- Size: 541,909 transactions
- Customers: 4,372 unique transactions

The dataset contains transaction-level purchase history including invoice numbers, product information, purchase quantity, price, transaction date, and customer identifiers.

## Methodology
The project followed a structured data science workflow:

### Data Preparation
- Data cleaning (duplicates, missing CustomerID removal)
- Removal of cancelled orders and invalid transactions
- Feature engineering (Revenue calculation)

### Feature Engineering
- Recency = Days since last purchase
- Frequency = Number of unique invoices
- Monetary = Total customer spend

### Modeling
- Log transformation (applied where appropriate)
- Feature scaling using StandardScaler
- K-Means clustering

### Evaluation Metrics
- Elbow Method (cluster compactness)
- Silhouette Score (cluster separation)
- Davies-Bouldin Index (cluster overlap)
- Calinski-Harabasz Index (cluster separation strength)

## Key Results
- Optimal Segments Identified: 3 customer segments
- Model Quality: Silhouette Score ≈ 0.42 (Good clustering quality)
- Frequent High-Value Customers: ~30% of customers generate ~82% of revenue
- Demonstrates strong Pareto-like distribution typical in retail

## Segments
### **Frequent High-Value Customers**

Characteristics:
- Low Recency
- High Frequency
- High Monetary Valye

Business Value
- Core revenue drivers
- High loyalty and engagement

Strategy
- VIP Programs
- Early product access
- Premium customer experience


### **Low-Value Customers** 

Characteristics:
- Lower purchase frequency
- Lower total spending
- Mixed recency patterns

Business Value:
- Growth opportunity segment

Strategy:
- Upsell campaigns
- Bundle offers
- Personalized promotions


### **At-Risk Customers**

Characteristics:
- High Recency (long time since last purchase)
- Previously moderate or strong purchase history

Business Value:
- Churn risk
- Previously valuable customers

Strategy:
- Win-back campaigns
- Targeted re-engagement discounts

## Files
- `1_Initial_Data_Analysis.ipynb` - Data cleaning, preparation, RFM feature engineering
- `2_Exploratory_Data_Analysis.ipynb` - Distribution analysis, skewness evaluation, outlier analysis
- `3_Clustering.ipynb` - Feature transformation, scaling, K-Means clustering, segment profiling

## Technologies
- Python
- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn

## How to Run
1. Clone the repository
2. Install dependencies:
```
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```
3. Run notebooks in order:
```
1_Initial_Data_Analysis.ipynb
2_Exploratory_Data_Analysis.ipynb
3_Clustering.ipynb
```

## Recommendations
### Frequent High-Value Customers
- Loyalty rewards programs
- Early access product launches

### Low-Value Customers
- Cross-sell and bundle strategies
- Promotional incentives

### At-Risk Customers
- Win-back email campaigns
- Limited-time reactivation offers


