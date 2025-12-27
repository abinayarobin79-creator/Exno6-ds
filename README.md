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
 import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()

<img width="970" height="171" alt="Screenshot 2025-12-27 215513" src="https://github.com/user-attachments/assets/7ed9271d-357a-4a32-af1f-bb78244c9b04" />

x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

<img width="853" height="705" alt="Screenshot 2025-12-27 215521" src="https://github.com/user-attachments/assets/695720ce-ca33-48ba-9442-7e52a674c62a" />
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')

<img width="848" height="717" alt="Screenshot 2025-12-27 215530" src="https://github.com/user-attachments/assets/4c7615bf-c46c-4af7-8806-70632233aa41" />

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

<img width="1032" height="455" alt="Screenshot 2025-12-27 215547" src="https://github.com/user-attachments/assets/8717eaba-586f-4525-af37-986d494c3deb" />

sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

<img width="953" height="715" alt="Screenshot 2025-12-27 215555" src="https://github.com/user-attachments/assets/c888a56a-d8f9-4343-930b-4c1d1ee3848b" />

sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

<img width="939" height="700" alt="Screenshot 2025-12-27 215604" src="https://github.com/user-attachments/assets/86076f40-75ac-41c3-9358-bee763f7ef06" />

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

<img width="928" height="692" alt="Screenshot 2025-12-27 215613" src="https://github.com/user-attachments/assets/10d47d82-e177-40b4-9013-ae8817973ed5" />

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

<img width="1023" height="447" alt="Screenshot 2025-12-27 215622" src="https://github.com/user-attachments/assets/98972378-55ac-40c4-90e7-2ba900094723" />

sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

<img width="981" height="706" alt="Screenshot 2025-12-27 215631" src="https://github.com/user-attachments/assets/20fdee6d-6eeb-45b8-bb6d-6f57aac9a203" />

sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()


<img width="940" height="804" alt="Screenshot 2025-12-27 215654" src="https://github.com/user-attachments/assets/42ac7638-5fc7-4bb7-8c43-9e1fba5988c5" />

numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

<img width="986" height="789" alt="Screenshot 2025-12-27 215703" src="https://github.com/user-attachments/assets/239c910c-bb29-4c9b-8162-441b45be6038" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.


