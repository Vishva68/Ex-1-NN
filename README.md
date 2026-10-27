<H3>ENTER YOUR NAME VISHVANANDH N</H3>
<H3>ENTER YOUR REGISTER NO. 212224240186</H3>
<H3>EX. NO.1</H3>
<H3>DATE 27-10-2026</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
import pandas as pd
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

# Read dataset
data = pd.read_csv("carsemission.csv")
print(data.head())

# Check missing values
print(data.isnull().sum())

# Handle missing values
data.fillna(data.mean(numeric_only=True), inplace=True)

# Check duplicates
print(data.duplicated())

# Describe data
print(data.describe())

# Normalize numerical data
scaler = MinMaxScaler()
df1 = pd.DataFrame(scaler.fit_transform(data[['Volume', 'Weight', 'CO2']]),
                   columns=['Volume', 'Weight', 'CO2'])
print(df1)

# Split input and output
X = pd.get_dummies(data[['Car', 'Model', 'Volume', 'Weight']])
y = data['CO2']

# Training and testing
print("Training data:")
print(X_train.head())
print(y_train.head())

print("Testing data:")
print(X_test.head())
print(y_test.head())

print("Length of X_test:", len(X_test))

```


## OUTPUT:
<img width="850" height="450" alt="image" src="https://github.com/user-attachments/assets/0464e14b-1c2d-4d27-baef-070f8e9f28be" />
<img width="795" height="447" alt="image" src="https://github.com/user-attachments/assets/15b69a95-d261-4fb0-a68b-528d012133d2" />
<img width="817" height="442" alt="image" src="https://github.com/user-attachments/assets/a7071bda-3ab1-44d6-b60e-ccdcf021eb9e" />
<img width="716" height="445" alt="image" src="https://github.com/user-attachments/assets/3762f0f8-e2a7-42f8-8a9e-00e499be5f8e" />
<img width="660" height="447" alt="image" src="https://github.com/user-attachments/assets/fec0032e-4f8f-4fa1-89f6-e57225f52f83" />
<img width="841" height="452" alt="image" src="https://github.com/user-attachments/assets/b980c422-ea3a-4e2f-a505-868e96b04b3a" />
<img width="832" height="457" alt="image" src="https://github.com/user-attachments/assets/7e9fb525-658e-426e-a6fb-d48463a6fb98" />
<img width="846" height="455" alt="image" src="https://github.com/user-attachments/assets/9ad5b964-763e-4852-8bb6-d72a4a6e4a88" />
<img width="832" height="437" alt="image" src="https://github.com/user-attachments/assets/8662582f-aa53-4b26-b668-7b2e0d7c3172" />
<img width="822" height="460" alt="image" src="https://github.com/user-attachments/assets/400aab0f-1470-4a28-a08c-16dd5f109edf" />
<img width="797" height="447" alt="image" src="https://github.com/user-attachments/assets/b9854c2c-6ec1-45e7-a3f1-3957dd1e9cfd" />

















## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.




