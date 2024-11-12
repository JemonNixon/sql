### Python Fundamentals

1. **Data Types and Variables**

   ```python
   # Basic data types
   age = 23                      # int
   salary = 45000.50             # float
   name = "John Doe"             # str
   is_intern = True              # bool

   # Collections: list, tuple, dictionary, and set
   numbers = [1, 2, 3, 4]        # list
   coordinates = (10, 20)        # tuple
   employee = {"name": "John", "age": 23}  # dict
   unique_values = {1, 2, 3}     # set
   ```

2. **Control Structures**

   ```python
   # If-else statement
   score = 80
   if score >= 90:
       print("Excellent")
   elif score >= 75:
       print("Good")
   else:
       print("Needs improvement")

   # For loop
   for i in range(3):
       print("Iteration:", i)

   # While loop
   count = 0
   while count < 3:
       print("Count:", count)
       count += 1
   ```

3. **Functions**

   ```python
   def calculate_square(num):
       return num * num

   result = calculate_square(4)
   print("Square:", result)
   ```

4. **File Handling**

   ```python
   # Writing to a file
   with open('sample.txt', 'w') as file:
       file.write("Hello, this is a sample file.")

   # Reading from a file
   with open('sample.txt', 'r') as file:
       content = file.read()
       print(content)
   ```

---

### Numpy Basics

1. **Creating and Manipulating Arrays**

   ```python
   import numpy as np

   # Creating an array
   array = np.array([1, 2, 3, 4])
   print("Array:", array)

   # Basic operations
   print("Array + 2:", array + 2)
   print("Array * 3:", array * 3)
   ```

2. **Array Reshaping and Indexing**

   ```python
   # Reshape array
   reshaped_array = array.reshape(2, 2)
   print("Reshaped Array:\n", reshaped_array)

   # Slicing and indexing
   print("First element:", array[0])
   print("Last two elements:", array[-2:])
   ```

3. **Mathematical Operations**

   ```python
   # Aggregation functions
   print("Sum:", np.sum(array))
   print("Mean:", np.mean(array))
   print("Max:", np.max(array))
   print("Min:", np.min(array))
   ```

4. **Statistical Operations**

   ```python
   # Statistical functions
   print("Standard Deviation:", np.std(array))
   print("Variance:", np.var(array))
   ```

---

### Pandas Basics

1. **Creating DataFrames**

   ```python
   import pandas as pd

   data = {'Name': ['Alice', 'Bob', 'Charlie'],
           'Age': [24, 27, 22],
           'Salary': [50000, 60000, 55000]}
   df = pd.DataFrame(data)
   print("DataFrame:\n", df)
   ```

2. **Data Exploration**

   ```python
   print("First 2 rows:\n", df.head(2))
   print("Data Info:\n", df.info())
   print("Statistics:\n", df.describe())
   ```

3. **Selecting and Filtering Data**

   ```python
   # Selecting columns
   print("Names:\n", df['Name'])

   # Filtering rows
   print("Age > 23:\n", df[df['Age'] > 23])
   ```

4. **Handling Missing Values**

   ```python
   # Creating a DataFrame with NaN values
   df_with_nan = pd.DataFrame({'A': [1, None, 3], 'B': [4, 5, None]})
   print("With NaNs:\n", df_with_nan)

   # Drop rows with NaN values
   print("Drop NaNs:\n", df_with_nan.dropna())

   # Fill NaN values
   print("Fill NaNs:\n", df_with_nan.fillna(0))
   ```

5. **Group By and Aggregation**

   ```python
   # Group by 'Age' and find mean salary
   print("Grouped by Age:\n", df.groupby('Age')['Salary'].mean())
   ```

6. **Merging and Joining DataFrames**

   ```python
   # Merging two DataFrames
   df1 = pd.DataFrame({'Name': ['Alice', 'Bob'], 'Score': [85, 90]})
   merged_df = pd.merge(df, df1, on='Name', how='inner')
   print("Merged DataFrame:\n", merged_df)
   ```

---

### Data Visualization (Matplotlib Basics)

1. **Basic Plotting**

   ```python
   import matplotlib.pyplot as plt

   # Simple line plot
   x = [1, 2, 3, 4]
   y = [10, 20, 25, 30]
   plt.plot(x, y)
   plt.xlabel('X Axis')
   plt.ylabel('Y Axis')
   plt.title('Line Plot')
   plt.show()
   ```

2. **Bar Plot**

   ```python
   categories = ['A', 'B', 'C']
   values = [5, 7, 3]

   plt.bar(categories, values)
   plt.xlabel('Category')
   plt.ylabel('Values')
   plt.title('Bar Plot')
   plt.show()
   ```

3. **Histogram**

   ```python
   data = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
   plt.hist(data, bins=4)
   plt.xlabel('Value')
   plt.ylabel('Frequency')
   plt.title('Histogram')
   plt.show()
   ```

4. **Scatter Plot**

   ```python
   x = [1, 2, 3, 4]
   y = [10, 15, 13, 18]

   plt.scatter(x, y)
   plt.xlabel('X')
   plt.ylabel('Y')
   plt.title('Scatter Plot')
   plt.show()
   ```

 
