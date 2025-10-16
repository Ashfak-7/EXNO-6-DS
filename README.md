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

```python
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```

<img width="638" height="447" alt="435469968-46974ab5-7fc7-40fb-a9b2-1616f16727bc" src="https://github.com/user-attachments/assets/13876145-d014-4c5e-b698-652daf216ae6" />


```python
df=sns.load_dataset("tips")
df
```

<img width="552" height="404" alt="435469992-772058e7-b9c9-4946-af42-d4406deedba8" src="https://github.com/user-attachments/assets/30b105a0-4267-4d8d-b184-34b31a04131c" />

```python
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```

<img width="655" height="461" alt="435470015-00076ba5-5f2a-4c33-9423-e06f766c1128" src="https://github.com/user-attachments/assets/41433616-e486-40b4-bf23-431e19d650cc" />


```python
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-:Line Plot')
plt.xlabel('X-Label')
plt.ylabel('Y-Label')
```

<img width="654" height="492" alt="435470033-3b9eb27a-c0b9-457f-a02f-8086f94e405f" src="https://github.com/user-attachments/assets/6db04fb9-8509-4994-b498-783752eb15b2" />


```pythonn
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

<img width="859" height="658" alt="435470086-ba675234-156c-4f40-ba00-b91adbf8c295" src="https://github.com/user-attachments/assets/4cdc2d66-4808-4ba7-a649-d10fbb30ad6c" />


```python
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```

<img width="616" height="445" alt="435470133-a1202464-30c2-4c24-8684-f980c4dc569d" src="https://github.com/user-attachments/assets/36f5b068-a21f-4d70-aa76-bee9461f7f68" />


```python
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```

<img width="689" height="484" alt="435470153-064c936b-69b7-4b04-9139-92e04b3c7ddb" src="https://github.com/user-attachments/assets/d99026e8-f1e5-4ef1-a48f-bbce736a7550" />


```python
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset (2).csv")
tit
```

<img width="871" height="750" alt="435470206-75d93cfc-103e-4935-bb9b-529b7e02a18d" src="https://github.com/user-attachments/assets/97880b06-fe2d-452e-8757-2c768de61a47" />

<img width="830" height="164" alt="435470222-0f6680c0-650a-4cb6-b7a3-9228272f82de" src="https://github.com/user-attachments/assets/329d9889-31c1-430c-9ed9-61dd61487d5e" />


```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```

<img width="882" height="594" alt="435470279-5aa1f428-1294-42a2-9696-3f54053a37ef" src="https://github.com/user-attachments/assets/2f1e7744-7fbd-4091-b10b-67f6eeac3892" />


```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')
plt.title("Fare of Passenger by Embarked Town,Divided by Class")
```

<img width="834" height="501" alt="435470294-52cf845e-40a3-498e-ae6f-77defcd62af5" src="https://github.com/user-attachments/assets/12f7be0f-8877-4e46-be74-499e15906d63" />

```python
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

<img width="697" height="492" alt="435470313-4512ff1c-abe3-4d2f-97b9-81c67965af87" src="https://github.com/user-attachments/assets/f88f36b8-20e8-4317-a543-e09cb2c2c24d" />


```python
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var
```

<img width="272" height="446" alt="435470331-a288772d-c3c9-489a-b964-fcea264cf95e" src="https://github.com/user-attachments/assets/67618e54-fe78-4016-8f09-3615a54314ec" />

```python
sns.histplot(data=num_var,kde=True)
```

<img width="688" height="463" alt="435470353-eb6e12be-8dc3-4375-a00b-69ee220fce25" src="https://github.com/user-attachments/assets/80494a97-54cf-40e4-b0fa-18faba30a424" />


```python
sns.histplot(data=tit,x="Pclass",hue="Survived",kde=True)
```

<img width="659" height="455" alt="435470389-6411df41-8b23-4ce5-ba97-160d90cc6099" src="https://github.com/user-attachments/assets/35d0a901-d7ed-4611-a6bf-5723b0c3061d" />


```python
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
```

<img width="659" height="367" alt="435470408-557baafa-c44d-46ab-b03d-0e01c5db5220" src="https://github.com/user-attachments/assets/f13c5267-5b90-4899-9744-d9ab19ef5583" />


```python
sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Student Marks')
```

<img width="859" height="500" alt="435470420-cc753817-cd75-4cf9-9409-3dce7023c06f" src="https://github.com/user-attachments/assets/77368f59-f3ab-4e45-81b0-568687e0ceb3" />


```python
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```

<img width="648" height="463" alt="435470443-b6550aa1-ea2c-4978-ae0e-cff9920d6325" src="https://github.com/user-attachments/assets/8042125b-eb99-4236-9c9a-a0740ce9e021" />

```python
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
            whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```

<img width="691" height="475" alt="435470462-206df3e2-54af-4abd-b2e5-a31311276f92" src="https://github.com/user-attachments/assets/f80fe13d-3582-467c-9ce1-337e6e4cd5e5" />

```python
sns.boxplot(x='Pclass',y='Age',data=tit,palette='rainbow')
plt.title("Age by Passenger Class,Titanic")
```

<img width="830" height="576" alt="435470482-81ddc5a1-6823-479b-b360-fc21fc88eaa5" src="https://github.com/user-attachments/assets/7880a602-1848-408e-bc18-8491b93b0f5a" />

```python
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set3",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

<img width="676" height="472" alt="435470496-ab7e35ac-a698-4216-a3bb-dbff277f49bb" src="https://github.com/user-attachments/assets/68b5c38c-d05e-4bce-9a19-21ad254170e9" />

```python
import seaborn as sns
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip)
```

<img width="710" height="476" alt="435470521-57d0dbbd-da57-48ba-a7fe-7e548ab2b107" src="https://github.com/user-attachments/assets/d5d83649-daf0-4fe8-afbf-be0fc6be4241" />


```python
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```

<img width="640" height="467" alt="435470548-48df3249-f2bc-4f44-8e33-7ed92a07dc8f" src="https://github.com/user-attachments/assets/38093ce0-5128-4aab-837a-85422bb661c6" />



```python
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x="tip",y="day",data=tip)
```

<img width="736" height="461" alt="435470571-88ed24c3-72ab-41da-bc86-bc6cbb5424ab" src="https://github.com/user-attachments/assets/cb4b4672-d8cd-4c9c-85b4-f799a6b73900" />


```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set3',alpha=0.8)
```

<img width="730" height="462" alt="435470590-db1d9b73-a36f-4782-bbc4-c242755e029a" src="https://github.com/user-attachments/assets/082c714a-3dd7-4279-a9e8-2f183eafa762" />


```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```

<img width="701" height="461" alt="435470615-ef326aa4-2bcc-4ab9-b274-b1855378c6cf" src="https://github.com/user-attachments/assets/3a89cae7-c26c-4092-a72b-f36c046f658b" />

```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```

<img width="719" height="487" alt="435470663-3ff8d8d7-8b00-4330-9ce5-d1a7cb4aad7e" src="https://github.com/user-attachments/assets/6ece8878-c2f8-489f-832b-b668aaf10680" />


```python
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted:\n")
print(data)
```

<img width="342" height="220" alt="435470674-1fbe9442-4177-4a2f-84bd-ffd61ec0d776" src="https://github.com/user-attachments/assets/89302be3-5ac9-4bee-b740-88cb2e888b38" />

```python
hm=sns.heatmap(data=data)
```

<img width="631" height="423" alt="435470691-d50fead1-94c9-42dd-8af8-544edc2673d5" src="https://github.com/user-attachments/assets/8e31c92e-315c-4fde-9318-f9fb4aa04b6e" />

```python
tips=sns.load_dataset('tips')
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)
```

<img width="614" height="450" alt="435470717-3ce516bc-0d85-405f-b09e-a3709bff6ab2" src="https://github.com/user-attachments/assets/1da09ea3-10b1-480f-b48c-290bdb78a7a5" />

# Result:

Data Visualization using seaborn python library for the given datas has been performed successfully.

