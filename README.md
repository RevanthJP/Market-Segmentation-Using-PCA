# Market Segmentation Using PCA

## Executive Summary
The Hair Salon dataset focuses on various variables essential for market segmentation, particularly in the context of a salon chain's product line. The goal of this project is to perform Principal Component Analysis (PCA) on the dataset to identify the most significant factors influencing marketing strategies.

## Introduction
This project explores different methods for determining the best components influencing the marketing of hair products. Steps undertaken include data exploration (shape, missing values, outliers), univariate and bivariate analysis, graphical representation, and scaling. The objective is to identify the principal components driving the business's marketing success.

## Data Description
The dataset contains the following features:
- **ProdQual**: Product Quality
- **Ecom**: E-commerce activity
- **TechSup**: Tech Support satisfaction
- **CompRes**: Complaint Resolution
- **Advertising**: Advertising effectiveness
- **ProdLine**: Product Line information
- **SaleFImage**: Salesforce Image
- **CompPricing**: Competitive Pricing
- **WartyClaim**: Warranty & Claims data
- **OrdBilling**: Order & Billing details
- **DelSpeed**: Delivery Speed
- **Satisfaction**: Customer Satisfaction

## Exploratory Data Analysis (EDA)

### Data Sample
Here is a sample of the dataset's first five rows:

| ProdQual | Ecom | TechSup | CompRes | Advertising | ProdLine | SaleFImage | CompPricing | WartyClaim | OrdBilling | DelSpeed | Satisfaction |
|----------|------|---------|---------|-------------|----------|------------|-------------|------------|------------|----------|--------------|
| 4        | 3    | 2       | 5       | 2           | 3        | 5          | 4           | 2          | 3          | 4        | 3            |

### Descriptive Statistics
The dataset includes 13 features with their respective statistical details (mean, median, std, min, max, quartiles), and the absence of null values is confirmed.

### Univariate Analysis
Each feature's distribution has been visualized. Key observations:
- **Tech support, Delivery speed, and Product Quality** are left-skewed.
- Other variables show varied distributions, not typically skewed.

#### Outliers
Outliers were identified in features like **Ecom, SalesFImage, OrdBilling**, and **DelSpeed** using boxplots.

### Pairplot
The pairplot below visualizes the relationships between features and their distributions:

<img width="489" alt="image" src="https://github.com/user-attachments/assets/b4a0e15d-5d23-4034-b1f7-de5371c77fd6">


### Correlation
Correlation analysis reveals the following:
- **SalesFImage** is positively correlated with **Ecom**.
- **WartyClaim** correlates with **TechSup**.
- **DelSpeed** is linked to **CompRes**.

#### Heatmap
A heatmap further shows the correlation of all features, highlighting strong correlations among a few key variables.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/be49894f-93a8-4703-a246-ec46329a9326">


## Scaling the Data

Data scaling was performed using **StandardScaler** to normalize the features and improve model performance. After scaling, all features have the same standard deviation, which aids in reducing bias due to differing scales.

### Covariance vs. Correlation
We compared the covariance matrix and the correlation matrix. Despite their differences in interpretation, the correlation matrix provides clearer insights into variable relationships after scaling.

## Outliers Before and After Scaling
Outliers were identified before scaling in variables like **Ecom** and **SalesFImage**, and after scaling, the same variables continued to show outliers. These outliers were treated using capping techniques.

## PCA Analysis

### Covariance Matrix, Eigenvalues, and Eigenvectors
The covariance matrix was computed, and the eigenvalues and eigenvectors were derived for the scaled dataset. Key results include:
- Eigenvalues: 3.04, 2.16, 1.50, etc.
- The eigenvectors indicate the principal directions of variance in the data.

### Explained Variance
The explained variance of principal components reveals that the first 5 components explain over 80% of the dataset's total variance, making them optimal for this analysis.

#### Scree Plot
The scree plot visually confirms that the first five components account for the majority of the variance.

<img width="429" alt="image" src="https://github.com/user-attachments/assets/0d3a97d7-964b-4aef-aa8f-263b05ea602b">


### Business Implications
The PCA results offer actionable insights:
- **E-commerce** and **Salesforce Image** are strongly correlated, suggesting that improving the Salesforce Image can drive more e-commerce transactions.
- Focus should also be placed on improving features like **Advertising** and **Product Quality**, as they play a critical role in customer satisfaction and business success.

## Conclusion
PCA has enabled us to identify the key factors influencing the market segmentation of the salon's products. By concentrating efforts on improving the first five principal components, the business can achieve better segmentation and, ultimately, higher customer satisfaction and sales.
