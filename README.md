# HAPAN_MGP_PA3

### PROBLEM 1

// Import pandas
    
    import pandas as pd

// Load .csv file
    
    cars = pd.read_csv('cars.csv')
    cars

// Display first five rows
    
    cars.head()

// Display last five rows
    
    cars.tail()

### PROBLEM 2

// Import pandas

    import pandas as pd

// Load .csv file
    
    cars = pd.read_csv('cars.csv')
    cars

// Display the first five rows with odd-numbered columns using 'iloc'

    oc = cars.iloc[:, 1::2]

    result = oc.head()
    result

// Display the row that contains the ‘Model’ of ‘Mazda RX4’

    cars[0:1]

// Show how many cylinders does the car model ‘Camaro Z28’ have using 'loc'

    cars.loc[cars['Model']=='Camaro Z28', ['Model', 'cyl']]

// Show how many cylinders and what gear type the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have using 'loc'

    cars.loc[[1,28,18],['Model', 'cyl', 'gear']]
