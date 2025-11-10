# DATA-SCIENCE-TASK-2
#Titanic Dataset Exploratory Data Analysis (EDA) - Task 2This summary provides a theoretical description of the data wrangling and exploratory data analysis (EDA) conducted on the Titanic passenger survival dataset, focusing on identifying key predictors of survival.

# Data Preparation and Quality Assessment:
The analysis began with the ingestion of the Titanic training dataset, which comprised 891 entries across 12 columns1.
Missing Value Identification: An initial assessment revealed three columns with missing values
(NaN)2:Age: 177 missing values3.Cabin: 687 missing values4.
Embarked: 2 missing values5.
Imputation Strategy: The missing values in the continuous Age column were handled by median imputation6. 
The median age of 28.0 years 7was used to fill the 177 null entries, resulting in a complete Age column for analysis8.
This strategy is preferred over mean imputation as it is less sensitive to potential outliers9.
Key Statistics: The mean survival rate for the entire passenger cohort was approximately 38.4% (0.383838)10.
The average age of passengers (after imputation) was approximately 29.36 years11.

# Exploratory Data Analysis (EDA)
The EDA focused on visualizing distributions and examining bivariate relationships between passenger attributes and the target variable, Survived (where 0 = No and 1 = Yes)12.
1. Univariate Analysis (Distribution)Survival Count: A countplot showed that the number of passengers who did not survive (Survived = 0) was notably higher than the number who survived (Survived = 1)13.
2. Age Distribution: A histogram, plotted after imputation, indicated a concentration of passengers in the young to middle-aged range, with a significant peak near the imputed median age of 2814.

# Bivariate Analysis (Survival Factors)
Bar plots were critical in assessing the impact of categorical variables on the survival rate:Survival by Gender (Sex): A bar plot clearly showed a high survival rate for females and a significantly lower rate for males, underscoring a strong relationship between gender and survival outcome15.
Survival by Passenger Class (Pclass): A bar plot revealed a hierarchical relationship: the survival rate was highest for First-Class passengers (Pclass = 1) and decreased progressively through Second (Pclass = 2) and Third Class (Pclass = 3), indicating socioeconomic status was a critical determinant of survival16.
Multivariate AnalysisAge vs. Fare Scatter Plot: This plot, colored by survival status, suggested that passengers paying higher fares generally had a greater chance of survival, supporting the link between wealth/class and outcome. No single age group was observed to have a dominant survival advantage based purely on age17.

# Correlation Analysis
A correlation heatmap of all numerical variables provided a quantitative summary of relationships:Strongest Predictors of Survival:Pclass: Exhibited the strongest negative correlation with survival ($\rho = -0.34$)18.Fare: Showed a positive correlation with survival ($\rho = 0.26$)19.
