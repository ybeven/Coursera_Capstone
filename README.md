# Coursera_Capstone

## Business Understanding

The Seattle government will prevent avoidable car accidents by warning drivers, medical systems and police to remind them to be more careful in an emergency.

In most cases, driving with drug and alcohol abuse, or not paying enough attention to driving at high speeds are the main causes of accidents, and solve this, should issue more stringent regulation to prevent accidents. In addition to the above reasons, weather, visibility or road conditions are the main uncontrollable factors, which can be avoided by revealing hidden patterns in the data and issuing warnings to the local government, police and drivers on the target road.

The target audience of the project is local Seattle government, police, rescue groups, car insurance company, also is very helpful for every driver who need to pay more attention when concur related situation. The model and its results are going to provide some advice for the target audience to make insightful decisions for reducing the number of accidents and injuries for the city.

## Data

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

## Methodology
For implementing the solution, I have used Github as a repository and running Jupyter Notebook to preprocess data and build Machine Learning models. Regarding coding, I have used Python and its popular packages such as Pandas, NumPy and Sklearn.
After balancing SEVERITYCODE feature, and standardizing the input feature, the data has been ready for building machine learning models.

I have employed three machine learning models:
* Decision Tree
* Linear Regression
* K Nearest Neighbour (KNN)
## Build, results
After importing necessary packages and splitting preprocessed data into test and train sets, for each machine learning model, built and evaluated the model and shown the results, and accuracy report, say from Precision, Recall, and f1-score to evaluate the model.

## Conclusion
give the conclusion at last.

