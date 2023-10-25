
## MACHINE_LEARNING_PROJECT - UNSUPERVISED-LEARNING

 **PROBLEM STATEMENT:**
   
   - The problem is to uncover patterns and structures within
     the dataset and use these findings for informed decision-making.

 **PROJECT DESCRIPTION:**

   - The project revolves around using unsupervised learning
     techniques on the "Wholesale Data" dataset.

   - It includes two main tasks: exploratory data analysis and
     pre-processing, and unsupervised learning.

   - Exploratory data analysis involves data import, cleaning,
     analysis, visualization, handling missing values and outliers,
     and feature engineering.

   - Unsupervised learning encompasses k-means clustering, hierarchical
     clustering, and principal component analysis (PCA) to group similar
     data points and identify patterns.
   
 **PROJECT GOAL:**

   - The primary goal of the project is to gain insights from the
     dataset through data analysis and visualization.

   - The secondary goal is to effectively communicate these insights
     to stakeholders.

   - Specific goals include data preprocessing, clustering analysis,
     and dimensionality reduction using PCA.

   - The project aims to provide visualizations and metrics to enable informed
     decisions in response to business questions.

**PROCESS:**

**STEP 1:**Exploratory Data Analysis (EDA) & Data Preprocessing

   - Start by importing the Wholesale Data dataset.

   - Check for missing values and decide how to handle them
     (imputation or removal).

   - Identify and handle outliers if necessary.

   - Conduct an exploratory data analysis to understand the
     characteristics of the dataset.

   - Perform data preprocessing tasks such as data scaling.

   - Visualize the relationships between different variables
     using plots like scatter plots, histograms, and
     correlation matrices.

   - Explore the distributions and summary statistics
     of the data.

**STEP 2:** K-Means Clustering   

   - Implement K-Means clustering on the preprocessed data.

   - Use the Elbow Method to determine the optimal
     number of clusters.

   - Cluster the data and analyze the characteristics of
     each cluster.

   - Visualize the clusters using scatter plots or other
     relevant techniques.


**STEP 3:** Hierarchical Clustering: 

   - Implement hierarchical clustering to understand the
     data's hierarchical structure.

   - Choose a suitable linkage method (e.g., Ward's method,
     complete linkage, etc.).

   - Visualize the dendrogram to interpret the hierarchical
     relationships between data points.

   - Determine the number of clusters based on the dendrogram
     or other criteria.


**STEP 4:** Principal Component Analysis (PCA)

   - Apply PCA to reduce the dimensionality of the data
     while preserving variance.

   - Analyze the explained variance ratio to decide on
     the number of principal components.

   - Visualize data in the reduced-dimensional space to
     observe patterns.


**STEP 5:** Conclusion

**Exploratory Data Analysis (EDA) & Data Preprocessing**

This summary encompasses the key insights gained from the
Exploratory Data Analysis (EDA) and data preprocessing stages:

1. No missing values were found in the dataset, indicating
   that the dataset is complete.

2. The analysis of attributes such as 'Fresh,' 'Milk,' 'Grocery,'
   and 'Delicatessen' revealed significant differences between their
   mean and median values, indicating skewed data distributions.
   None of the attributes appear to follow a normal distribution.

3. The data attributes exhibit a high degree of skewness with long
   positive tails, suggesting that most of the data is concentrated
   near zero.

4. Outliers were visually detected and are scheduled for removal
   from the dataset. This decision is based on the understanding
   that Principal Component Analysis (PCA) is sensitive to noisy
   data and outliers can introduce noise into the analysis.

5. The pair plot visualization unveiled a strong correlation between
   'Detergents and Paper products' and 'Grocery products,' implying
   that customers tend to spend on these two product categories together.
   This correlation will be further investigated.

6. Correlation heatmaps highlighted several strong correlations, including:
   - A high correlation of 0.92 between 'Detergents_Paper' and 'Grocery.'
   - A notable correlation of 0.73 between 'Milk' and 'Grocery.'
   - A correlation of 0.66 between 'Detergents_Paper' and 'Milk.'

7. The feature 'Milk' displayed strong correlations with other features,
   indicating its potential predictability based on these features.
   However, even stronger correlations exist among other features,
   affecting the significance of 'Milk' as a predictor.

8. Overall, the visualizations provided evidence that the data is not
   normally distributed, with all features skewed to the right and data
   values concentrated near zero.

9. Natural logarithm scaling was applied to the data, transforming the
   distribution of each feature to be more normal. This preprocessing
   step mitigates the impact of outliers and enhances the data's suitability
   for certain algorithms.

10. The feature scaling aimed to make the data more compatible with
    clustering algorithms. It was also important to assess whether
    feature correlations remained intact after scaling.

11. A systematic approach was taken to identify and address outliers.
    Five data points were identified as outliers for multiple features.

12. To maintain data quality and reduce the influence of noisy data on
    clustering algorithms, the decision was made to remove these five
    data points that were identified as outliers for more than one feature.

 **Machine Model Insight:**

**PCA, Dimensionality Reduction & Biplot Visualization Results and Insights:**

Principal Component Analysis (PCA) was applied to the `good_data`,
resulting in essential findings:

1. PCA provided insights into the explained variance of each
   principal component. For instance, Dimension 1 explained approximately
   37.08% of the total variance.

2. The weights (loadings) of each feature for every principal component
   were presented. These weights signified how each feature contributed
   to a given dimension, with positive and negative weights indicating
   relationships.

3. A comprehensive interpretation of the primary dimensions was given,
   emphasizing:
    - Dimension 1's association with 'Grocery' and 'Detergents_Paper.'
    - Dimension 2's relation to lower spending on 'Milk,' 'Grocery,'
      and 'Detergents_Paper.'
    - Dimension 3's focus on 'Delicassen' and its negative correlation
      with 'Milk' and 'Grocery.'
    - The characteristics of other dimensions.

4. With Dimension reduction, Data was transformed into two dimensions,
   termed "Dimension 1" and "Dimension 2," simplifying data representation
   and analysis.

5. "Dimension 1" explained the primary variance, and values along this
    dimension illustrated data point deviations. Negative values implied
    lower spending in categories associated with this dimension.

6. "Dimension 2" encapsulated secondary variance, providing insights into
    spending patterns and deviations.

7. A biplot visualized the original feature projections, making it easier
   to interpret data point positions. For instance, lower right corner data
   points indicated high spending on specific categories.

8. The visualization highlighted strong correlations, such as the negative
   association of 'Detergents_Paper,' 'Grocery,' and 'Milk' with "Dimension 1."


