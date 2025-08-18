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
```python

import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('/content/Crypto Data Since 2015.csv')
df['Date'] = pd.to_datetime(df['Date'])
df.set_index('Date', inplace=True)
monthly_bitcoin = df['Bitcoin (USD)'].resample('ME').mean()
plt.figure(figsize=(10,5))
plt.plot(monthly_bitcoin.index, monthly_bitcoin.values, marker='o')
plt.title("Bitcoin Yearly Average Price")
plt.xlabel("Year")
plt.ylabel("Bitcoin (USD)")
plt.show()

```

# OUTPUT:

<img width="887" height="470" alt="image" src="https://github.com/user-attachments/assets/1b0726c5-31da-4da2-89df-20c697299bf4" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
