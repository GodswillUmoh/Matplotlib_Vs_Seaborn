# Matplotlib_Vs_Seaborn
The two are python libraries us for visualization. Some will ask which should I use. The answer is not necessarily yes or no.
Both complement each other and very useful in what the programmer whats to achieve. In this report, I run visuals with Matplotlib and seaborn.

## Defining The terms
> Matplotlib is a widely used Python library for data visualization. Also, Seaborn is a Python data visualization library built on top of Matplotlib. It provides a high-level interface for creating visually appealing and informative statistical graphics

## Key Difference
> Matplotlib provides the foundation for creating plots and is more flexible but requires more customization.
> Seaborn offers a simpler, high-level interface for creating complex plots with minimal effort.

## Displaying some of the python codes for Matplotlib
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

