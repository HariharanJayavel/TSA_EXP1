# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 17.08.2025

# AIM:
To Develop a python program to Plot a time series data ( market price of a commodity).

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```c
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
from statsmodels.tsa.seasonal import seasonal_decompose
df=pd.read_csv('/content/Crypto Data Since 2015.csv')
df.head()
x=df['Date']
y=df['Bitcoin (USD)']
plt.figure(figsize=(10,5))
plt.plot(x,y)
plt.title("Bitcoin Price Analysis")
plt.xlabel("Date")
plt.ylabel("Bitcoin (USD)")
plt.show()
```

# OUTPUT:

<img width="881" height="470" alt="image" src="https://github.com/user-attachments/assets/6ca4bea2-8028-4605-a693-f200d05ed739" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
