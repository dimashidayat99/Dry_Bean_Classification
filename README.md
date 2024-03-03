# Introduction 

Crop Classification is the core concept of smart farming that helps to improve traditional farming techniques and enables more precise and efficient cultivation methods. Improving crop classification involves accurate data collection, advanced data analysis and modeling, integration of multiple influencing factors, and continuous learning and adaptation. Farmers are influenced by smart farming due to its potential to increase productivity and  efficiency, reduce resource wastage, enable precise decision-making, optimize resource allocation, and improve overall profitability. The classification of dry bean varieties based on parameters extracted through image processing techniques poses several challenges that require further investigation. This research aims to address two key problem areas in this domain: feature importance and hyperparameter tuning. By addressing these issues, this study aims to enhance the accuracy and robustness of dry bean classification models.


# Problem Statement

Determining the importance of features extracted from images is crucial for improving the performance of classification models. While numerous image processing techniques can extract various features, it remains unclear which features are most relevant for accurate classification. Hyperparameter tuning plays a vital role in optimizing the performance of classification models. Selecting appropriate values for hyperparameters, such as learning rates, regularization terms, and batch sizes, significantly affects the model's ability to generalize and classify unseen dry bean samples accurately. However, the process of hyperparameter tuning is complex and time-consuming, requiring systematic exploration of various parameter combinations. By investigating different hyperparameter tuning approaches and evaluating their impact on classification accuracy, this research aims to provide insights into improving the efficiency and effectiveness of dry bean classification models. To address these research problems, this study will utilize a publicly available dataset obtained from Kaggle, consisting of a diverse range of dry bean images. Through an in-depth analysis of feature importance and rigorous experimentation with hyperparameter tuning techniques, the research aims to improve the classification accuracy of dry bean varieties. The findings of this study will contribute to the development of more reliable and efficient dry bean classification systems, benefiting agricultural research, farmers, and food industries involved in dry bean production and distribution.

# Research Questions

1. What is the impact of feature importance analysis and hyperparameter tuning on the classification accuracy of dry bean varieties based on parameters extracted from image processing techniques?

2. How does a mobile app for dry bean classification based on image processing techniques enhance accessibility and usability for farmers and agricultural practitioners?

# Research Objectives

1. To improve classification accuracy, this research aims to identify key features extracted from dry bean images and evaluate the impact of hyperparameter tuning on classification model performance.

2. To develop a user-friendly and accessible mobile app for accurately classifying dry bean varieties using image processing techniques, providing a practical tool to optimize cultivation practices for farmers and agricultural practitioners.

# Dataset

The [dataset](ttps://www.kaggle.com/datasets/muratkokludataset/dry-bean-dataset) used in this study is sourced from Kaggle and consists of a collection of morphological attributes of dry beans. For the classification model, images of 13,611 grains of 7 different registered dry beans were taken with a high-resolution camera. Beanimages obtained by the computer vision system were subjected to segmentation and feature extraction stages, and a total of 16 features; 12 dimensions and 4 shape forms, were obtained from the grains. It provides valuable information for developing a Dry Bean Classification System that aims to optimize cultivation practices and provide personalized classification for dry bean farmers.

The dataset contains observations of dry beans, with each instance represented by various numerical attributes. The included attributes are as follows:

1. Area: The area of the bean.
2. Perimeter: The perimeter length of the bean.
3. MajorAxisLength: The length of the major axis of the bean.
4. MinorAxisLength: The length of the minor axis of the bean.
5. AspectRatio: Ratio of length of the major axis to the length of the minor axis.
6. Eccentricity: A measure of the deviation of the bean shape from a perfect circle.
7. ConvexArea: The area of the smallest convex polygon that can enclose the bean.
8. EquivDiameter: The diameter of a circle with the same area as the bean.
9. Extent: The ratio of the bean area to the convex area.
10. Solidity: The ratio of the bean area to the convex hull area.
11. Roundness: A measure of how closely the bean resembles a circle.
12. Compactness: A measure of how compact the bean shape is.
13. ShapeFactor1: A shape factor calculated using the area and perimeter.
14. ShapeFactor2: A shape factor calculated using the area and major axis length.
15. ShapeFactor3: A shape factor calculated using the area and minor axis length.
16. ShapeFactor4: A shape factor calculated using the area and eccentricity.

The dataset includes a categorical column called "Class," which represents the class label
of each bean. The class labels indicate the specific variety or type of dry bean, allowing for
classification tasks and the dry bean types are Sekaer, Barbunya, Bombay, Cali, Dermosan,
Horoz and Sira. By analyzing this dataset, the research aims to contribute to the
understanding of the morphological determinants of dry bean quality and provide practical
solutions to optimize dry bean farming practices. The following image shows the different
types of dry bean shapes and sizes.

![]()

# Architecture

Data architecture involves starting with the data source, the dried beans dataset, and
understanding the schema and format of the dataset. Then apply data preprocessing
techniques to clean the data, handle missing values, outliers, and duplicates, and transform it into a suitable format for analysis. This step ensures the quality and integrity of the data and makes it ready for further processing.The data preparation phase focuses on splitting the data into training and testing sets and performing cross-validation or training-validation splits for model evaluation. Data architecture ensures proper partitioning and organisation of data subsets to enable effective model training and scoring. During the data modelling phase, this architecture makes it easy to integrate different machine learning models into your pipeline. This enables seamless data flow between models and ensures compatibility between input data and model requirements. Performance metrics such as accuracy, precision, recall, and F1 score as well as fitting analysis are calculated and analysed within the data architecture. This allows efficient computation and comparison of model performance, providing insight into the effectiveness of classification models. The data architecture also supports hyperparameter tuning to test and evaluate different combinations of parameters. This process optimises model performance and identifies the best set of hyperparameters for the selected model. Finally, data architecture plays a key role in providing the best model for real-world applications. Supports model integration into various deployment environments, including: An application by ensuring smooth flow and transformation of input data for classification. Overall, the data architecture of the dry bean classification pipeline is responsible for effectively organising, processing, and utilising data at various stages of the classification process, ultimately resulting in accurate and reliable predictions.

![]()

# Findings

## Descriptive Analysis
### Univariate Analysis
#### Distribution of Independent Variables

![]()

1. Area - the distribution for Area is positively skewed. Most of the data lies around 30000 to 80000 with the mode of 40000 in area. While some of the data have around 150000 to 200000 in area which indicate as outliers in area data.
2. Perimeter - the distribution of Perimeter is positively skewed with two modes of non symetric bimodal distribution. Most of the data lies in around 500 to 1250 with the first mode of the distribtion is at around 700 while second mode is around 1000. A few data is at around 1250 to 2000 which indicate the outliers in perimeter data.
3. MajorAxisLength -  the distribution of MajorAxisLength is positively skewed with two modes of non symetric of bimodal distribution. Most of the data lies in around 200 to 450 with the first mode is around 250 while the second mode is around 390. As can be seen, there are a few data at around 500 to 700 which indicates the outliers.
4. MinorAxisLength -  the distribution of MajorAxisLength is positively skewed with two modes of non symetric of bimodal distribution. Most of the data lies in around 150 to 250 with the first mode is around 290 while the second mode is around 240. As can be seen, there are a few data at around 330 to 430 which indicates the outliers.
5. AspectRation - the distribution of AspecRation is slightly positive skewed. The distribution is not fully uniform and not fully bimodal since it has peak and has a bell shape with most data lies around 1.20 to 2.25 with the mode of the distribution is at 1.50.
6. Eccentricity - the distribution of Eccentricity is negatively skewed with the mode of around 0.75 with most of the data lies in around 0.6 to 0.9.
7. ConvexArea - the distribution of ConvexArea is positively skewed with the mode of around 40000. Most of the data lies around 30000 to 80000 while some of the data lies in range 100000 to 200000 which may indicated as outliers.
8. EquivDiameter - the distribution of EquivDiameter is positively skewed with two modes of non symetric of bimodal distribution with first mode at around 230 and second mode is at 300 with most of the data lies in around 140 to 340.
9. Extent - the distribution of Extent is slighly negative skewed with the mode of around 0.78 with most of the data is around 0.7 to 0.83.
10. Solidity - the distribution of Solidity is negatively skewed with the mode of around 0.99 with most of the data lies in around 0.98 to 0.99.
11. Roundness -  the distribution of Roundness is negatively skewed with the mode at around 0.9 with most of the data lies around 0.8 to 0.95.
12. Compactness - the distribution of Compactness is uniform and can be considered as trimodal distribution. The first mode (highest peak) is at around 0.8 while second mode is at 0.9 and third mode is at 0.7. Most of the data lies between around 0.7 to 0.9.
13. ShapeFactor1 - the distribution of ShapeFactor1 is quite uniform. However it has three modes which indicates trimodal distributions. The first mode is around 0.007 while seconde mode is around 0.005 while third mode is around 0.003. Most of the data lies from around 0.005 to 0.008.
14. ShapeFactor2 -  the distribution of ShapeFactor2 looks uniform but it is slighly positive skewed bimodal distribution. The first mode is around 0.001 and second mode is at 0.0017. Most fo the data lies in around 0.00075 to 0.0025.
15. ShapeFactor3 - the distribution of ShapeFactor3 is slightly positive skewed and can be considered as trimodal distribution. The first mode (highest peak) is at around 0.65 while second mode is at around 0.49 and third mode is at around 0.82. Most of the data lies between around 0.49 to 0.82.
16. ShapeFactor4 - the distribution of ShapeFactor4 is negatively skewed with the mode of around 0.999. Most of the ata lies within 0.99 to 1.00.
    
#### Distribution of Dependent Variable

![]()

Upon analysing the dataset, it is evident that there has been no significant change in the distribution of class variables and sample size. However, a closer look reveals that the dataset suffers from an imbalance issue. The majority class is Dermason while Bombay represents the minority class.This imbalance can have serious implications on any analysis or modelling performed on this data. It may lead to biassed results and inaccurate predictions, especially for the underrepresented classes such as Bombay. Therefore, it is crucial to address this issue by employing techniques such as oversampling or undersampling to balance out the classes.

#### Outliers Analysis

![]()

There are 1129 identified outlier data points. These outliers are predominantly found in the minority class of Bombay, indicating that there may be some underlying factors contributing to their presence. While removing these outliers would result in a reduction of the dataset. Therefore, the decision is to retain them for the time being. The reasoning behind this decision is that if the outliers were to remove them and subsequently experience low accuracy with the models, it would be difficult to determine whether these issues were due to the removal of important data points or other factors entirely. However, should encounter such problems with the models down the linea and will certainly consider removing these outliers as an option. Until then, they will remain part of the dataset but will not be given undue weight or consideration during analysis.

### Multivariate Analysis
#### Scatter Plot Among Variables
![]()

The scatter plot matrix shows the relationship between variables in the dataset. This plot can shows the linearity and non linearity as well as the first picture of how well these variable is correlated with each other. For instances, Extend, Solidity, Roundess, ShapeFactor2 and ShapeFactor4 shows no correlations to all other variables since all the data point is scattered. For linear examples, the ConvexArea with Area, EquivDiameter with Area and ShapeFactor3 with Compactness have shown the strong linearity relationship while EquivDiameter with Perimeter, MajorAxisLength with EquivDiameter, Perimeter with MajorAxisLength and EquiveDiameter with MinorAxisLength has shown some degree of linearlity (weak linear relationship). For non linear examples, it can been seen that Area with Perimeter, Eccentricity with AspectRation, Compactness with AspectRation and MinorAxisLength with ShapeFactor1 shows the strong non linear relationship while ShapeFactor2 with MajorAxisLength, ShapeFactor1 with Perimeter, Area with ShapeFactor2 and ShapeFactor1 with ConvexArea have shown some degree of non linearity (weak non linear relationship).

#### Correlation Among Variables

![]()

1. Area - strong positive correlation: Perimeter, MajorAxisLength, MinorAxisLength, ConvexArea, and EquivDimater.
2.  While Area has strong negative correlation with ShapeFactor1 and ShapeFactor2.
3. Perimeter has strong positive correlation with Area, MajorAxisLength, MinorAxisLength, ConvexArea and EquivDimater. Perimeter has strong negative correlation with Roundness, ShapeFactor1, ShapeFactor2 and Class.
4. MajorAxisLength has strong positive correlation with Area, Perimeter, MinorAxisLength, ConvexArea and EquivDiameter. MajorAxisLength has strong negative correlation with Roundness, Compactness, ShapeFactor1, ShapeFactor2 and ShapeFactor3.
5.  


#### Correlation with Dependent Variables
![]()

## Predictive Analysis
### Modeling
### Evaluation
### Hyperparameter Tuning
### Features Importance

# Deployment

# Conclusion

# 

