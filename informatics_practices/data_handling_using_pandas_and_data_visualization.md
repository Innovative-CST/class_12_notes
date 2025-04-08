# Data Science 
Data science or data analysis, it is the process of analysing a large set of data points to get answer to questions related to that data set.

# Pandas
Pandas (Panel Data, and Python Data Analysis) is a python library that makes data science or data analysis easy and effective. 
It is the most famous python library for data science that offers powerful and flexible data structures which makes data analysis and manipulation easy.
It is a high level data manipulation tool developed by [Wes McKinney](https://wesmckinney.com).

# Features of Pandas
- Pandas can handle several tasks related to data processing & has the following silent features:
- It can read or write in many different data formats.
- Columns from Pandas data structure can be deleted or inserted.
- It supports groupby operation for data transformation and allows high performance merging and joining of data.
- It has functionality to find and fill missing data.
- It allows us to apply operation to independent groups within the data.
- It supports recheping of data into different forms.

**Note**: Installing process may differ due to operating system. So please install the python according to your operating system or you can visit [Beginners Guide for installing python](https://wiki.python.org/moin/BeginnersGuide/Download)

**Note**: If you don't know how to install pandas you can search about it on YouTube because these steps may very according to the system.

# Data structures in pandas
A data structure is a way of storing and organizing data in a computer so that it can be accessed and operated on efficiently.

Pandas provides and deals with the three data structures:

- **Series**: It is a one-dimensional structure of storing homogeneous (same data type), mutable data.
- **Data Frame**: It is a two-dimensional structure of storing heterogeneous (multiple data types), mutable data.
- **Panel**: it is a three dimensional way of storing data. 

## Series
Series in pandas is like a one-dimensional structure capable of holding homogeneous data of any type like string, int, float, Python objects.
The data applied to Series method can be anyone of the following types:

- Sequence
- Scalar
- A dictionary
- A mathematical data
- Numpy & ndarray

### Creating Series object
#### Creating Empty Series

A basic series which can be created is empty series.
This is created just by calling Series method with no parameters.


```python
import pandas
sr = pandas.Series()
```

Output:
```cmd
Series([], dtype: float64)
```

#### Creating Series with Arguments

Syntax:
```cmd
pandas.Series(<data>, <index>)  
pandas.Series(data = <data>, index = <index>)
```

#### Create a series using 2 different lists

```python
import pandas as pd
names = ["Aman", "Madhu", "Sahil"]
scores = [85, 90, 95]
sr = pandas.Series(scores, names)
print(sr)
```
Output:
```output
Aman     85  
Madhu    90  
Sahil    95  
dtype: int64
```

#### Creating series using range method and for-loop

Example Code:

```python
import pandas
days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]
index = [x for x in range(1, 8)]
series = pandas.Series(days, index)
print(series)
```
Output:
```output
1       Sunday
2       Monday
3      Tuesday
4    Wednesday
5     Thursday
6       Friday
7     Saturday
dtype: object
```
Example Code:
```python
import pandas
days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]
series = pandas.Series(days)
print(series)
```
Output:
```output
0       Sunday
1       Monday
2      Tuesday
3    Wednesday
4     Thursday
5       Friday
6     Saturday
dtype: object
```

#### Creating a series using missing value
Example Code:
```python
import numpy
import pandas
series = pandas.Series([1,2,3,numpy.nan])
print(series)
```
Output:
```output
0    1.0
1    2.0
2    3.0
3    NaN
dtype: float64
```

**Note**: NaN → Not a number

#### Creating a series using scaler or constant values
Example Code:
```python
import pandas as pd
students = ["Ankur", "Karan", "Jay"]
sr = pd.Series("Good Day", index=students)
print(sr)
```
Output:
```output
Ankur    Good Day
Karan    Good Day
Jay      Good Day
dtype: object
```

#### Creating a Series from dictionary
Example Code:
```python
import pandas

months = {
    "January" : 31,
    "February" : 28,
    "March" : 31
}
sr = pandas.Series(months)
print(sr)
```
Output:
```output
January     31
February    28
March       31
dtype: int64
```
**Note**: Order may vary in dictionary.

#### Creating a Series using mathematical expression
Example Code:
```python
import pandas
import numpy

s1 = numpy.arange(10, 15, 1)
sr = pandas.Series(s1, s1 * 2)
print(sr)
```
Output:
```output
20    10
22    11
24    12
26    13
28    14
dtype: int32
```

#### Creating a Series using numpy ndarray
Example Code:
```python
import pandas
import numpy

s1 = numpy.arange(3, 13, 3.5)
print(s1)
sr = pandas.Series(s1)
print(sr)
```
Output:
```output
[ 3.   6.5 10. ]
0     3.0
1     6.5
2    10.0
dtype: float64
```