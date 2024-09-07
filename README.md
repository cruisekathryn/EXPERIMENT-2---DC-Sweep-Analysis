# **EXPERIMENT 2 - Numerical Python**
Name: **Cruz, Kathryn Angel S.**  
Section: **2ECE-A**  
***
The objective in this experiment is to identify and apply various codes and functions from the Numpy library in creating a Python program.  *A separate Jupyter Notebook file was also submitted to see the Python code for each problems.*

***  
## PROBLEM 1: NORMALIZATION PROBLEM
Normalization is one of the most basic preprocessing techniques in data analytics.
This involves centering and scaling process. Centering means subtracting the data from the mean and scaling means dividing with its standard deviation.
Mathematically, normalization can be expressed as  
<p align="center">
  <img src="https://github.com/user-attachments/assets/d8530f29-da97-44f0-b9b5-ce30cb0139d7" alt="Sublime's custom image"/>
</p>  

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and .std() calls.  

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as *X_normalized.npy*

### Solution:
```python
import numpy as np

# Create a randomized 5x5 ndarray
X = np.random.random((5,5))

# Normalize X using the mean and standard deviation
X_mean = X.mean()
X_std = X.std()
X_normalized = (X-X_mean)/X_std

# Saves the normalized ndarray as X_normalized.npy
np.save('X_normalized.npy', X_normalized)

# Prints the original and normalized arrays
print("Original Array:\n", X, "\n") ; print("Normalized Array: \n", X_normalized)
```
### Result:
<p align="center">
  <img src="https://github.com/user-attachments/assets/3b389fa2-a48b-46a2-b8bc-5a6a395bccf0" alt="Problem 2 Example"/>
</p>  

***  
## PROBLEM 2: DIVISIBLE BY 3 PROBLEM
Create the following 10 x 10 ndarray which are the squares of the first 100 positive integers.
<p align="center">
  <img src="https://github.com/user-attachments/assets/988ceb63-69d3-44d2-ac0e-3be1d67be9b6" alt="Problem 2 Example"/>
</p>  

From this ndrray, determine all the elements that are divisible by 3. Save the result as *div_by_3.npy*  
### Solution:
```python
import numpy as np

# Create an array of the first 100 positive integers
A = np.arange(1,101)

# Compute squares of the elements and reshape the array into a 10x10 ndarray
A_squared = (np.square(A)).reshape(10,10)

# Determine all elements in A_squared that are divisible by 3
div_by_3 = A_squared[A_squared%3==0]

# Saves the arrays with elements divisible by 3 as div_by_3.npy
np.save('div_by_3.npy', div_by_3)

# Prints the original 10x10 matrix and the 
print("Original 10X10 matrix with squared values:\n", A_squared); print("\nNumbers divisible by 3\n", div_by_3)
```  
### Result:
<p align="center">
  <img src="https://github.com/user-attachments/assets/697f5a1e-0e48-4fac-afe3-123929ede854" alt="Problem 2 Example"/>
</p>
