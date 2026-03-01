Distributed Machine Learning for High-Value Fare Classification in Large-Scale Urban
Mobility Data
Abstract
In this project, binary classification is considered, the distributed machine learning is used to
make the high-value taxi trip binary classification based on the New York City Yellow Taxi
January 2023 data. The Apache Spark 3.5.1 and PySpark MLlib scalable pipeline were used
to process millions of transportation records (stored on Parquet formatted files). The AUC,
accuracy, and F1-score were used to compare four classification algorithms Logistic
Regression, Decision Tree, Random Forest, and Gradient Boosted Trees. The results of the
experiment prove that ensemble approaches have higher predictive power and can better
represent the nonlinear fare trends. Scalability experiments also indicate the relevance of
partition tuning in optimisation of distributed computing.
1. Introduction
The platforms of urban mobility produce huge amounts of structured transactional data on a
day to day basis. The analysis of such data is requisite to optimise revenues, surge pricing,
detecting frauds, and planning transport policies. When faced with multi-million-record
transportation datasets, traditional machine learning systems that are single node in nature are
not able to scale.
The proposed problem in this project will be solved by using distributed classification models
in Apache Spark to detect high-value taxi trips. It is a research that concentrates on predictive
performance and computational scalability in a big data environment.
2. Problem Statement
Current methods of transportation analytics have a number of limitations:
● Low scaling with large urban mobility data.
● Large-scale computation of single environments.
● Weakness in nonlinear fare behaviour capturing.
● Large aggregation bottlenecks when performing.
As such, a distributed machine learning system is needed, which effectively classifies high-
fare trips whilst preserving good predictive speed.
3. Research Objectives
The project aims to:
● A Scalable Spark-based data engineering pipeline.
● Use several methods of PySpark MLlib classification.
● Perform model evaluation in terms of strong classification measures.

● Compare the effect of partition tuning on algorithm performance.
● Get business insight on fare and revenue patterns.
4. Dataset Overview
The analysis will use the NYC Yellow Taxi Trip Records which are January 2023. Data is in
Parquet format and it has millions of structured trip-level data.
Key Attributes
● Fare amount
● Trip distance
● Passenger count
● Pickup and drop off locations IDs.
● Payment type
● Pickup timestamp
The binary variable (highfare) was engineered based on the following rule:
High fare = fareamount &gt; 30 USD
Exploratory analysis showed that the class balance was moderate and genders were skewed to
the right which can commonly be seen in urban transport system.
5. Methodology
The suggested scheme includes the following steps:
● Ingestion Distributed Data ingestion with Apache Spark.
● Null processing and data cleaning.
● VectorAssembler/FEATURE ENGINEER
● by VectorCal 286 /8880
● Creation of binary targets by fare thresholding.
● Train-test split (80/20)
● PySpark MLlib model training.
● Performance evaluation
● Scalability analysis through repartitioning.
The tune of Spark configurations was made to match parallelism and overhead.
6. Machine Learning Models
There were four distributed classifiers:
● Management control Logistic Regression (baseline linear model)
● Decision Tree Classifier
● Random Forest Classifier
● Gradient Boosted Trees Classifier.

Ensemble models based on trees were chosen because they are resistant to feature scaling and
model nonlinear interactions.
7. Performance Metrics
The following were used to determine model performance:
● Area under the ROC Curve(AUC)- main measure.
● Accuracy
● F1-score
The reason was the appropriate certification of AUC due to its strength of resistance to class
imbalance and that it can measure the quality of ranking regardless of the classification
threshold.
8. Results and Discussion
The experimental findings reveal that ensemble models are much better in comparison to
linear and single-tree models.
Key Findings
● Random Forest 0.99 Gradient Boosted Trees 0.99
● Regression Logistic reached a moderate score (0.95 AUC).
● Decision Tree showed satisfactory results albeit, less stable.
● Ensemble averaging lowered the model variance and enhanced generalisation.
Analysis of features showed that trip distance and spatial variables are excellent predictors of
high-fare trips.
9. Scalability Analysis
Significant distributed system trade-offs as evidenced by partition tuning Bombied
experiments (50-400 partitions) showed:
● The first thing is that increasing the number of partitions enhances parallelism.
● Overscheduling and re-scheduling overhead.
● Maximum performance is reached at moderate levels of partition.
● The ensemble models consume more computational resources.
These results prove the relevance of balanced Spark set-up in large-scale ML pipelines.
10. Visual Analytics
Analytical insights were created in interactive Tableau dashboards and included:
● ROC performance comparison
● Evaluation in confusion matrix.
● Hourly revenue patterns
● Spatial distribution of revenue.

● Scalability performance of Spark.
The dash boards indicate that the revenue is strongly concentrated in the high demand times
and the high-value area in picking up.
11.Conclusion
The project manages to prove that distributed machine learning can be effective in the
classification of high-fare taxi trips. Random Forest and Gradient Boosted Tree are both
examples of ensemble model which demonstrates better predictive power than the linear
baselines. The paper also validates that caution is very critical in partition tuning in attaining
the best distributed computation efficiency. The research results have a practical implication
in relation to smart transportation and revenue optimisation.
12. Future Work
This can be improved in future through:
● Hyperparameter optimisation which is automated.
● State-of-the-art geospatial engineering.
● Online cost-performance analysis.
● Making use of deep learning solutions.
