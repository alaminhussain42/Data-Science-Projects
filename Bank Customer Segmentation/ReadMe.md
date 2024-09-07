# Bank Customer Segmentation

## Introduction
The goal of this project is to conduct customer market segmentation for a bank, enabling the marketing team to launch targeted advertising campaigns tailored to specific customer groups. By identifying these segments, the bank can optimize its resources and improve customer engagement.

## Objectives
1. **Market Segmentation**: Group customers into distinct segments based on behavioral and demographic data.
2. **Targeted Marketing**: Allow the marketing team to develop strategies for each customer segment.

## Approach
### 1. **Dimensionality Reduction (PCA)**
   - We used **Principal Component Analysis (PCA)** to reduce the dimensions of the dataset. This helped in simplifying the feature set while retaining most of the variance.
   - Before applying PCA, we conducted **Bartlett’s test of sphericity** to check the appropriateness of PCA for dimensionality reduction.

### 2. **Clustering Techniques**
   - **K-Means Clustering**: 
     - We experimented with different numbers of clusters using the **Elbow Method** to find the optimal number of clusters.
     - We also used the **Silhouette Score** to assess the quality of the clustering.
   - **Gaussian Mixture Models (GMM)**:
     - For GMM, we used both the **Bayesian Information Criterion (BIC)** and **Akaike Information Criterion (AIC)** to evaluate the model and select the number of clusters.

### 3. **t-SNE Visualization**
   - After clustering, we applied **t-distributed Stochastic Neighbor Embedding (t-SNE)** to visualize the customer segments in two dimensions.

## Evaluation Metrics
- **Silhouette Score** and **Elbow Method** were used to evaluate the KMeans clustering results.
- **BIC** and **AIC** were used to evaluate the performance of the GMM model.

## Results
The segmentation identified clear groups of customers, and the clustering models demonstrated good fit, allowing the bank to effectively tailor its marketing campaigns.

## Conclusion
Through dimensionality reduction, clustering, and visualization, we were able to successfully segment the bank's customers into meaningful groups. This segmentation will help the marketing team in creating more personalized and effective advertising strategies.

## Technologies Used
- **Python Libraries**: Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
- **Clustering Models**: KMeans, Gaussian Mixture Models (GMM)
- **Dimensionality Reduction**: PCA, t-SNE
