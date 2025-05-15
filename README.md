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

import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

df = sns.load_dataset('tips')  


print("Dataset Preview:")
print(df.head())


# 1. Count plot for categorical data
plt.figure(figsize=(6,4))
sns.countplot(x='day', data=df)
plt.title("Count of Records by Day")
plt.show()
![image](https://github.com/user-attachments/assets/349406d6-070c-4d95-b95f-58ba510bd6c6)
![image](https://github.com/user-attachments/assets/4d536a4f-cad2-4a11-910f-ad4804839d27)



# 2. Histogram of total bill
plt.figure(figsize=(6,4))
sns.histplot(df['total_bill'], kde=True, color='green')
plt.title("Histogram of Total Bill")
plt.show()
![image](https://github.com/user-attachments/assets/7e0ed4e2-4fc8-49e5-92a5-48252e481d6c)


# 3. Box plot to see distribution by gender
plt.figure(figsize=(6,4))
sns.boxplot(x='sex', y='total_bill', data=df)
plt.title("Boxplot of Total Bill by Gender")
plt.show()
![image](https://github.com/user-attachments/assets/565daf02-bcfb-4a5b-9fac-2a3585189d33)


# 4. Violin plot to observe distribution
plt.figure(figsize=(6,4))
sns.violinplot(x='day', y='total_bill', hue='sex', data=df, split=True)
plt.title("Violin Plot of Total Bill by Day and Gender")
plt.show()
![image](https://github.com/user-attachments/assets/c39cd7bb-b672-486e-968f-dc4fbec0f585)


# 5. Pairplot to examine relationships
sns.pairplot(df, hue='sex')
plt.suptitle("Pairplot of Tips Dataset", y=1.02)
plt.show()
![image](https://github.com/user-attachments/assets/ba2545e2-880d-4b29-bc5c-1e1b2de743a5)


# 6. Heatmap for correlation
plt.figure(figsize=(6,5))
sns.heatmap(df.corr(numeric_only=True), annot=True, cmap='coolwarm')
plt.title("Correlation Heatmap")
plt.show()
![image](https://github.com/user-attachments/assets/a0b90262-d34f-4030-b08b-6c58d07c6b44)

# 7. Scatter plot with regression line
plt.figure(figsize=(6,4))
sns.regplot(x='total_bill', y='tip', data=df)
plt.title("Regression Line between Total Bill and Tip")
plt.show()
![image](https://github.com/user-attachments/assets/1a36700c-fa62-4e37-a8de-57e81d1c5c14)

# 8. Bar plot
plt.figure(figsize=(6,4))
sns.barplot(x='sex', y='tip', data=df)
plt.title("Average Tip by Gender")
plt.show()

# 9. Swarmplot for detailed distribution
plt.figure(figsize=(6,4))
sns.swarmplot(x='day', y='tip', data=df)
plt.title("Swarmplot of Tips by Day")
plt.show()
![image](https://github.com/user-attachments/assets/84677590-35be-4161-9897-5047ab96df0e)



# Result:
 Thus data visualization using seaborn python library for the given datas are performed successfully.

