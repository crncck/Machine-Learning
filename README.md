# Machine Learning

**Machine learning** is the use and development of computer systems that are able to learn and adapt without following explicit instructions, by using algorithms and statistical models to analyze and draw inferences from patterns in data.

Machine learning is used in various applications like –  **voice search technology, image recognition, automated translation, self-driven cars**, etc.

<br>

## 1. Basic Concepts in Machine Learning

### 1.1. Types of Data

```mermaid
graph
A[Types of data] --> B[Quantitative]
A --> C[Qualitative]
C --> D[Nominal]
C --> E[Ordinal]
B --> F[Discrete]
B --> G[Continuous]
```

- **Quantitative data** is data that can be counted or measured in numerical values.
	- To Visualize: histogram, box plots, scatter plots
		- Discrete: countable
		- Continuous: measurable


- **Qualitative data** describes qualities or characteristics.
	- To Visualize: bar charts, dot charts
		- Nominal: labelled categories
		- Ordinal: ordered categories

<br>

### 1.2. Types of Statistics

```mermaid
graph LR
A[Types of statistics] --> B(Descriptive)
A --> C(Inferential)
```

- **Descriptive Statistics**:  Summarizes the characteristics of a data set and gives information about raw data regarding its description or features.
	- Measures of central tendency
		-  Mean
		- Median
		- Mode
	-  Measures of dispersion
		- Range
		- Standard deviation
		- Variance
	- Frequency distributions
	- Histograms

<br>

- **Inferential Statistics**: the practice of using sampled data to draw conclusions or make predictions about a larger sample data sample or population.
	- Linear regression
	- Logistic regression
	- LDA & KNN
	- Decision trees and more..

<br>

### 1.3. Learning Types

```mermaid
graph
A[Machine Learning] --> B(Supervised Learning)
B --> E(Classification)
B --> F(Regression)
A --> C(Unsupervised Learning)
C --> G(Clustering)
C --> H(Dimensionality Reduction)
A --> D(Reinforcement Learning)
```

<br>

**1-Supervised Learning**: Use of labeled datasets to train algorithms that to classify data or predict outcomes accurately.

- Classification: It is the task of predicting a discrete class label. ***Examples**, fraud detection, email spam detection, diagnostics, image classification.*
	-  K-Nearest Neighbor
	- Logistic Regression
	- Support Vector Machines
	- Decision Trees
	- Artificial Neural Networks

- Regression: It is the task of predicting a continuous quantity. ***Examples**, risk assessment, score prediction.*
	- Linear Regression
	- Polynomial Regression
	- Support Vector Regression
	- Decision Tree Regression
	- Multiple Linear Regression
	- Random Forest Regression

<br>

**2-Unsupervised Learning**: Use of machine learning algorithms to analyze and cluster unlabeled datasets. These algorithms discover hidden patterns or data groupings without the need for human intervention.

- Clustering: It is identifying and grouping similar data points in larger datasets without concern for the specific outcome. ***Examples**, biology, city planning, targetted marketing.*
	-  K-Means Clustering
	- Hierarchical Clustering

- Dimensionality Reduction: It is a statistical technique of reducing the amount of random variables in a problem by obtaining a set of principal variables. ***Examples**, text mining, face recognition, image recognition, big data visualization.*
	- PCA
	- Kernel PCA

<br>

**3-Reinforcement Learning**: It is a method based on rewarding desired behaviors and/or punishing undesired ones. A reinforcement learning agent is able to perceive and interpret its environment, take actions and learn through trial and error. ***Examples**, gaming, finance sector, inventory management, robot navigation.*
- Q-Learning
- State-Action-Reward-State-Action (SARSA)
- Deep Q Network (DQN)

<br>

## 2. Steps in Building Machine Learning Model

 1.  Problem formulation
 2. Data tidying
 3. Data Preprocessing
	- Data Cleaning
		- Missing Data
		- Noisy Data
		- Outlier
	- Data Integration
	- Data Transformation
		- Aggregation
		- Normalization
		- Feature Selection
		- Discretization
		- Concept Hierarchy Generation
	- Data Reduction
		- Data Cube Aggregation
		- Attribute Subset Selection
		- Numerosity Reduction
		- Dimensionality Reduction
 4. Train-Test Split
 5. Model Building
 6. Performance Metrics and Validation
 7. Prediction

<br>

### 2.1. Data Preprocessing

Data preprocessing is a step in the data mining and data analysis process that takes raw data and transforms it into a format that can be understood and analyzed by computers and machine learning.

Data preprocessing is important to improve the overall data quality. 

Why is data preprocessing important?
-   Duplicate or missing values may give an incorrect view of the overall statistics of data.
-   Outliers and inconsistent data points often tend to disturb the model’s overall learning, leading to false predictions.

Data preprocessing handles them.

There are **four main steps** of data preprocessing.

```mermaid
graph 
A(Data Preprocessing) --> B(Data Cleaning)
A --> C(Data Integration)
A --> D(Data Transformation)
A --> E(Data Reduction)
```
<br>

#### 2.1.1. Data Cleaning
**Data cleaning** is the process of adding missing data and correcting, repairing, or removing incorrect or irrelevant data from a dataset.

- **Missing data:** Some data is missing in the dataset. It can be handled in various ways:
	- **Ignore the tuples:** when dataset is huge and multiple values are missing within a tuple.
	
	- **Fill the missing values:** fill the missing values manually, by attribute mean or the most probable value.

- **Noisy data:** It is a meaningless data. It can be generated due to faulty data collection, data entry errors. It can be handled in following ways :
	- **Binning:** It works on sorted data values. The data is divided into equal-sized bins, and each bin/bucket is dealt with independently. Income, for example, could be grouped: $35,000-$50,000, $50,000-$75,000, etc
	
	- **Regression:** It helps to smoothen noise by fitting all the data points in a regression function. The regression used may be linear (having one independent variable) or multiple (having multiple independent variables).
	
	- **Clustering:** Creation of groups/clusters from data having similar values. The values that don't lie in the cluster can be treated as noisy data and can be removed.

<br>

#### 2.1.2. Data Integration

**Data integration** is one of the data preprocessing steps that are used to merge the data present in multiple sources into a single larger data store like a data warehouse.

<br>

#### 2.1.3. Data Transformation

**Data transformation** is taken in order to transform the data in appropriate forms suitable for mining process. This involves following ways:
-  **Aggregation:** Data aggregation combines all of your data together in a uniform format.

-  **Normalization:** It is done in order to scale the data values in a specified range (-1.0 to 1.0 or 0.0 to 1.0).
	-   Min-max normalization
	-   Z-Score normalization
	-   Decimal scaling normalization

-  **Feature selection:** Feature selection is the process of deciding which variables are most important to your analysis. New properties of data are created from existing attributes to help in the data mining process.

-  **Discreditization:** This is done to replace the raw values of numeric attribute by interval levels or conceptual levels.

-  **Concept hierarchy generation:** Concept hierarchy generation can add a hierarchy within and between your features that wasn’t present in the original data. If your analysis contains wolves and coyotes, for example, you could add the hierarchy for their genus: _canis_.

<br>

#### 2.1.4. Data Reduction

The size of the dataset can be too large to be handled by data analysis and data mining algorithms.

One possible solution is to obtain a reduced representation of the dataset that is much smaller in volume but produces the same quality of analytical results. For this, we use **data reduction** techniques.

- **Data Cube Aggregation:** It is a way of data reduction, in which the gathered data is expressed in a summary form.

- **Attribute Subset Selection:** The highly relevant attributes should be used, rest all can be discarded. It, essentially, combines tags or features.

- **Numerosity Reduction:** The data can be represented as a model or equation like a regression model. This would save the burden of storing huge datasets instead of a model.

- **Dimensionality Reduction:** This technique aims to reduce the number of redundant features we consider in machine learning algorithms. Dimensionality reduction can be done using techniques like Principal Component Analysis etc.
