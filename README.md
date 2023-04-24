# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file

# CODE

```
import pandas as pd
df=pd.read_csv('/content/Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
df1 = pd.read_csv("/content/data.csv")
df1.head()
df1['Ord_1'].unique()
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
df2 = pd.read_csv("/content/titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```

# OUPUT

![OUT1](https://user-images.githubusercontent.com/119477857/234037532-818dfa6e-f39f-4693-b6c6-dd3eb2249bcb.png)

![OUT2](https://user-images.githubusercontent.com/119477857/234037595-f1b8e1ad-cc5d-4dfc-b459-94984a4dfbc8.png)

![OUT3](https://user-images.githubusercontent.com/119477857/234037640-56ee27b7-a0ba-4236-beac-eafd7db53497.png)

![OUT4](https://user-images.githubusercontent.com/119477857/234037688-9ca02dfd-d0d9-4680-b2ff-166423631493.png)

![OUT5](https://user-images.githubusercontent.com/119477857/234037733-c804cec2-214f-470f-b50d-1db597aa08ac.png)

![OUT6](https://user-images.githubusercontent.com/119477857/234037766-4d2361c1-849a-4dd6-91cb-fceba960b35b.png)

![OUT7](https://user-images.githubusercontent.com/119477857/234037792-ba33a9b4-6231-4de9-8c40-a655807a845b.png)

![OUT8](https://user-images.githubusercontent.com/119477857/234037838-5d7380a1-e397-47bf-bdf8-cbaf2407f8b5.png)

![OUT9](https://user-images.githubusercontent.com/119477857/234037868-f78b1a09-5d9a-4c3d-a47c-35a6a7219c7e.png)

![OUT10](https://user-images.githubusercontent.com/119477857/234037907-4240d306-716f-4065-b467-ce7336151959.png)

![OUT11](https://user-images.githubusercontent.com/119477857/234037946-ba362714-182d-4860-bcf5-c322a05dd034.png)

![OUT12](https://user-images.githubusercontent.com/119477857/234037977-44763914-27a9-485a-aefe-5c08857931f4.png)

# RESULT
The Feature Generation process was performed and saved the data to a file.
