# EXPERIMENT 2 - NUMERICAL PYTHON

This repository contains Python scripts created to address various problems in ECE2112. A summary of each script is provided below.

### 1. Normalization Problem

###### A randomly generated 5x5 array is required to be normalized for this task. To normalize the random array, first produce it, then center it by subtracting the mean, then scale it by dividing it by the standard deviation. Save the normalized array to a file named `X_normalized.npy}.

**Function:**

```python

import numpy as np

# Create a 5x5 random values
X = np.random.random((5, 5))

# Calculate the mean and standard deviation
X_mean = np.mean(X)
X_std = np.std(X)

# Standardize the matrix
X_normalized = (X - X_mean) / X_std

# Save the standardized matrix
np.save('X_normalized.npy', X_normalized)

# Load and display the saved data
print("\nOriginal Array:\n", X)
print("\nNormalized Array:\n", X_normalized)

```
**Output:**



![Screen Shot 2024-09-08 at 7 49 20 PM](https://github.com/user-attachments/assets/18581160-ff82-43e7-ae2a-f7409f556d63)



### 2. Divisible by 3 Problem

###### The task is to create a 10x10 array containing the squares of the initial 100 positive integers. Finding every element in the array divisible by three is the aim, and the elements saved in a file named `div_by_3.npy` are the result.


**Function:**

```python

import numpy as np

# Generate random positive integer from 1 to 100
squares = np.arange(1, 101)**2

# Reshape into a 10x10 matrix
squares_10x10 = squares.reshape(10, 10)

# Extract elements divisible by 3
div_by_3 = squares_10x10[squares_10x10 % 3 == 0]

# Save the result to a file
np.save('div_by_3.npy', div_by_3)

# Load and display the saved data
data = np.load('div_by_3.npy')
data

```

**Output:**

![Screen Shot 2024-09-08 at 7 52 29 PM](https://github.com/user-attachments/assets/c7ce811a-ca3b-44a9-a006-2a0be70771e9)

