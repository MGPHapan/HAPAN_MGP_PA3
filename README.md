# HAPAN_MGP_PA3

### PROBLEM 1
- We need Pandas to handle the dataset.  
- We use .read_csv() to load cars.csv into a DataFrame.  
- We use .head() and .tail() to preview the first and last 5 rows.  
- Output: The DataFrame, first 5 rows, and last 5 rows of the dataset.  

```Python
import pandas as pd             # Import Pandas in library

cars = pd.read_csv('cars.csv')  # Load dataset into a DataFrame
cars                            # Display dataset

cars.head()                     # Display first 5 rows
cars.tail()                     # Display last 5 rows
```

### PROBLEM 2
- We need .iloc[] to select columns by position. 1::2 means start at column 1 and take every second column (odd-numbered).  
- We use .head() to show only the first 5 rows of this selection.  
- We need .loc[] to filter rows by conditions or labels.  
- Output: Subsets of the DataFrame according to the conditions.  

```Python
import pandas as pd                                     # Import Pandas in library

cars = pd.read_csv('cars.csv')                          # Load dataset into a DataFrame
cars                                                    # Display dataset

oc = cars.iloc[:, 1::2]                                 # Select odd-numbered columns (index 1, 3, 5, …)
result = oc.head()                                      # Display first 5 rows of selected columns
result

cars[0:1]                                               # Display the row for Mazda RX4

cars.loc[cars['Model']=='Camaro Z28', ['Model','cyl']]  # Show cylinders of Camaro Z28

cars.loc[[1,28,18],['Model','cyl','gear']]              # Show cylinders & gear for 3 specific models
```

VERSION 2
