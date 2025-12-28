# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
import pandas as pd import seaborn as sns import matplotlib.pyplot as plt df=pd.read_csv("titanic_dataset.csv") df.head()
<img width="1032" height="178" alt="image" src="https://github.com/user-attachments/assets/14dd1474-5ff4-4d7f-bb1b-594f8c541752" />
x=[1,2,3,4,5] y=[3,6,2,7,1] sns.lineplot(x=x,y=y) plt.title('Line Plot')
<img width="659" height="533" alt="image" src="https://github.com/user-attachments/assets/f5eb9d69-f5a0-4b74-bbd3-bc644349d2c1" />
x=[1,2,3,4,5] y1=[3,5,2,6,1] y2=[1,6,4,3,8] y3=[5,2,7,1,4] sns.lineplot(x=x,y=y1) sns.lineplot(x=x,y=y2) sns.lineplot(x=x,y=y3) plt.title('Multi Line Plot')
<img width="664" height="536" alt="image" src="https://github.com/user-attachments/assets/99971ec3-dec2-44b1-8820-9db49a545762" />
plt.figure(figsize=(8,5)) sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow') plt.title("Fare Of Passenger By Embarked Town")
<img width="846" height="579" alt="image" src="https://github.com/user-attachments/assets/63e1af23-e525-4890-b434-6c59e725591b" />
sns.scatterplot(x="Age", y="Fare", data=df) plt.title('Scatterplot of Age vs Fare') plt.show()
<img width="703" height="549" alt="image" src="https://github.com/user-attachments/assets/b3e51dec-438c-45be-b8a0-189964774aaf" />
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200)) plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class') plt.show()
<img width="706" height="551" alt="image" src="https://github.com/user-attachments/assets/ceead66c-4b80-4680-a0be-a3b27faf114e" />
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/83e03ae1-af74-4513-a22f-55b3b9d0a750" />
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow') plt.title("Age By Passenger Class")
<img width="684" height="550" alt="image" src="https://github.com/user-attachments/assets/1115f738-b9f8-4b2c-b26e-bf135e470a3d" />
sns.violinplot(x="Pclass", y="Fare", data=df) plt.title('Violin Plot of Fare by Passenger Class')
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/7c755e83-cfa5-435e-a9ab-011812059f67" />
plt.show()
sns.kdeplot(data=df['Age'], shade=True) plt.title('Density Plot of Passenger Ages') plt.show()
<img width="723" height="551" alt="image" src="https://github.com/user-attachments/assets/403af563-f8d0-4ea9-bba6-e9235af17c43" />
numeric_df = df.select_dtypes(include=['float64', 'int64']) corr_matrix = numeric_df.corr() sns.heatmap(corr_matrix, annot=True, cmap='coolwarm') plt.title('Heatmap of Titanic Dataset') plt.show()
<img width="730" height="614" alt="image" src="https://github.com/user-attachments/assets/8ed4d803-5e45-43b8-ab02-6053490340aa" />

# Result:
Thus,the Data vizualization seaborn python data is successfully
