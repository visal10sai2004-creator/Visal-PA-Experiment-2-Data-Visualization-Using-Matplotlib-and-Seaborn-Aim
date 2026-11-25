## Experiment 2: Data Visualization Using Matplotlib and Seaborn

## Aim

To visualize data using Matplotlib and Seaborn libraries.

## Algorithm

1.  **Start.**

2.  Import the Matplotlib and Seaborn libraries.

3.  Load data into a Pandas DataFrame.

4.  Plot a histogram for age distribution using `plt.hist()`.

5.  Plot a scatter plot for Age vs. Salary using `sns.scatterplot()`.

6.  Plot salary distribution using `sns.boxplot()`.

7.  Show the plots sequentially.

8.  **Stop.**


## Program


```

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
# Create Dataset
data = {
    'Age': [22, 25, 30, 27, 32, 38, 26, 29, 35, 40],
    'Salary': [30000,35000,40000,45000,50000,38000,42000,48000,34000,37000],
    'Salary_color': ['red','blue','orange','purple','green','yellow','lightblue','pink','brown','magenta']
}
df = pd.DataFrame(data)
print("\nDataset:")
print(df)
# Histogram
plt.figure(figsize=(6,4))
plt.hist(df['Age'], bins=6, color='orange', edgecolor='black')
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
# Scatter Plot
plt.figure(figsize=(6,4))
sns.scatterplot(x='Age', y='Salary', data=df, color='purple')
plt.title('Age vs Salary')
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()
# Pie Chart
plt.figure(figsize=(6,6))
plt.pie(
    df['Salary'],
    labels=df['Age'],
    colors=df['Salary_color'],
    autopct='%1.1f%%'
)
plt.title('Salary Distribution by Age')
plt.show()
# Box Plot
plt.figure(figsize=(6,4))
sns.boxplot(x=df['Salary'], color='gold')
plt.title('Salary Distribution')
plt.xlabel('Salary')
plt.show()


```

## Output

```

Dataset:
   Age  Salary Salary_color
0   22   30000          red
1   25   35000         blue
2   30   40000       orange
3   27   45000       purple
4   32   50000        green
5   38   38000       yellow
6   26   42000    lightblue
7   29   48000         pink
8   35   34000        brown
9   40   37000      magenta

```


<img width="536" height="393" alt="image" src="https://github.com/user-attachments/assets/e43a0e3b-6acc-475e-81d2-c08a2175e4fe" />


<img width="558" height="393" alt="image" src="https://github.com/user-attachments/assets/2035f42d-3e18-4108-a143-197bd6f5a4c1" />


<img width="481" height="504" alt="image" src="https://github.com/user-attachments/assets/ae6e4afa-a259-4c8d-a31b-e27ea028aa46" />


<img width="490" height="393" alt="image" src="https://github.com/user-attachments/assets/7403e0fd-37d1-4ea7-87d9-25dd47fc30e3" />


## Result 


Thus, data visualization was successfully performed using Matplotlib and Seaborn libraries in Python. The histogram was used to represent age distribution, the scatter plot showed the relationship between age and salary, the pie chart displayed salary distribution by age, and the box plot represented the salary distribution. Hence, different graphical techniques were used to understand and analyze the dataset effectively.

