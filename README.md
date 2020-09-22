# Coursera_Capstone

## 1. Business Understanding

The Seattle government will prevent avoidable car accidents by warning drivers, medical systems and police to remind them to be more careful in an emergency.

In most cases, driving with drug and alcohol abuse, or not paying enough attention to driving at high speeds are the main causes of accidents, and solve this, should issue more stringent regulation to prevent accidents. In addition to the above reasons, weather, visibility or road conditions are the main uncontrollable factors, which can be avoided by revealing hidden patterns in the data and issuing warnings to the local government, police and drivers on the target road.

The target audience of the project is local Seattle government, police, rescue groups, car insurance company, also is very helpful for every driver who need to pay more attention when concur related situation. The model and its results are going to provide some advice for the target audience to make insightful decisions for reducing the number of accidents and injuries for the city.

## 2. Data

The data was collected by the Seattle Police Department and Accident Traffic Records Department from 2004 to present.
The data consists of 37 independent variables and 194,673 rows. 

The models aim to predict the severity of an accident, I choose 5 features were selected for this project along with the target variable being Severity Code. Target variable are, INATTENTIONIND, UNDERINFL, WEATHER, ROADCOND, LIGHTCOND and SPEEDING.

**SEVERITYCODE:** A code that corresponds to the severity of the collision.

0: Property Damage Only Collision，in dataset：1

1: Injury Collision, in dataset:2

**INATTENTION:** Whether or not collision was due to inattention. (Y/N)

0: NAN

1: Yes

**UNDERINFL:** Whether or not a driver involved was under the influence of drugs or alcohol.

0: N

1: Y

**SPEEDING:** Whether or not speeding was a factor in the collision. (Y/N).

0: NAN

1: Y


**LIGHTCOND：** The light conditions during the collision.

0: Day Light

1: Medium, represent Dark - Street Lights On, Dusk, Dawn, 

2: Dark, represent Dark - No Street Lights, Dark - Street Lights Off, Dark - Unknown Lighting

other: Unknow

**WEATHER:** A description of the weather conditions during the time of the collision.

0: Clear

1: Overcast, Partly Cloudy

2: Fog/Smog/Smoke, Blowing Sand/Dirt, Severe Crosswind

3: Raining, Snowing, Sleet/Hail/Freezing Rain

**ROADCOND:**

0: Dry

1: Snow/Slush, Sand/Mud/Dirt

2: Wet, Ice, Standing Water, Oil

**Hint:**
0 was assigned to the element be the least probable cause of severe accident, high number represented bad condition which could lead higher accident severity. I found that, there were either ‘Other’ or ‘Unknown’ rows, but rows are unique values for every variable, will not delete those rows entirely, this may led to a lot of loss of data.

## 3. Methodology
For implementing the solution, I have used Github as a repository and running Jupyter Notebook to preprocess data and build Machine Learning models. Regarding coding, I have used Python and its popular packages such as Pandas, NumPy and Sklearn.
After balancing SEVERITYCODE feature, and standardizing the input feature, the data has been ready for building machine learning models.

The machine learning models used are Logistic Regression, Decision Tree Analysis and k-Nearest Neighbor. 

- **Logistic Regression**
As I learned in previous course, Logistic regression is the appropriate regression analysis to conduct when the dependent variable is dichotomous (binary).  Like all regression analyses, the logistic regression is a predictive analysis.  Logistic regression is used to describe data and to explain the relationship between one dependent binary variable and one or more nominal, ordinal, interval or ratio-level independent variables.
Sometimes logistic regressions are difficult to interpret; the Intellectus Statistics tool easily allows you to conduct the analysis, then in plain English interprets the output.

- **Decision Tree Analysis**
Decision tree analysis decomposes the data set into smaller subsets. At the same time, related decision trees are being developed gradually. The end result is a tree with decision nodes and leaf nodes.
- **K Nearest Neighbors**
K nearest neighbors is a simple algorithm that stores all available cases and classifies new cases based on a similarity measure (based on distance). 
In pattern recognition, the k-nearest neighbors algorithm (k-NN) is a non-parametric method proposed by Thomas Cover used for classification and regression. In both cases, the input consists of the k closest training examples in the feature space. The output depends on whether k-NN is used for classification or regression:
In k-NN classification, the output is a class membership. An object is classified by a plurality vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). If k = 1, then the object is simply assigned to the class of that single nearest neighbor.
In k-NN regression, the output is the property value for the object. This value is the average of the values of k nearest neighbors.

### Reason for Method Chosen
**Advantages of Logistic Regression:**
- Easy, fast and simple classification method.
- θ parameters explains the direction and intensity of significance of independent variables over the dependent variable.
- Can be used for multiclass classifications also.
- Loss function is always convex.


**Advantages of Decision Tree Analysis:**
- No preprocessing needed on data.
- No assumptions on distribution of data.
- Handles colinearity efficiently.
- Decision trees can provide understandable explanation over the prediction.


**Advantages of KNN:**
- Easy and simple machine learning model.
- Few hyperparameters to tune.

On the other hand, for large data sets, the SVM model is inaccurate, and the data set has so many rows filled with data. In addition, SVM is best suited for filling text and image data sets.

In conclusion, I have employed three machine learning models:
* Decision Tree
* Linear Regression
* K Nearest Neighbour (KNN)


## 4.Results
After importing necessary packages and splitting preprocessed data into test and train sets, for each machine learning model, built and evaluated the model and shown the results, and accuracy report, say from Precision, Recall, and f1-score to evaluate the model.

### 4.1 Decision Tree Analysis
The decision tree classifier in the scikit-learn library is used to run the decision tree classification model on the "car accident severity" data. The criterion selected for the classifier is "entropy" and the maximum depth is "6".

#### 4.1.1 Classification Report

|              | precision | recall | f1-score |
|--------------|-----------|--------|----------|
| 0            | 1.00      | 0.70   | 0.82     |
| 1            | 0.00      | 0.49   | 0.01     |
| Accuracy     | 0.696     |        |          |
| micro avg    | 0.70      | 0.70   | 0.70     |
| macro avg    | 0.50      | 0.60   | 0.41     |
| weighted avg | 1.00      | 0.70   | 0.82     |

#### 4.1.2 Confusion Matrix

![image](https://github.com/ybeven/Coursera_Capstone/blob/master/imgs/01.jpg)





## Conclusion
give the conclusion at last.

