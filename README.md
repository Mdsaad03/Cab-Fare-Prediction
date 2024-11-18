![image](https://github.com/user-attachments/assets/da2fa754-204b-472c-b641-0e0875cb521f)# Cab-Fare-Prediction
Developed a machine learning model to predict cab fares using regression techniques. The project included data cleaning, feature engineering, and optimizing model performance for accurate predictions.
This project involves building a machine learning model to predict cab fares based on a dataset containing various features such as pickup and drop-off locations, date, time, and distance. The objective was to create an accurate predictive model to estimate cab fares by performing thorough data analysis, feature engineering, and model optimization.

### Key Features:
- **Data Preprocessing**: Handled missing values and cleaned erroneous data entries.
- **Feature Engineering**: Created new features like distance using the Haversine formula based on coordinates.
- **Exploratory Data Analysis (EDA)**: Visualized the data to understand distributions, outliers, and trends.
- **Modeling**: Implemented and trained regression models using Scikit-learn to make predictions.
- **Model Optimization**: Performed hyperparameter tuning to improve model accuracy.
- **Output**: Saved the model's predictions to a CSV file using Pandas for further analysis.

### Tools & Technologies Used:
- **Programming Language**: Python
- **Libraries**: Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn
- **Environment**: Jupyter Notebook
This project provided hands-on experience in data cleaning, feature engineering, regression modeling, and optimization, contributing to enhanced predictive analytics skills.

### Procedure
IMPORT OF LIBRARIES AND DATASETS
Pandas: For performing basic operations on dataset
Numpy : For mathematical calculations
Matplotlib & Seaborn: For visualizations & plots
![image](https://github.com/user-attachments/assets/5d39647a-3cc3-4fbc-b104-0d4d3e111fff)

- **change Directory**:
  ![image](https://github.com/user-attachments/assets/5761d335-abca-4156-a902-8d35da7eee19)
  - **Now load the file which i provided
    ![image](https://github.com/user-attachments/assets/203cf5e6-e0c2-48f7-9db9-0cc796f4bb4c)

  ### DATA UNDERSTANDING
  ![image](https://github.com/user-attachments/assets/793103ef-a657-49a2-bd91-f6fd65b39c80)

  ![image](https://github.com/user-attachments/assets/75b4dce3-8a2c-49b9-b753-cdbd2108cf32)

  ![image](https://github.com/user-attachments/assets/317d46a4-4131-421b-9bdd-9c9008959324)

 ![image](https://github.com/user-attachments/assets/ca92b642-a195-4f11-b6e6-c5e2d11d40df)

 ### DATA CLEANING AND MISSING VALUE ANALYSIS
![image](https://github.com/user-attachments/assets/704f164a-23ab-4b12-bd80-c191766363c9)

![image](https://github.com/user-attachments/assets/f8628786-8804-4f34-8a03-0b2f83a4e901)

![image](https://github.com/user-attachments/assets/515235bf-2991-48d4-9db2-a7c6b8c97660)

![image](https://github.com/user-attachments/assets/1f2e256b-582b-4ae6-a3aa-abd48d8e029a)

### OBSERVATIONS

An outlier in pickup_datetime column of value 43
Latitudes range from -90 to 90
Longitudes range from -180 to 180
Passenger count should not exceed 6
Few missing values and High values of fare and Passenger count are present. So, decided to remove them.

![image](https://github.com/user-attachments/assets/f5108ce8-3433-4f8c-9d73-d22924fc6e89)

![image](https://github.com/user-attachments/assets/4ecad617-53d1-41b3-86a7-9a79e47d34fb)

![image](https://github.com/user-attachments/assets/86648813-8a50-4b87-ab7c-56e9248c2781)

### observation

We can see maximum number of passanger count is 5345 which is actually not possible. So,reducing the passenger count to 6 (even if we consider the SUV.
We also need to remove passenger count having 0 value
passenger_count variable

![image](https://github.com/user-attachments/assets/2b171898-b653-47a0-b4b7-059cc9db52a6)

![image](https://github.com/user-attachments/assets/e3730bac-a33f-452f-80fc-d1b424292bb2)

- **fare_amount variable**
![image](https://github.com/user-attachments/assets/776b6f5d-36a5-4306-a55f-ef64e172ed22)

![image](https://github.com/user-attachments/assets/c9cbb347-5004-4e72-a55b-d658ec0e4a30)

![image](https://github.com/user-attachments/assets/48bf4459-cbdb-4efe-8c00-1694a87d81e0)

- **pickup_latitude and pickup_longitude variable**
  ![image](https://github.com/user-attachments/assets/1fd8d29b-4ef7-45ab-8047-b144ed6bb1b1)
No values are there in that range
![image](https://github.com/user-attachments/assets/d897f372-bbc1-4efd-96b0-3c6d5669352c)

- **Now, we cleared both the dataset (train and test) which can be further used for data analysis**

### Calculating distance based on the given coordinates
- **As we have given pickup_longitute and pickup_latitude values.So,we need to calculate the distance using the haversine formula.**
- **Haversine formula(the great circle distance between two points on the earth (specified in decimal degrees))**
![image](https://github.com/user-attachments/assets/91bbb413-1b93-4003-aab9-4cd2a13068ea)

![image](https://github.com/user-attachments/assets/9b405a2f-0dbd-4d55-b159-d6cf9a54f3ec)

![image](https://github.com/user-attachments/assets/0f0cd227-e788-44dc-854e-dfd325c88c60)

### OBSERVATIONS

- **As we can see that top 23 values in the distance variables are very high.**
- **It means more than 8000 Kms distance they have travelled.**
- **Just after 23rd value from the top, the distance goes down to 129, which means these values are showing some outliers.**
- **We need to remove these values.**

  ![image](https://github.com/user-attachments/assets/29cb9d14-57e7-4dd4-9524-effb43363a72)

  ### OBSERVATIONS

- **Now, we have splitted the pickup_datetime variable into different varaibles like month, year, day etc. Now, we dont need to have that pickup_datetime variable. Hence we can drop that.**
  ![image](https://github.com/user-attachments/assets/79958007-8b2f-4837-a72d-9037e56def4f)
  
  ![image](https://github.com/user-attachments/assets/8b2aacde-b491-4a2c-a9ed-91aede161a37)

 ### DATA VISUALIZATION
 ![image](https://github.com/user-attachments/assets/24c843f4-0dcf-44ad-bb86-f09dab49ceb1)

 ![image](https://github.com/user-attachments/assets/dd60253e-0e7d-457a-b0f5-42b56f04c17d)

 ### OBSERVATIONS

- **By seeing the above plots we can easily conclude that:**
- **Single travelling passengers are most frequent travellers.**
- **At the sametime, we can also conclude that highest Fare are coming from single & double travelling passengers.**
- ![image](https://github.com/user-attachments/assets/f5db6eb0-949d-45ba-bd52-cf7330a48f8c)
- ![image](https://github.com/user-attachments/assets/9b95837c-55d9-4eb2-849c-e4c34da206bb)
- ![image](https://github.com/user-attachments/assets/6711c2ab-41f1-4f64-925b-43c4bdf8e620)
- ![image](https://github.com/user-attachments/assets/67644e22-f090-4e3c-9695-7790e8561db7)

- **OBSERVATIONS**:
The day of the week does not seem to have much influence on the number of cabs ride.
![image](https://github.com/user-attachments/assets/8256ec37-50b3-4a03-b257-10fd7dd1c889)
![image](https://github.com/user-attachments/assets/5e379c79-51a4-45cd-8e18-5b0e709a9016)
### OBSERVATIONS
It is quite obvious that distance will effect the amount of fare.
FEATURE SCALING
![image](https://github.com/user-attachments/assets/23caa41f-5234-484b-97ef-5f702977a2d2)
![image](https://github.com/user-attachments/assets/cd2929e6-5e57-4b6c-a7de-4c39fdd323db)
![image](https://github.com/user-attachments/assets/fc4feae3-157a-4131-b9ad-7f8b246c18ff)
![image](https://github.com/user-attachments/assets/b78b2710-798c-4086-a49f-94c48ab06370)

- **Since skewness of target variable(fare_amount) is high, apply log transform to reduce the skewness**

![image](https://github.com/user-attachments/assets/771bb011-aa64-4493-9f25-f8bc59992f4b)
![image](https://github.com/user-attachments/assets/6c5f9424-0522-434c-80b7-f4f47ab04a9c)
### OBSERVATIONS
- **Here, we can see bell shaped distribution.
Hence our continous variables are now normally distributed, we will use not use any Feature Scalling technique i.e, Normalization or Standarization for our training data**

![image](https://github.com/user-attachments/assets/d814b9bb-dc8c-44aa-a9fc-0e747791201c)

### OBSERVATIONS
- **As we can see a bell shaped distribution.
Hence our continous variables are now normally distributed, we will use not use any Feature Scalling technique. i.e, Normalization or Standarization for our test data.**

![image](https://github.com/user-attachments/assets/373df363-cc28-4dc7-a995-20bfc4b6b5e0)

### DECISION TREE MODEL

![image](https://github.com/user-attachments/assets/6b614610-59c6-4e81-aae9-56e2bddfddd1)

### RANDOM FOREST MODEL

![image](https://github.com/user-attachments/assets/35a62b91-0153-4bf1-b999-c48e8b2f87cd)

### GRADIENT BOOSTING
![image](https://github.com/user-attachments/assets/38c398b6-875c-4dc8-a7ba-2816591a9939)

### OPTIMIZATION OF RESULTS ( with PARAMETERS TUNING)
![image](https://github.com/user-attachments/assets/cd9728b2-c657-40c4-b85d-cc30a299295f)

### Random Haperparameter Grid
![image](https://github.com/user-attachments/assets/1726eeeb-1f3a-499c-a35d-881d5d460325)
![image](https://github.com/user-attachments/assets/196bce61-cfc9-40c3-a4f1-079bfc5c70ca)
![image](https://github.com/user-attachments/assets/a7954abd-7f25-4441-a1dc-2f573952567e)
![image](https://github.com/user-attachments/assets/86f4900a-983f-4b86-8139-06f32cbdeb1e)

### FARE PREDICTION (from cleaned and processed test dataset)
- **We already have cleaned and processed test and training dataset.
Hence, we will be predicting using grid search CV for Random Forest Model.**
![image](https://github.com/user-attachments/assets/acb13b43-dbdd-4d57-8d85-f49fd84c3652)
![image](https://github.com/user-attachments/assets/7f763ed3-08ef-4224-8a87-0cafb90386e1)

### Save the data in new file.
![image](https://github.com/user-attachments/assets/c1041ded-a301-412c-a078-9cd2b2c98204)












  













  



  




  





















 

  

  






