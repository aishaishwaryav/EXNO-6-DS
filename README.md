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
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1225" height="202" alt="image" src="https://github.com/user-attachments/assets/552b51b8-fa90-4494-8fc3-391b370dbd0d" />
 
1.LINE PLOT
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="616" height="451" alt="image" src="https://github.com/user-attachments/assets/2cee6035-880d-4c21-9781-4e5df6d18565" />

2.MULTI LINE PLOT

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="622" height="462" alt="image" src="https://github.com/user-attachments/assets/d33cd248-dba8-4061-b440-f1e4cb0351da" />

TO VISUALIZE RELATIONSHIPS

1.BAR CHART

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="787" height="517" alt="image" src="https://github.com/user-attachments/assets/8c890715-d449-4b24-bf66-f63ca1b8f662" />

2.SCATTER PLOT

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="704" height="477" alt="image" src="https://github.com/user-attachments/assets/9f369d7d-6e51-4674-a33c-02dffc3e6757" />

3.BUBBLE CHART

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="721" height="463" alt="image" src="https://github.com/user-attachments/assets/6534da6f-ce38-48c2-9413-6cd0278bb590" />

TO CAPTURE DISTRIBUTIONS

1.HISTOGRAM

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="719" height="465" alt="image" src="https://github.com/user-attachments/assets/014f0376-7db8-4672-bfea-d511e20715ad" />

2.BOX PLOT

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="699" height="501" alt="image" src="https://github.com/user-attachments/assets/e8159af8-3dd2-4e7f-b22d-c3ad2e399721" />

3.VIOLIN PLOT

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="749" height="469" alt="image" src="https://github.com/user-attachments/assets/142c065d-05fe-49b1-8353-e83aab1ede3c" />


4.DENSITY PLOT

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="747" height="470" alt="image" src="https://github.com/user-attachments/assets/6a33bf4c-5f06-417c-9947-2c63d48737e7" />


5.HEATMAP

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="695" height="511" alt="image" src="https://github.com/user-attachments/assets/13b3cb89-bb6e-4afc-9c1e-e0a766c1be8b" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
