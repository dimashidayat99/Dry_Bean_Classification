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

The [dataset](https://www.kaggle.com/datasets/muratkokludataset/dry-bean-dataset) used in this study is sourced from Kaggle and consists of a collection of morphological attributes of dry beans. For the classification model, images of 13,611 grains of 7 different registered dry beans were taken with a high-resolution camera. Beanimages obtained by the computer vision system were subjected to segmentation and feature extraction stages, and a total of 16 features; 12 dimensions and 4 shape forms, were obtained from the grains. It provides valuable information for developing a Dry Bean Classification System that aims to optimize cultivation practices and provide personalized classification for dry bean farmers.

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

1. Area - Strong positive correlation: Perimeter, MajorAxisLength, MinorAxisLength, ConvexArea, and EquivDimater. Strong negative correlation: ShapeFactor1 and ShapeFactor2.
2. Perimeter - Strong positive correlation: Area, MajorAxisLength, MinorAxisLength, ConvexArea and EquivDimater. Strong negative correlation: Roundness, ShapeFactor1, ShapeFactor2 and Class.
3. MajorAxisLength - Strong positive correlation: Area, Perimeter, MinorAxisLength, ConvexArea and EquivDiameter. Strong negative correlation: Roundness, Compactness, ShapeFactor1, ShapeFactor2 and ShapeFactor3.
4. MinorAxisLength - Strong positive correlation: Area, Perimeter, MajorAxisLength, ConvexArea and EquivDiameter. Strong negative correlation: ShapeFactor1.
5. AspectRation - Strong positive correlation: MajorAxisLength and Eccentricity. Strong negative correlation: Roundness, Compactness, ShapeFactor2 and ShapeFactor3.
6. Eccentricity - Strong positive correlation: MajorAxisLength and AspectRation. Strong negative correlation: Roundness, Compactness, ShapeFactor2 and ShapeFactor3.
7. ConvexArea - Strong positive correlation: Area, Perimeter, MajorAxisLength, MinorAxisLength and EquivDiameter. Strong negative correlation: ShapeFactor1 and ShapeFactor2.
8. EquivDiameter - Strong positive correlation: Perimeter, MajorAxisLength, MinorAxisLength and ConvexArea. Strong negative correlation: ShapeFactor1 and ShapeFactor2.
9. Extent - No strong correlation. 
10. Solidity - Strong positive correlation: ShapeFactor4 and Roundess. Strong negative correlation: None.
11. Roundness - Strong positive correlation: Solidity, Compactness, ShapeFactor2 and ShapeFactor3. Strong negative correlation: Perimeter, MajorAxisLength, AspectRation and Eccentricity.
12. Compactness - Strong positive correlation: Roundness, ShapeFactor2 and ShapeFactor3. Strong negative correlation: MajorAxisLength, AspectRation and Eccentricity.
13. ShapeFactor1 - Strong positive correlation: None. Strong negative correlation: Area, Perimeter, MajorAxisLength, MinorAxisLength, ConvexArea and EquivDiameter.
14. ShapeFactor2 - Strong positive correlation: Roundness, Compactness, ShapeFactor3 and ShapeFactor4. Strong negative correlation: Area, Perimeter, MajorAxisLength, AspectRation, Eccentricity, ConvexArea and EquivDiameter.
15. ShapeFactor3 - Strong positive correlation:  Roundness, Compactness and ShapeFactor3. Strong negative correlation: MajorAxisLength, AspectRation and Eccentricity.
16. ShapeFactor4 - Strong positive correlation: ShapeFactor2 and Solidity. Strong negative correlation: None.
17. Class - Strong positive correlation: None. Strong negative correlation: None.

#### Correlation with Dependent Variables
![]()

In order to gain a deeper understanding of the relationship between various features and the target variable "Class", a thorough analysis is conducted. This involves calculating the correlation coefficient for each feature with respect to Class, which provides valuable insights into their respective strengths of association. From the correlation analysis, not all features are created equal when it comes to their correlation with Class. Some, such as Extent, Eccentricity, AspectRatio, Compactness, ShapeFactor3 and ShapeFactor4 exhibit weaker
correlations than others. While still potentially useful in certain contexts, these features may not be as reliable predictors of Class as those that demonstrate stronger associations. 

## Predictive Analysis
### Modeling

For Data Modelling, it is divided into two different types of model for machine learning which is classical machine learning and modern machine learning. For classical machine learning models, 10-fold cross-validation was performed using the training data. This means that the training data was split into 10 equal parts called folds. Each fold alternately serves as the validation set, while the other nine folds are combined to form the training set. By rotating the folds and repeating this process 10 times. This approach gave a better understanding of how well the model performed on different subsets of the training data. The classic machine learning chosen were Logistic Regression, Support Vector Machine (SVM), Gaussian Naïve Bayes, K Nearest Neighbour(K-NN), Extra Tree, Random Forest, Decision Tree, LightGBM and XGBoost. The modern machine learning used neural network consists of four layers. An input layer, three hidden layers, and an output layer. The number of units in the input layer is determined by the input dimension, which represents the number of columns of input data which in this case is 16. Each hidden layer has 64 neurons and uses a Rectified Linear Unit (ReLU) activation function that introduces nonlinearity into the network. This helps the model learn complex relationships and patterns in the data. The output layer has 7 neurons, indicating that the model is designed for a multiclass classification problem with 7 possible classes of Dry Beans. The output layer uses a softmax activation function that produces probability distributions between classes. This allows the model to assign probabilities to each class of Dry Beans and make predictions based on the highest probabilities.

### Evaluation
![]()
For logistic regression, Gaussian Naive Bayes, SVM and Neural Network, the accuracy curves show consistently high accuracy across the folds for both train data and validation data. This shows that these models can learn effectively from the training data and perform well on new and unfamiliar data. Therefore, these are considered well-fitting models. On the other hand, the KNN, Decision Tree, Random Forest, Xgboost, and Extra-Tree models showed variation in accuracy from convolution to convolution. Accuracy curves showed higher accuracy for training data compared to validation data. This suggests that these models are overfitted, focusing too much on specific examples in the training data and not translating well to new, unseen data. In summary, from the accuracy plots, logistic regression, Gaussian Naive Bayes, and SVM were found to be suitable models as they consistently achieved high accuracy on both training and validation data. However, KNN, decision tree, random forest, Xgboost, and extra-tree models were overfitted because they improved in accuracy on the training data but decreased in accuracy on the validation data. These insights will help you understand the strengths and weaknesses of each model and help you choose the right model for the classification of Dry Beans.

![]()
All the models achieve accuracy higher than 90% which means all models performed good enough. However, from the fitting analysis, some models are overfitting such as KNN, ExtraTree, RandomForest, DecisionTree, Lightgbm and Xgboost. The remaining well fitted model is Logistic regression, SVM, GaussianNaiveBayes and Neural Network. Hyperparameter tuning for these 4 models are computationally expensive. Therefore, We select only 1 best model and tune the model to improve the accuracy further. Among these models, SVM shows the highest accuracy. Therefore, SVM will be tuned.

### Hyperparameter Tuning

![]()

After hyperparamter tuning of SVM model, the accuracy of SVM increases from 0.9464 to 0.9541. The difference is very small but it still performed well for short execution time for hyperparameter tuning.

### Features Importance

The feature importance is obtained based on the tuned SVM model. The features importances in ascending order are Extent, ShapeFactor2, Solidity, ShapeFactor3, Area, ConvexArea, Compactness, MinorAxisLength, Perimeter, EquiveDiameter, roundness,ShapeFactor4, MajorAxisLength, ShapeFactor1, AspectRation and Eccentricity.

# Deployment

The deployment of the model was built using Flask app that is run locally on my computer. The final product of this project was a website application based on the findings from descriptive and predictive analysis. The web application was built by utilizing the website template Mordernized from [AdminMart](https://adminmart.com/product/modernize-free-bootstrap-5-admin-template/). 

The demo of the website:


# Conclusion
Throughout this project, the objectives set at the beginning has been successfully achieved, with a focus on contributing to the future of agriculture and smart farming practices. Some of the noteworthy progress include achieving a higher accuracy for classification than the past researches, at 0.9541 using the SVM hyperparameter-tuned model. Furthermore, from the best models tested, the feature importance has been recognized. In ascending order are ascending order are Extent, ShapeFactor2, Solidity, ShapeFactor3, Area, ConvexArea, Compactness, MinorAxisLength, Perimeter, EquiveDiameter, roundness,ShapeFactor4, MajorAxisLength, ShapeFactor1, AspectRation and Eccentricity. Lastly, in order to successfully contribute to the agriculturecommunity, a deployment structure has been identified and clearly defined, through the use of a web application which allows ease of access. As such, the working structure and wireframe has been developed for implementation.

To conclude, the outcomes of this project have valuable implications for the field of dry bean research, aiding in species identification, crop management, and agricultural practices. With further refinement and expansion, the project's findings can contribute to advancing the understanding and utilisation of dry beans in various industries and sectors

#
Notes: This project used website template from Mordenized from [AdminMart](https://adminmart.com/product/modernize-free-bootstrap-5-admin-template/). Where I only edit and used based on my needs. All the library, software, technology and etc used in the development of website are not my work.

