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
NAME: VAISHNAVIDEVI V


REG NO:212223040230
```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/5ebc90bd-e2c7-44f7-bea0-aaa3a79e73fe)
```
df=sns.load_dataset('tips')
df
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/72459e98-f5ea-4bb4-a7a2-a6a44c9f763d)
```
sns.lineplot(x='total_bill',y='tip',data=df,hue='sex',linestyle='solid',legend='auto')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/0df857a5-6fd8-4cd7-8cc4-4afac12569d4)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-Line Plot')
plt.xlabel('X Label')
plt.ylabel('Y Lbel')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/878a2de5-5e0e-48a2-a86b-30641c9106e4)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/1259f51f-5be7-4cbb-963b-e22417e22bbc)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/25e619ff-5674-463c-83ef-6db4bcf71b4c)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/a7821d08-b812-4d0a-a31b-d2d8d2c4348e)
```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/d420004b-4947-4982-8822-8e091d4c2556)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/6af33110-1f33-4ee0-9ad8-067c8c344995)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/72e604dd-914f-4d4e-a8be-d2cc6572b28d)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/8b942432-e331-4f8c-bae7-74b18939e108)
```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/e264d020-9594-48e3-b154-6f49edc043dc)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/18efe9cb-616e-446c-9c58-5cdd72a4be21)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/8c280caa-0672-49c4-86d4-0987726ad754)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/dda607c5-9719-4277-b152-38fbd0f9ce47)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/e199b39b-099c-4ae5-92fd-670f3ea6339a)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/aca2c18f-b186-4cb5-bd46-83bbb4736c98)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/876ce9b6-03d2-4ce8-ba2a-4e81fd87a53f)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/e215a4d8-5cdc-4912-9674-67637911fc62)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/bb4d692b-8293-48d4-b634-20ab0e01921c)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/ec85ccb3-2f33-4f55-9289-580309acb24f)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/7e7b1cea-ee95-44e7-a9a9-882368562b43)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/d4e4842c-e5d4-4db6-8c64-1aa72e29ba39)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/05b28957-4959-41a7-b222-ecf9cbd39141)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/805b0432-424f-4f07-9c53-250059b27be4)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/9fb6c87b-fe9c-4c73-b7f8-6758b9f5c37f)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/Kalpanareshma/EXNO-6-DS/assets/122040453/12f0265a-2d04-4087-adcb-1778588da21e)

# Result:
 Thus, all the data visualization techniques of seaborn has been implemented.
