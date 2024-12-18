# Matplotlib_Vs_Seaborn
The two are python libraries use for visualization. Some will ask which should I use. The answer is not necessarily yes or no.
Both complement each other and very useful in what the programmer wants to achieve. In this report, I run visuals with Matplotlib and seaborn.

## Defining The terms
> Matplotlib is a widely used Python library for data visualization. Also, Seaborn is a Python data visualization library built on top of Matplotlib. It provides a high-level interface for creating visually appealing and informative statistical graphics

## Key Difference
> Matplotlib provides the foundation for creating plots and is more flexible but requires more customization.
> Seaborn offers a simpler, high-level interface for creating complex plots with minimal effort.

# Displaying some of the python codes for Matplotlib
```python
'''
Some of the popular visualization for matplotlib include:
plt.plot()
plt.bar()
plt.hist()
plt.scatter
'''
# The coordinate is given as (x, y)
```

```python
import matplotlib.pyplot as plt

# Values for x and y
x = [1, 2, 3, 4]
y = [10, 30, 40, 100]
plt.plot(x, y, marker = "o", markersize=17, color="red", linestyle="dashed", linewidth=5)
plt.show()
```

## Exercise 1
> Activity 1
> You are a trainer and the following scores were recorded for the trainees:
> Chioma = [70, 80, 90, 95, 30, 89]
> David = [40, 60, 50, 45, 70, 55]
> based_score =[20, 40, 60, 70, 80, 100]
> Plot a graph using python

## Answer:
```python
import matplotlib.pyplot as plt

#You are a trainer and the following scores were recorded for the trainees:
chioma = [70, 80, 90, 95, 30, 89]
david = [40, 60, 50, 45, 70, 55]

based_score = [20, 40, 60, 70, 80, 100]
#Plot a graph using python, label='Chioma, label='David'

plt.plot(based_score, chioma, marker="o", color="red", markersize="14", label='Chioma')
plt.plot(based_score, david, marker="o", color="green", markersize="14", label='David')
plt.title("A Graph of Students scores")
plt.xlabel("Scores")
plt.ylabel("Students' Score")
plt.legend()
plt.show()
```
### [View the results of the code Here](https://colab.research.google.com/drive/11C7KOKAHf4BT18V76uzWFrnqUwdbdoNA#scrollTo=u2CdnB6sEWkC)


## Exercise 2
> Given the following: Data for multiple lines:
> x = [1, 2, 3, 4, 5],
> y1 = [1, 4, 9, 16, 25],
> y2 = [1, 2, 3, 4, 5],
> y3 = [2, 8, 20, 25, 30]

plot a graph with python

## Answer:
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [1, 4, 9, 16, 25]
y2 = [1, 2, 3, 4, 5]
y3 = [2, 8, 20, 25, 30]

plt.plot(x, y1, marker="o", color="red", markersize="14", label='y1')
plt.plot(x, y2, marker="o", color="green", markersize="14", label='y2')
plt.plot(x, y3, marker="o", color="purple", markersize="14", label='y3')
plt.title("A Graph of x against y1, y2, y3")
plt.xlabel("X Values")
plt.ylabel("Y Values")

plt.legend()
plt.show()
```
### [View the results of the code Here](https://colab.research.google.com/drive/11C7KOKAHf4BT18V76uzWFrnqUwdbdoNA#scrollTo=u2CdnB6sEWkC)


## Exercise 3
>Given the set of dataset, plot a bar, histogram with py.

## Answer:
```python
#Creating a Bar Chart

grades = ['F', 'P', 'C', 'B', 'A']
cum_scores = [30, 40, 50, 60, 70]

#Plotting bar
plt.bar(grades, cum_scores, color='orange')
#plt.hist(cum_scores, bins=6, color='purple')


#labels
plt.xlabel('Students Grades')
plt.ylabel('Cummulative Scores')
plt.title('Students Grading')

#To show
plt.show()
```
### [View the results of the code Here](https://colab.research.google.com/drive/11C7KOKAHf4BT18V76uzWFrnqUwdbdoNA#scrollTo=u2CdnB6sEWkC)


## Exercise 4
Given the set of dataset, plot a subplot for y1 and y2

## Answer:
```python
import matplotlib.pyplot as plt

#Dataset
x = [1, 2, 3, 4, 5]
y1 = [1, 4, 9, 16, 25]
y2 = [1, 2, 3, 4, 5]

#Creating the subplot
fig, (fig1, fig2) = plt.subplots(1, 2) #arrange in 1 row 2 column

#first plot
fig1.plot(x, y1, color='purple')
fig1.set_title('Y1 Scores')

#second plot
fig2.plot(x, y2, color= 'green')
fig2.set_title('Y2 Scores')

#Set Overall Title
fig.suptitle("A Graph of x and Y1, Y2")

#plt.savefig('My figure')
#show
plt.show()
```
### [View the results of the code Here](https://colab.research.google.com/drive/11C7KOKAHf4BT18V76uzWFrnqUwdbdoNA#scrollTo=u2CdnB6sEWkC)

# Displaying some of the python Exercises for Seaborn
> Dataset Used is the Iris data that is preloaded in the seaborn library
```python
'''
Some of the popular visualization for seaborn include:
sns.barplot()
sns.displot()
sns.heatmap()
sns.boxplot()

to have multiple color, one can use the palette (e.g palette='rocket', Set1, 2, )
The hue function works like legend in powerBI by grouping for visualization
'''
# The coordinate is given as (x, y)
```

## Seaborn Exercises
Using the Iris Dataset, carryout the following visualization and provide meaningful insights to the data. The task are:

> a). Load the dataset
b). Print the Top 5 and Bottom 5 rows of the dataset
c). Print the number of rows and columns in the dataset
d). Plot a bar chat to visualize data
e). Plot a distribution graph to visualize data
f). Produce a chart to show correlation across data
g). Produce a Chart using the count function
h). create a box plot.

## Answer to the Exercises
### [To view the result of the Codes, Click Here](https://colab.research.google.com/drive/11C7KOKAHf4BT18V76uzWFrnqUwdbdoNA#scrollTo=rCW2jNqZOzLw)

```python
#  a). Load the dataset
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

#using a preloaded data in seaborn
dataset = sns.load_dataset('iris')

b). Print the Top 5 
dataset.head()
```
```python
# Print Bottom 5 rows of the dataset
dataset.tail()
```
```python
# c). Print the number of rows and columns in the dataset
# Printing the shape of the Iris Data
dataset.shape
#results (150, 5), that is 150 rows and 5 columns
```

```python
# Plot a bar chat to visualize data
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

sns.barplot(x= 'species', y = 'sepal_width', data = dataset)
```

```python
# Plot a distribution graph to visualize data
# e) Distribution plot for sepal_length
sns.displot(dataset.sepal_length, bins= 10, color="red")
plt.show()
```

```python
# Produce a chart to show correlation across data
# Plotting with heatmap
# Produce a chart to show correlation across data
# Plotting with heatmap

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

#using a preloaded data in seaborn
# We can exclude the string data being the last column
dataset.info()

#Exclude the last column being string
num_var = dataset.iloc[:, :-1]
num_var.head()

#Plotting the heatmap
sns.heatmap(num_var.corr(), cbar=True, linewidths=0.5)

```
> To interpret heatmap(), pay attention to the dark and light spots; the dark often show low correlation while light shows high correlation considering the scale by the side of the graph.


```python
# Produce a Chart using the count function
# Produce a Chart using the count function
# in this case we will like to count the species, vertical
sns.countplot(x='species', data=dataset, palette= 'rocket')
plt.show()

# Produce a Chart using the count function
# in this case we will like to count the sepal_length, showing horizontally
sns.countplot(y='sepal_length', data=dataset, palette= 'rocket')
plt.show()

# Adding hue to the graph
sns.countplot(x='petal_width', data=dataset, palette= 'rocket', hue='species')
plt.show()
```

> boxplot is an excellent tool for exploring and summarizing differences in y-axis variable across the x-axis variable. In this analysis, each boxplot represents the distribution of sepal_length for a specific species. _The line inside each box is the median (50th percentile) of sepal_length for that species._
> __Spread of Data__: The length of the box represents the interquartile range (IQR), which is the range between the 25th percentile (lower edge of the box) and the 75th percentile (upper edge of the box). _A smaller box indicates that most of the values are tightly clustered around the median._

> __Outliers__: Points outside the "whiskers" (lines extending from the box) are considered outliers. Whiskers extend to approximately 1.5 times the IQR beyond the 25th and 75th percentiles.
```python
# h). create a box plot.
sns.boxplot(x='species', y='sepal_length', data=dataset)
plt.show()
```
