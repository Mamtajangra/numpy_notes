# Introduction to NumPy

NumPy is a Python library created in 2005 that performs numerical calculations. It is generally used for working with arrays.

NumPy also includes a wide range of mathematical functions, such as linear algebra, Fourier transforms, and random number generation, which can be applied to arrays.

---

## What is NumPy Used for?

NumPy is an important library generally used for:

- Machine Learning
- Data Science
- Image and Signal Processing
- Scientific Computing
- Quantum Computing
# NumPy Array Creation

The NumPy array is similar to a list, but with added benefits such as being faster and more memory efficient.
## Create Array Using Python List 

```
import numpy as np

# create a list named list1
list1 = [2, 4, 6, 8]

# create numpy array using list1
array1 = np.array(list1)

print(array1)

# Output: [2 4 6 8]
```
---

## Create an Array Using np.zeros()

The `np.zeros()` function allows us to create an array filled with all zeros. For example,

```
import numpy as np

# create an array with 4 elements filled with zeros
array1 = np.zeros(4)

print(array1)

# Output: [0. 0. 0. 0.]
```

---

## Create an Array With np.arange()

The `np.arange()` function returns an array with values within a specified interval. For example,

```
import numpy as np

# create an array with values from 0 to 4
array1 = np.arange(5)

print("Using np.arange(5):", array1)

# create an array with values from 1 to 8 with a step of 2
array2 = np.arange(1, 9, 2)

print("Using np.arange(1, 9, 2):",array2)
```


---

## Create an Array With np.random.rand()

The `np.random.rand()` function is used to create an array of random numbers.

Let's see an example to create an array of **5** random numbers,

```
import numpy as np

# generate an array of 5 random numbers
array1 = np.random.rand(5)

print(array1)
```
**Output**

[0.08455648 0.56379034 0.66463204 0.97608605 0.30700052]

---

## Create an Empty NumPy Array

To create an empty NumPy array, we use the `np.empty()` function. For example,

```
import numpy as np

# create an empty array of length 4
array1 = np.empty(4)

print(array1)
```
**Output**

[1.47966080e-316 0.00000000e+000 9.06092203e-312 2.47218893e-253]

# NumPy N-D Array Creation

NumPy is not restricted to 1-D arrays, it can have arrays of multiple dimensions, also known as N-dimensional arrays or ndarrays.

An N-dimensional array refers to the number of dimensions in which the array is organized.

An array can have any number of dimensions and each dimension can have any number of elements
## N-D Array Creation From List of Lists

##Create a 2-D NumPy Array

```
import numpy as np

# create a 2D array with 2 rows and 4 columns
array1 = np.array([[1, 2, 3, 4],
                  [5, 6, 7, 8]])

print(array1)
```


**Output**

[[1 2 3 4]
 [5 6 7 8]]


### Create a 3-D NumPy Array

Let's say we want to create a 3-D NumPy array consisting of two **"slices"** where each slice has **3** rows and **4** columns.

```
import numpy as np

# create a 3D array with 2 "slices", each of 3 rows and 4 columns
array1 = np.array([[[1, 2, 3, 4],
                [5, 6, 7, 8], 
                [9, 10, 11, 12]],
                     
                [[13, 14, 15, 16], 
                 [17, 18, 19, 20], 
                 [21, 22, 23, 24]]])

print(array1)
```
**Output**

[[[ 1  2  3  4]
  [ 5  6  7  8]
  [ 9 10 11 12]]

 [[13 14 15 16]
  [17 18 19 20]
  [21 22 23 24]]]
---

## Creating N-d Arrays From Scratch

We saw how to create N-d NumPy arrays from Python lists. Now we'll see how we can create them from scratch.

To create multidimensional arrays from scratch we use functions such as

- `np.zeros()`
- `np.arange()`
- `np.random.rand()`

---

## Create N-D Arrays using np.zeros()

The `np.zeros()` function allows us to create N-D arrays filled with all zeros. For example,

```
import numpy as np

# create 2D array with 2 rows and 3 columns filled with zeros
array1 = np.zeros((2, 3))

print("2-D Array: ")
print(array1)

# create 3D array with dimensions 2x3x4 filled with zeros
array2 = np.zeros((2, 3, 4))

print("\n3-D Array: ")
print(array2)
```

**Output**

2-D Array: 
[[0. 0. 0.]
 [0. 0. 0.]]

3-D Array: 
[[[0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]]

 [[0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]]]

---

## Create N-D Array with a Specified Value

In NumPy, we can use the `np.full()` function to create a multidimensional array with a specified value.

For example, to create a 2-D array with the value **5**, we can do the following:

```
import numpy as np

# Create a 2-D array with elements initialized to 5 
numpy_array = np.full((2, 2), 5)

print("Array:", numpy_array)
```

**Output**

[[5 5]
 [5 5]]

---

## Creating Arrays With np.random.rand()

The `np.random.rand()` function is used to create an array of random numbers.

```
import numpy as np

# create a 2D array of 2 rows and 2 columns of random numbers
array1 = np.random.rand(2, 2)

print("2-D Array: ")
print(array1)

# create a 3D array of shape (2, 2, 2) of random numbers
array2 = np.random.rand(2, 2, 2)

print("\n3-D Array: ")
print(array2)
```

**Output**

2-D Array: 
[[0.13198621 0.54730421]
 [0.36570987 0.16233836]]

3-D Array: 
[[[0.15666007 0.4580507 ]
  [0.84769856 0.76699589]]

 [[0.45395202 0.39944328]
  [0.62999479 0.39629496]]]

Here,

- `np.random.rand(2, 2)` - creates a 2D array of **2** rows and **2** columns of random numbers.
- `np.random.rand(2, 2, 2)` - creates a 3D array with 2 slices, each slice having **2** rows and **2** columns of random numbers.

---

## Create Empty N-D NumPy Array

To create an empty N-D NumPy array, we use the `np.empty()` function. For example,

```
import numpy as np

# create an empty 2D array with 2 rows and 2 columns
array1 = np.empty((2, 2))

print("2-D Array: ")
print(array1)

# create an empty 3D array of shape (2, 2, 2) 
array2 = np.empty((2, 2, 2))

print("\n3-D Array: ")
print(array2)
```

**Output**

2-D Array: 
[[8.86495615e-317 0.00000000e+000]
 [2.21149159e-316 1.76125651e-312]]

3-D Array: 
[[[1.0749539e-316 0.0000000e+000]
  [0.0000000e+000 0.0000000e+000]]

 [[0.0000000e+000 0.0000000e+000]
  [0.0000000e+000 0.0000000e+000]]]

# NumPy Data Types

A data type is a way to specify the type of data that will be stored in an array. For example,

```
array1 = np.array([2, 4, 6])
```

Here, the array1 array contains three integer elements, so the data type is Integer(`int64)`), by default.

NumPy provides us with several built-in data types to efficiently represent numerical data.

---

## NumPy Data Types

NumPy offers a wider range of numerical data types than what is available in Python. Here's the list of most commonly used numeric data types in NumPy:

1. `int8`, `int16`, `int32`, `int64` - signed integer types with different bit sizes
2. `uint8`, `uint16`, `uint32`, `uint64` - unsigned integer types with different bit sizes
3. `float32`, `float64` - floating-point types with different precision levels
4. `complex64`, `complex128` - complex number types with different precision levels

---

## Check Data Type of a NumPy Array

To check the data type of a NumPy array, we can use the `dtype` attribute. For example,

```
import numpy as np

# create an array of integers 
array1 = np.array([2, 4, 6])

# check the data type of array1
print(array1.dtype) 

# Output: int64
```


---

### Example: Check Data Type of NumPy Array

```
import numpy as np

# create an array of  integers
int_array = np.array([-3, -1, 0, 1])

# create an array of floating-point numbers
float_array = np.array([0.1, 0.2, 0.3])

# create an array of complex numbers
complex_array = np.array([1+2j, 2+3j, 3+4j])

# check the data type of int_array
print(int_array.dtype)  # prints int64

# check the data type of float_array
print(float_array.dtype)  # prints float64

# check the data type of complex_array
print(complex_array.dtype)  # prints complex128
```

**Output**

int64
float64
complex128

Here, we have created types of arrays and checked the default data types of these arrays using the `dtype` attribute.

- `int_array` - contains four integer elements whose default data type is `int64`
- `float_array` - contains three floating-point numbers whose default data type is `float64`
- `complex_array` - contains three complex numbers whose default data type is `complex128`

---

## Creating NumPy Arrays With a Defined Data Type

In NumPy, we can create an array with a defined data type by passing the `dtype` parameter while calling the `np.array()` function. For example,

```
import numpy as np

# create an array of 32-bit integers
array1 = np.array([1, 3, 7], dtype='int32')

print(array1, array1.dtype)
```

**Output**

[1 3 7] int32

In the above example, we have created a NumPy array named array1 with a defined data type.

Notice the code,

```
np.array([1, 3, 7], dtype='int32')
```

Here, inside `np.array()`, we have passed an array `[1, 3, 7]` and set the `dtype` parameter to `int32`.

Since we have set the data type of the array to `int32`, each element of the array is represented as a 32-bit integer.

---

```
import numpy as np

# create an array of integers
int_array = np.array([1, 3, 5, 7])

# convert data type of int_array to float
float_array = int_array.astype('float')

# print the arrays and their data types
print(int_array, int_array.dtype)
print(float_array, float_array.dtype)
```

**Output**

[1 3 5 7] int64
[1. 3. 5. 7.] float64

Here, `int_array.astype('float')` converts the data type of `int_array` from `int64` to `float64` using `astype()`.

# NumPy Array Attributes

In NumPy, attributes are properties of NumPy arrays that provide information about the array's shape, size, data type, dimension, and so on.

For example, to get the dimension of an array, we can use the `ndim` attribute.

There are numerous attributes available in NumPy, which we'll learn below.

---

## Common NumPy Attributes

Here are some of the commonly used NumPy attributes:

|Attributes|Description|
|---|---|
|`ndim`|returns number of dimension of the array|
|`size`|returns number of elements in the array|
|`dtype`|returns data type of elements in the array|
|`shape`|returns the size of the array in each dimension.|
|`itemsize`|returns the size (in bytes) of each elements in the array|
|`data`|returns the buffer containing actual elements of the array in memory|

To access the Numpy attributes, we use the `.` notation. For example,

```
array1.ndim
```

This returns the number of dimensions in array1.

---

## Numpy Array ndim Attribute

The `ndim` attribute returns the number of dimensions in the numpy array. For example,

```
import numpy as np

# create a 2-D array 
array1 = np.array([[2, 4, 6],
                  [1, 3, 5]])

# check the dimension of array1
print(array1.ndim) 

# Output: 2
```---

```

## NumPy Array size Attribute
import numpy as np
The `size` attribute returns the total number of elements in the given array.

Let's see an example.

import numpy as np
array1 = np.array([[1, 2, 3],
                 [6, 7, 8]])

# 
return total number of elements in array1
print(array1.size)


## NumPy Array shape Attribute

In NumPy, the `shape` attribute returns a tuple of integers that gives the size of the array in each dimension. For example,

```
import numpy as np

array1 = np.array([[1, 2, 3],
                [6, 7, 8]])

# return a tuple that gives size of array in each dimension
print(array1.shape)

# Output: (2,3)
```
Here, array1 is a 2-D array that has **2** rows and **3** columns. So `array1.shape` returns the tuple `(2,3)` as an output.

---

## NumPy Array dtype Attribute

We can use the `dtype` attribute to check the datatype of a NumPy array. For example,

```
import numpy as np

# create an array of integers 
array1 = np.array([6, 7, 8])

# check the data type of array1
print(array1.dtype) 

# Output: int64
```
In the above example, the `dtype` attribute returns the data type of array1.

Since array1 is an array of integers, the data type of array1 is inferred as `int64` by default.


---

## NumPy Array itemsize Attribute

In NumPy, the `itemsize` attribute determines size (in bytes) of each element in the array. For example,

```
import numpy as np

# create a default 1-D array of integers
array1 = np.array([6, 7, 8, 10, 13])

# create a 1-D array of 32-bit integers 
array2 = np.array([6, 7, 8, 10, 13], dtype=np.int32)

# use of itemsize to determine size of each array element of array1 and array2
print(array1.itemsize)  # prints 8
print(array2.itemsize)  # prints 4
```
**Output**

8
4

Here,

- array1 is an array containing **64-bit** integers by default, which uses **8** bytes of memory per element. So, `itemsize` returns **8** as the size of each element.
- array2 is an array of **32-bit** integers, so each element in this array uses only **4** bytes of memory. So, `itemsize` returns **4** as the size of each element.

---

## NumPy Array data Attribute

In NumPy, we can get a buffer containing actual elements of the array in memory using the `data` attribute.

In simpler terms, the `data` attribute is like a pointer to the memory location where the array's data is stored in the computer's memory.

Let's see an example.

```
import numpy as np

array1 = np.array([6, 7, 8])
array2 = np.array([[1, 2, 3],
                [6, 7, 8]])

# print memory address of array1's and array2's data
print("\nData of array1 is: ",array1.data)
print("Data of array2 is: ",array2.data)
```
**Output**

Data of array1 is: <memory at 0x7f746fea4a00>
Data of array2 is:  <memory at 0x7f746ff6a5a0>

# NumPy Input Output

NumPy offers input/output (I/O) functions for loading and saving data to and from files.

Input/output functions support a variety of file formats, including binary and text formats.

- The binary format is designed for efficient storage and retrieval of large arrays.
- The text format is more human-readable and can be easily edited in a text editor.

---

## Most Commonly Used I/O Functions

Here are some of the commonly used NumPy Input/Output functions:

|Function|Description|
|---|---|
|`save()`|saves an array to a binary file in the NumPy `.npy` format.|
|`load()`|loads data from a binary file in the NumPy `.npy` format|
|`savetxt()`|saves an array to a text file in a specific format|
|`loadtxt()`|loads data from a text file.|

---

## NumPy save() Function

In NumPy, the `save()` function is used to save an array to a binary file in the NumPy `.npy` format.

Here's the syntax of the `save()` function,

```
np.save(file, array)
```

- `file` - specifies the file name (along with path if required)
- `array` - specifies the NumPy array to be saved

Now, let's see an example.

```
import numpy as np

# create a NumPy array
array1 = np.array([[1, 3, 5], 
                   [7, 9, 11]])

# save the array to a file
np.save('file1.npy', array1)
```


Here, we saved the NumPy array named array1 to the binary file named `file1.npy` in our current directory.

---

## NumPy load() Function

In the previous example, we saved an array to a binary file. Now we'll load that saved file using the `load()` function.

Let's see an example.

```
import numpy as np

# load the saved NumPy array
loaded_array = np.load('file1.npy')

# display the loaded array
print(loaded_array)
```
**Output**

[[ 1  3  5]
 [ 7  9 11]]

Here, we have used the `load()` function to read a binary file named `file1.npy`. This is the same file we created and saved using `save()` function in the last example.

---

## NumPy savetxt() Function

In NumPy, we use the `savetxt()` function to save an array to a text file.

Here's the syntax of the `savetxt()` function:

```
np.save(file, array)
```

- `file` - specifies the file name
- `array` - specifies the NumPy array to be saved

Now, let's see an example,

```
import numpy as np

# create a NumPy array
array2 = np.array([[1, 3, 5], 
                   [7, 9, 11]])

# save the array to a file
np.savetxt('file2.txt', array2)
```
The code above will save the NumPy array array2 to the text file named `file2.txt` in our current directory.

---

## NumPy loadtxt() Function

We use the `loadtxt()` function to load the saved `txt` file.

Let's see an example to load the `file2.txt` file that we saved earlier.

```
import numpy as np

# load the saved NumPy array
loaded_array = np.loadtxt('file2.txt')

# display the loaded array
print(loaded_array)
```



**Output**

[[1. 3. 5.]
 [7. 9. 11.]]

Here, we have used the `loadtxt()` function to load the text file named `file2.txt` that was previously created and saved using the `savetxt()` function.

**Note**: The values in the loaded array have dots `.` because `loadtxt()` reads the values as floating point numbers by default.
# Numpy Array Indexing

In NumPy, each element in an array is associated with a number. The number is known as an **array index**.

Let's see an example to demonstrate NumPy array indexing.


Array Indexing in NumPy

In the above array, 5 is the 3rd element. However, its index is 2.

This is because the array indexing starts from 0, that is, the first element of the array has index 0, the second element has index 1, and so on.


---

## Access Array Elements Using Index

We can use indices to access individual elements of a NumPy array.

Suppose we have a NumPy array:

```
array1 = np.array([1, 3, 5, 7, 9])
```

Now, we can use the index number to access array elements as:

- `array1[0]` - to access the first element, i.e. **1**
- `array1[2]` - to access the third element, i.e. **5**
- `array1[4]` - to access the fifth element, i.e. **9**

---

### Example: Access Array Elements Using Index

```
import numpy as np

array1 = np.array([1, 3, 5, 7, 9])

# access numpy elements using index
print(array1[0])    # prints 1
print(array1[2])    # prints 5
print(array1[4])    # prints 9
```


**Note**: Since the last element of `array1` is at index **4**, if we try to access the element beyond that, say index **5**, we will get an index error: `IndexError: index 5 is out of bounds for axis 0 with size 5`

---

## Modify Array Elements Using Index

We can use indices to change the value of an element in a NumPy array. For example,

```
import numpy as np

# create a numpy array
numbers = np.array([2, 4, 6, 8, 10])

# change the value of the first element
numbers[0] = 12
print("After modifying first element:",numbers)    # prints [12 4 6 8 10]

# change the value of the third element
numbers[2] = 14
print("After modifying third element:",numbers)    # prints [12 4 14 8 10]
```


**Output**

After modifying first element: [12  4  6  8 10]
After modifying third element: [12  4 14  8 10]


---

## NumPy Negative Array Indexing

NumPy allows negative indexing for its array. The index of **-1** refers to the last item, **-2** to the second last item and so on.


NumPy Array Negative Indexing

Let's see an example.

```
import numpy as np

# create a numpy array
numbers = np.array([1, 3, 5, 7, 9])

# access the last element
print(numbers[-1])    # prints 9

# access the second-to-last element
print(numbers[-2])    # prints 7
```

**Output**
9
7

---

## Modify Array Elements Using Negative Indexing

Similar to regular indexing, we can also modify array elements using negative indexing. For example,

```
import numpy as np

# create a numpy array
numbers = np.array([2, 3, 5, 7, 11])

# modify the last element
numbers[-1] = 13
print(numbers)    # Output: [2 3 5 7 13]

# modify the second-to-last element
numbers[-2] = 17
print(numbers)    # Output: [2 3 5 17 13]
```


---

## 2-D NumPy Array Indexing

Array indexing in NumPy allows us to access and manipulate elements in a 2-D array.

To access an element of array1, we need to specify the row index and column index of the element. Suppose we have following 2-D array,

```
array1 = np.array([[1, 3, 5], 
                     [7, 9, 2], 
                     [4, 6, 8]])
```

Now, say we want to access the element in the third row and second column we specify the index as:

```
array1[2, 1] # returns 6
```

Since we know indexing starts from **0**. So to access the element in the third row and second column, we need to use index **2** for the third row and index **1** for the second column respectively.

---

### Example: 2-D NumPy Array Indexing

```
import numpy as np

# create a 2D array 
array1 = np.array([[1, 3, 5, 7], 
                       [9, 11, 13, 15],
                       [2, 4, 6, 8]])


# access the element at the second row and fourth column
element1 = array1[1, 3]  # returns 15
print("4th Element at 2nd Row:",element1)  

# access the element at the first row and second column
element2 = array1[0, 1]  # returns 3
print("2nd Element at First Row:",element2)  
```


**Output**

4th Element at 2nd Row: 15
2nd Element at First Row: 3

---

## Access Row or Column of 2D Array Using Indexing

In NumPy, we can access specific rows or columns of a 2-D array using array indexing.

Let's see an example.

```
import numpy as np

# create a 2D array 
array1 = np.array([[1, 3, 5], 
             [7, 9, 2], 
             [4, 6, 8]])

# access the second row of the array
second_row = array1[1, :]
print("Second Row:", second_row)  # Output: [7 9 2]

# access the third column of the array
third_col = array1[:, 2]
print("Third Column:", third_col)  # Output: [5 2 8]
```
**Output**

Second Row: [7 9 2]
Third Column: [5 2 8]

---

## 3-D NumPy Array Indexing

We learned how to access elements in a 2D array. We can also access elements in higher dimensional arrays.

To access an element of a 3D array, we use **three indices** separated by commas.

- The **first index** refers to the slice
- The **second index** refers to the row
- The **third index** refers to the column.

**Note**: In 3D arrays, slice is a 2D array that is obtained by taking a subset of the elements in one of the dimensions.

Let's see an example.

```
import numpy as np

# create a 3D array with shape (2, 3, 4)
array1 = np.array([[[1, 2, 3, 4], 
                   [5, 6, 7, 8], 
                   [9, 10, 11, 12]],
                     
                    [[13, 14, 15, 16], 
                    [17, 18, 19, 20], 
                    [21, 22, 23, 24]]])

# access a specific element of the array
element = array1[1, 2, 1]

# print the value of the element
print(element) 
 
# Output: 22
```

## NumPy Array Slicing

Array Slicing is the process of extracting a portion of an array.

With slicing, we can easily access elements in the array. It can be done on one or more dimensions of a NumPy array.

---

## Syntax of NumPy Array Slicing

Here's the syntax of array slicing in NumPy:

```
array[start:stop:step]
```

Here,

- `start` - index of the first element to be included in the slice
- `stop` - index of the last element (exclusive)
- `step` - step size between each element in the slice

**Note:** When we slice arrays, the start index is inclusive but the stop index is exclusive.

- If we omit `start`, slicing starts from the first element
- If we omit `stop`, slicing continues up to the last element
- If we omit `step`, default step size is 1

---

## 1D NumPy Array Slicing

In NumPy, it's possible to access the portion of an array using the slicing operator `:`. For example,

```
import numpy as np

# create a 1D array 
array1 = np.array([1, 3, 5, 7, 8, 9, 2, 4, 6])

# slice array1 from index 2 to index 6 (exclusive)
print(array1[2:6])  # [5 7 8 9]

# slice array1 from index 0 to index 8 (exclusive) with a step size of 2
print(array1[0:8:2])  # [1 5 8 2]

# slice array1 from index 3 up to the last element
print(array1[3:])  # [7 8 9 2 4 6]

# items from start to end
print(array1[:])   # [1 3 5 7 8 9 2 4 6]
```

- `array1[2:6]` - slices array1 from index **2** to index **6**, not including index **6**
- `array1[0:8:2]` - slices array1 from index **0** to index **8**, not including index **8**
- `array1[3:]` - slices array1 from index **3** up to the last element
- `array1[:]` - returns all items from beginning to end

---

## Modify Array Elements Using Slicing

With slicing, we can also modify array elements using:

- `start` parameter
- `stop` parameter
- `start` and `stop` parameter
- `start`, `stop`, and `step` parameter

### 1. Using start Parameter

```
import numpy as np

# create a numpy array
numbers = np.array([2, 4, 6, 8, 10, 12])

# modify elements from index 3 onwards
numbers[3:] = 20
print(numbers)

# Output: [ 2  4  6 20 20 20]
```

Here, `numbers[3:] = 20` replaces all the elements from index **3** onwards with new value **20**.

### 2. Using stop Parameter

```
import numpy as np

# create a numpy array
numbers = np.array([2, 4, 6, 8, 10, 12])

# modify the first 3 elements
numbers[:3] = 40
print(numbers)

# Output: [40 40 40  8 10 12]
```

Here, `numbers[:3] = 20` replaces the first 3 elements with the new value **40**.

### 3. Using start and stop parameter

```
import numpy as np

# create a numpy array
numbers = np.array([2, 4, 6, 8, 10, 12])

# modify elements from indices 2 to 5
numbers[2:5] = 22
print(numbers)

# Output: [2 4 22 22 22 12]
```

Here, `numbers[2:5] = 22` selects elements from index **2** to index **4** and replaces them with new value **22**.

### 4. Using start, stop, and step parameter

```
import numpy as np

# create a numpy array
numbers = np.array([2, 4, 6, 8, 10, 12])

# modify every second element from indices 1 to 5
numbers[1:5:2] = 16
print(numbers)

# Output: [ 2 16 6 16 10 12]
```
---

## NumPy Array Negative Slicing

We can also use _negative indices_ to perform negative slicing in NumPy arrays. During negative slicing, elements are accessed from the end of the array.

Let's see an example.

```
import numpy as np

# create a numpy array
numbers = np.array([2, 4, 6, 8, 10, 12])

# slice the last 3 elements of the array
# using the start parameter
print(numbers[-3:])    # [8 10 12]

# slice elements from 2nd-to-last to 4th-to-last element
# using the start and stop parameters
print(numbers[-5:-2])    # [4 6 8] 

# slice every other element of the array from the end
# using the start, stop, and step parameters
print(numbers[-1::-2])   # [12 8 4]
```
**Output**

Using numbers[-3:]- [ 8 10 12]
Using numbers[-5:-2]- [4 6 8]
Using numbers[-1::-2]- [12  8  4]

Here,

- `numbers[-3:]` - slices last 3 elements of numbers
- `numbers[-5:-2]` - slices numbers elements from 5th last to 2nd last(excluded)
- `numbers[-1::-2]` - slices every other numbers elements from the end with step size **2**

---

## Reverse NumPy Array Using Negative Slicing

In NumPy, we can also reverse array elements using the negative slicing. For example,

```
import numpy as np

# create a numpy array
numbers = np.array([2, 4, 6, 8, 10, 12])

# generate reversed array
reversed_numbers = numbers[::-1]
print(reversed_numbers)

# Output: [12 10 8 6 4 2]
```

Here, the slice `numbers[::-1]` selects all the elements of the array with a step size of **-1**, which reverses the order of the elements.

---

## 2D NumPy Array Slicing

A 2D NumPy array can be thought of as a matrix, where each element has two indices, row index and column index.

To slice a 2D NumPy array, we can use the same syntax as for slicing a 1D NumPy array. The only difference is that we need to specify a slice for each dimension of the array.

### Syntax of 2D NumPy Array Slicing

```
array[row_start:row_stop:row_step, col_start:col_stop:col_step]
```

Here,

- `row_start`,`row_stop`,`row_step` - specifies starting index, stopping index, and step size for the rows respectively
- `col_start`,`col_stop`,`col_step` - specifies starting index, stopping index, and step size for the columns respectively

Let's understand this with an example.

```
# create a 2D array
array1 = np.array([[1, 3, 5, 7], 
                   [9, 11, 13, 15]])

print(array1[:2, :2])

# Output

[[ 1  3]
 [ 9 11]]
```

Here, the `,` in `[:2, :2]` separates the rows of the array.

The first `:2` returns first 2 rows i.e., entire array1. This results in

```
[1  3]
```

The second `:2` returns first 2 columns from the 2 rows. This results in

```
[9 11]
```

---

### Example: 2D NumPy Array Slicing

```
import numpy as np

# create a 2D array 
array1 = np.array([[1, 3, 5, 7], 
                      [9, 11, 13, 15],
                      [2, 4, 6, 8]])


# slice the array to get the first two rows and columns
subarray1 = array1[:2, :2]

# slice the array to get the last two rows and columns
subarray2 = array1[1:3, 2:4]

# print the subarrays
print("First Two Rows and Columns: \n",subarray1)
print("Last two Rows and Columns: \n",subarray2)
```
**Output**

First Two Rows and Columns: 
[[ 1  3]
 [ 9 11]]
Last two Rows and Columns: 
 [[13 15]
 [ 6  8]]

Here,

- `array1[:2, :2]` - slices array1 that starts at the first row and first column (default values), and ends at the second row and second column (exclusive)
- `array1[1:3, 2:4]` - slices array1 that starts at the second row and third column (index **1** and **2**), and ends at the third row and fourth column (index **2** and **3**)


# NumPy Array Reshaping

NumPy array reshaping simply means changing the shape of an array without changing its data.

Let's say we have a 1D array.

```
np.array([1, 3, 5, 7, 2, 4, 6, 8])
```

We can reshape this 1D array into N-d array as

```
# reshape 1D into 2D array 
# with 2 rows and 4 columns
[[1 3 5 7]
 [2 4 6 8]]

# reshape 1D into 3D array 
# with 2 rows, 2 columns, and 2 layers
[[[1 3]
  [5 7]]

 [[2 4]
  [6 8]]]
```

Here, we can see that the 1D array has been reshaped into 2D and 3D arrays without altering its data.

---

## Syntax NumPy Array Reshaping

The syntax of NumPy array reshaping is

```
np.reshape(array, newshape, order = 'C')
```

Here,

- `array` - input array that needs to be reshaped,
- `newshape` - desired new shape of the array
- `order` (optional) - specifies the order in which the elements of the array should be arranged. By default it is set to `'C'`

**Note:** The `order` argument can take one of three values: `'C'`, `'F'`, or `'A'`. We will discuss them later in this tutorial.

---

## Reshape 1D Array to 2D Array in NumPy

We use the `reshape()` function to reshape a 1D array into a 2D array. For example,

```
import numpy as np

array1 = np.array([1, 3, 5, 7, 2, 4, 6, 8])

# reshape a 1D array into a 2D array 
# with 2 rows and 4 columns
result = np.reshape(array1, (2, 4))
print(result)
```


**Output**

[[1 3 5 7]
 [2 4 6 8]]

In the above example, we have used the `reshape()` function to change the shape of the 1D array named array1 into the 2D array. Notice the use of the `reshape()` function,

```
np.reshape(array1, (2, 4))
```

Here, `reshape()` takes two parameters,

- `array1` - array to be reshaped
- `(2, 4)` - new shape of array1 specified as a tuple with **2** rows and **4** columns.

---

### Example: Reshape 1D Array to 2D Array in NumPy

```
import numpy as np

# reshape a 1D array into a 2D array 
# with 4 rows and 2 columns
array1 = np.array([1, 3, 5, 7, 2, 4, 6, 8])
result1 = np.reshape(array1, (4, 2))
print("With 4 rows and 2 columns: \n",result1)


# reshape a 1D array into a 2D array with a single row
result2 = np.reshape(array1, (1, 8))
print("\nWith a single row: \n",result2)
```



**Output**

With 4 rows and 2 columns: 
[[1 3]
 [5 7]
 [2 4]
 [6 8]]

With a single row: 
 [[1 3 5 7 2 4 6 8]]

**Note**:

- We need to make sure that the new shape in `reshape()` has the same number of elements as the original array, else a `ValueError` will be raised.
- For example, reshaping an **8** element 1D array into a 2D array of **2** rows and **4** columns is possible, but reshaping it into a 2D array of **3** rows and **3** columns is not possible as that would require **3x3 = 9 elements**.

---

## Reshape 1D Array to 3D Array in NumPy

In NumPy, we can reshape a 1D NumPy array into a 3D array with a specified number of rows, columns, and layers. For example,

```
import numpy as np

# create a 1D array
array1 = np.array([1, 3, 5, 7, 2, 4, 6, 8])

# reshape the 1D array to a 3D array
result = np.reshape(array1, (2, 2, 2))

# print the new array
print("1D to 3D Array: \n",result)
```



**Output**

1D to 3D Array: 
[[[1 3]
  [5 7]]

 [[2 4]
  [6 8]]]

Here, since there are **8** elements in the array1 array, `np.reshape(array1, (2, 2, 2))` reshapes array1 into a 3D array with **2** rows, **2** columns and **2** layers.

---

## Flatten N-d Array to 1-D Array Using reshape()

Flattening an array simply means converting a multidimensional array into a 1D array.

To flatten an N-d array to a 1-D array we can use `reshape()` and pass **"-1"** as an argument.

Let's see an example.

```
import numpy as np

# flatten 2D array to 1D
array1 = np.array([[1, 3], [5, 7], [9, 11]])
result1 = np.reshape(array1, -1)
print("Flattened 2D array:", result1)

# flatten 3D array to 1D
array2 = np.array([[[1, 3], [5, 7]], [[2, 4], [6, 8]]])
result2 = np.reshape(array2, -1)
print("Flattened 3D array:", result2)
```
**Output**

Flattened 2D array: [ 1  3  5  7  9 11]
Flattened 3D array: [1 3 5 7 2 4 6 8]

Here, `reshape(array1, -1)` and `reshape(array2, -1)` convert 2-D array and 3-D array into a 1-D array by collapsing all dimensions.

# NumPy Arithmetic Array Operations

NumPy provides a wide range of operations that can perform on arrays, including arithmetic operations.

NumPy's arithmetic operations are widely used due to their ability to perform simple and efficient calculations on arrays.

In this tutorial, we will explore some commonly used arithmetic operations in NumPy and learn how to use them to manipulate arrays.

---

## List of Arithmetic Operations

Here's a list of various arithmetic operations along with their associated operators and built-in functions:

|Element-wise Operation|Operator|Function|
|---|---|---|
|Addition|`+`|`add()`|
|Subtraction|`-`|`subtract()`|
|Multiplication|`*`|`multiply()`|
|Division|`/`|`divide()`|
|Exponentiation|`**`|`power()`|
|Modulus|`%`|`mod()`|


---

## NumPy Array Element-Wise Addition

As mentioned earlier, we can use the both `+` operator and the built-in function `add()` to perform element-wise addition between two NumPy arrays. For example,

```
import numpy as np

first_array = np.array([1, 3, 5, 7])
second_array = np.array([2, 4, 6, 8])

# using the + operator
result1 = first_array + second_array
print("Using the + operator:",result1) 

# using the add() function
result2 = np.add(first_array, second_array)
print("Using the add() function:",result2) 
```
**Output**

Using the + operator: [ 3  7 11 15]
Using the add() function: [ 3  7 11 15]


---

## NumPy Array Element-Wise Subtraction

In NumPy, we can either use the `-` operator or the `subtract()` function to perform element-wise subtraction between two NumPy arrays. For example,

```
import numpy as np

first_array = np.array([3, 9, 27, 81])
second_array = np.array([2, 4, 8, 16])

# using the - operator
result1 = first_array - second_array
print("Using the - operator:",result1) 

# using the subtract() function
result2 = np.subtract(first_array, second_array)
print("Using the subtract() function:",result2) 
```

**Output**

Using the - operator: [ 1  5 19 65]
Using the subtract() function: [ 1  5 19 65]


---

## NumPy Array Element-Wise Multiplication

For element-wise multiplication, we can use the `*` operator or the `multiply()` function. For example,

```
import numpy as np

first_array = np.array([1, 3, 5, 7])
second_array = np.array([2, 4, 6, 8])

# using the * operator
result1 = first_array * second_array
print("Using the * operator:",result1) 

# using the multiply() function
result2 = np.multiply(first_array, second_array)
print("Using the multiply() function:",result2) 
```
**Output**

Using the * operator: [ 2 12 30 56]
Using the multiply() function: [ 2 12 30 56]


---

## NumPy Array Element-Wise Division

We can use either the `/` operator or the `divide()` function to perform element-wise division between two numpy arrays. For example,

```
import numpy as np

first_array = np.array([1, 2, 3])
second_array = np.array([4, 5, 6])

# using the / operator
result1 = first_array / second_array
print("Using the / operator:",result1) 

# using the divide() function
result2 = np.divide(first_array, second_array)
print("Using the divide() function:",result2) 
```
**Output**

Using the / operator: [0.25 0.4  0.5 ]
Using the divide() function: [0.25 0.4  0.5 ]

---

## NumPy Array Element-Wise Exponentiation

Array exponentiation refers to raising each element of an array to a given power.

In NumPy, we can use either the `**` operator or the `power()` function to perform the element-wise exponentiation operation. For example,

```
import numpy as np

array1 = np.array([1, 2, 3])

# using the ** operator
result1 = array1 ** 2
print("Using the ** operator:",result1) 

# using the power() function
result2 = np.power(array1, 2)
print("Using the power() function:",result2) 
```

**Output**

Using the ** operator: [1 4 9]
Using the power() function: [1 4 9]

---

## NumPy Array Element-Wise Modulus

We can perform a modulus operation in NumPy arrays using the `%` operator or the `mod()` function.

This operation calculates the remainder of element-wise division between two arrays.

Let's see an example.

```
import numpy as np

first_array = np.array([9, 10, 20])
second_array = np.array([2, 5, 7])

# using the % operator
result1 = first_array % second_array
print("Using the % operator:",result1) 

# using the mod() function
result2 = np.mod(first_array, second_array)
print("Using the mod() function:",result2)
```
**Output**

Using the % operator: [1 0 6]
Using the mod() function: [1 0 6]


# NumPy Array Functions

NumPy array functions are the built-in functions provided by NumPy that allow us to create and manipulate arrays, and perform different operations on them.

We will discuss some of the most commonly used NumPy array functions.

---

## Common NumPy Array Functions

There are many NumPy array functions available but here are some of the most commonly used ones.

|Array Operations|Functions|
|---|---|
|Array Creation Functions|`np.array()`, `np.zeros()`, `np.ones()`, `np.empty()`, etc.|
|Array Manipulation Functions|`np.reshape()`, `np.transpose()`, etc.|
|Array Mathematical Functions|`np.add()`, `np.subtract()`, `np.sqrt()`, `np.power()`, etc.|
|Array Statistical Functions|`np.median()`, `np.mean()`, `np.std()`, and `np.var()`.|
|Array Input and Output Functions|`np.save()`, `np.load()`, `np.loadtxt()`, etc.|

---

## NumPy Array Creation Functions

Array creation functions allow us to create new NumPy arrays. For example,

```
import numpy as np

# create an array using np.array()
array1 = np.array([1, 3, 5])
print("np.array():\n", array1)

# create an array filled with zeros using np.zeros()
array2 = np.zeros((3, 3))
print("\nnp.zeros():\n", array2)

# create an array filled with ones using np.ones()
array3 = np.ones((2, 4))
print("\nnp.ones():\n", array3)
```
**Output**

np.array():
[1 3 5]

np.zeros():
[[0. 0. 0.]
 [0. 0. 0.]
 [0. 0. 0.]]

np.ones():
[[1. 1. 1. 1.]
 [1. 1. 1. 1.]]


---

## NumPy Array Manipulation Functions

NumPy array manipulation functions allow us to modify or rearrange NumPy arrays. For example,

```
import numpy as np

# create a 1D array
array1 = np.array([1, 3, 5, 7, 9, 11])

# reshape the 1D array into a 2D array
array2 = np.reshape(array1, (2, 3))

# transpose the 2D array
array3 = np.transpose(array2)

print("Original array:\n", array1)
print("\nReshaped array:\n", array2)
print("\nTransposed array:\n", array3)
```

**Output**

Original array:
[ 1  3  5  7  9 11]

Reshaped array:
 [[ 1  3  5]
 [ 7  9 11]]

Transposed array:
 [[ 1  7]
 [ 3  9]
 [ 5 11]]

In this example,

- `np.reshape(array1, (2, 3))` - reshapes array1 into 2D array with shape `(2,3)`
- `np.transpose(array2)` - transposes 2D array array2

---

## NumPy Array Mathematical Functions

In NumPy, there are tons of mathematical functions to perform on arrays. For example,

```
import numpy as np

# create two arrays
array1 = np.array([1, 2, 3, 4, 5])
array2 = np.array([4, 9, 16, 25, 36])

# add the two arrays element-wise
arr_sum = np.add(array1, array2)

# subtract the array2 from array1 element-wise
arr_diff = np.subtract(array1, array2)

# compute square root of array2 element-wise
arr_sqrt = np.sqrt(array2)


print("\nSum of arrays:\n", arr_sum)
print("\nDifference of arrays:\n", arr_diff)
print("\nSquare root of first array:\n", arr_sqrt)
```
**Output**

Sum of arrays:
[ 5 11 19 29 41]

Difference of arrays:
 [ -3  -7 -13 -21 -31]

Square root of first array:
 [2. 3. 4. 5. 6.]

---

## NumPy Array Statistical Functions

NumPy provides us with various statistical functions to perform statistical data analysis.

These statistical functions are useful to find basic statistical concepts like mean, median, variance, etc. It is also used to find the maximum or the minimum element in an array.

Let's see an example.

```
import numpy as np

# create a numpy array
marks = np.array([76, 78, 81, 66, 85])

# compute the mean of marks
mean_marks = np.mean(marks)
print("Mean:",mean_marks)

# compute the median of marks
median_marks = np.median(marks)
print("Median:",median_marks)

# find the minimum and maximum marks
min_marks = np.min(marks)
print("Minimum marks:", min_marks)

max_marks = np.max(marks)
print("Maximum marks:", max_marks)
```
**Output**

Mean: 77.2
Median: 78.0
Minimum marks: 66
Maximum marks: 85

---

## NumPy Array Input/Output Functions

NumPy offers several input/output (I/O) functions for loading and saving data to and from files. For example,

```
import numpy as np

# create an array
array1 = np.array([[1, 3, 5], [2, 4, 6]])

# save the array to a text file
np.savetxt('data.txt', array1)

# load the data from the text file
loaded_data = np.loadtxt('array1.txt')

# print the loaded data
print(loaded_data)
```



**Output**

[[1. 3. 5.]
 [2. 4. 6.]]

In this example, we first created the 2D array named array1 and then saved it to a text file using the `np.savetxt()` function.

We then loaded the saved data using the `np.loadtxt()` function.

# Numpy Comparison/Logical Operations

NumPy provides several comparison and logical operations that can be performed on NumPy arrays.

NumPy's comparison operators allow for element-wise comparison of two arrays.

Similarly, logical operators perform boolean algebra, which is a branch of algebra that deals with `True` and `False` statements.

First we'll discuss comparison operations and then about logical operations in NumPy.

---

## NumPy Comparison Operators

NumPy provides various element-wise comparison operators that can compare the elements of two NumPy arrays.

Here's a list of various comparison operators available in NumPy.

|Operators|Descriptions|
|---|---|
|`<` (less than)|returns `True` if element of the first array is less than the second one|
|`<=` (less than or equal to)|returns `True` if element of the first array is less than or equal to the second one|
|`>` (greater than)|returns `True` if element of the first array is greater than the second one|
|`>=` (greater than or equal to)|returns `True` if element of the first array is greater than or equal to the second one|
|`==` (equal to)|returns `True` if the element of the first array is equal to the second one|
|`!=` (not equal to)|returns `True` if the element of the first array is not equal to the second one|

Next, we'll see examples of these operators.

---

## Example 1: NumPy Comparison Operators

```
import numpy as np

array1 = np.array([1, 2, 3])
array2 = np.array([3, 2, 1])

# less than operator
result1 = array1 < array2
print("array1 < array2:",result1)    # Output: [ True False False]

# greater than operator
result2 = array1 > array2
print("array1 > array2:",result2)    # Output: [False False  True]

# equal to operator
result3 = array1 == array2
print("array1 == array2:",result3)    # Output: [False  True False]
```
**Output**

array1 < array2: [ True False False]
array1 > array2: [False False  True]
array1 == array2: [False  True False]

Here, we can see that the output of the comparison operators is also an array, where each element is either `True` or `False` based on the array element's comparison.

---

## NumPy Comparison Functions

NumPy also provides built-in functions to perform all the comparison operations.

For example, the `less()` function returns `True` if **each element** of the first array is less than the corresponding element in the second array.

Here's a list of all built-in comparison functions.

|Functions|Descriptions|
|---|---|
|`less()`|returns element-wise `True` if the first value is less than the second|
|`less_equal()`|returns element-wise `True` if the first value is less than or equal to second|
|`greater()`|returns element-wise `True` if the first value is greater then second|
|`greater_equal()`|returns element-wise `True` if the first value is greater than or equal to second|
|`equal()`|returns element-wise `True` if two values are equal|
|`not_equal()`|returns element-wise `True` if two values are not equal|

Next, we will see an example of all these functions.

---

## Example 2: NumPy Comparison Functions

```
import numpy as np

array1 = np.array([9, 12, 21])
array2 = np.array([21, 12, 9])

# use of less()
result = np.less(array1, array2)
print("Using less():",result)    # Output: [ True False False]

# use of less_equal()
result = np.less_equal(array1, array2)
print("Using less_equal():",result)     # Output: [ True  True False]

# use of greater()
result = np.greater(array1, array2)
print("Using greater():",result)    # Output: [False False  True]

# use of greater_equal()
result = np.greater_equal(array1, array2)
print("Using greater_equal():",result)    # Output: [False  True  True]

# use of equal()
result = np.equal(array1, array2)
print("Using equal():",result)    # Output: [False  True False]

# use of not_equal()
result = np.not_equal(array1, array2)
print("Using not_equal():",result)    # Output: [ True False  True]
```



**Output**

Using less(): [ True False False]
Using less_equal(): [ True  True False]
Using greater(): [False False  True]
Using greater_equal(): [False  True  True]
Using equal(): [False  True False]
Using not_equal(): [ True False  True]

---

## NumPy Logical Operations

As mentioned earlier, logical operators perform Boolean algebra; a branch of algebra that deals with `True` and `False` statements.

Logical operations are performed element-wise. For example, if we have two arrays `x1` and `x2` of the same shape, the output of the logical operator will also be an array of the same shape.

Here's a list of various logical operators available in NumPy:

|Operators|Descriptions|
|---|---|
|`logical_and`|Computes the element-wise truth value of **x1** `AND` **x2**|
|`logical_or`|Computes the element-wise truth value of **x1** `OR` **x2**|
|`logical_not`|Computes the element-wise truth value of `NOT` **x**|

Next, we will see examples of these operators.

---

## Example 3: NumPy Logical Operations

```
import numpy as np

x1 = np.array([True, False, True])
x2 = np.array([False, False, True])

# Logical AND
print(np.logical_and(x1, x2)) # Output: [False False  True]

# Logical OR
print(np.logical_or(x1, x2)) # Output: [ True False  True]

# Logical NOT
print(np.logical_not(x1)) # Output: [False  True False]
```



Here, we have performed logical operations on two arrays, x1 and x2, containing boolean values.

It demonstrates the logical **AND**, **OR**, and **NOT** operations using `np.logical_and()`, `np.logical_or()`, and `np.logical_not()` respectively.

# NumPy Math Functions

Numpy provides a wide range of mathematical functions that can be performed on arrays.

Let's explore three different types of math functions in NumPy:

1. Trigonometric Functions
2. Arithmetic Functions
3. Rounding Functions

---

## 1. Trigonometric Functions

NumPy provides a set of standard trigonometric functions to calculate the trigonometric ratios (sine, cosine, tangent, etc.)

Here's a list of commonly used trigonometric functions in NumPy.

|Trigonometric Function|Computes (in radians)|
|---|---|
|`sin()`|the sine of an angle|
|`cos()`|cosine of an angle|
|`tan()`|tangent of an angle|
|`arcsin()`|the inverse sine|
|`arccos()`|the inverse cosine|
|`arctan()`|the inverse tangent|
|`degrees()`|converts an angle in radians to degrees|
|`radians()`|converts an angle in degrees to radians|

Let's see the examples.

```
import numpy as np

# array of angles in radians
angles = np.array([0, 1, 2])
print("Angles:", angles)

# compute the sine of the angles
sine_values = np.sin(angles)
print("Sine values:", sine_values)

# compute the inverse sine of the angles
inverse_sine = np.arcsin(angles)
print("Inverse Sine values:", inverse_sine)
```



**Output**

Angles: [0 1 2]
Sine values: [0.         0.84147098 0.90929743]
Inverse Sine values: [0.         1.57079633        nan]

In this example, the `sin()` and `arcsin()` functions calculate the sine and inverse sine values, respectively, for each element in the angles array.

The resulting values are in radians.

Now let's see the examples for `degrees()` and `radians()`.

```
import numpy as np

# define an angle in radians
angle =  1.57079633
print("Initial angle in radian:", angle)

# convert the angle to degrees
angle_degree = np.degrees(angle)
print("Angle in degrees:", angle_degree)

# convert the angle back to radians
angle_radian = np.radians(angle_degree)
print("Angle in radians (after conversion):", angle_radian)
```
**Output**

Initial angle in radian: 1.57079633
Angle in degrees: 90.0000001836389
Angle in radians (after conversion): 1.57079633

Here, we first initialized an angle in radians. Then we converted it to degrees using the `degrees()` function.

Similarly, we used `radians()` to convert the degrees back to radians.

---

## 2. Arithmetic Functions

NumPy provides a wide range of arithmetic functions to perform on arrays.

Here's a list of various arithmetic functions along with their associated operators:

|Operation|Arithmetic Function|Operator|
|---|---|---|
|Addition|`add()`|`+`|
|Subtraction|`subtract()`|`-`|
|Multiplication|`multiply()`|`*`|
|Division|`divide()`|`/`|
|Exponentiation|`power()`|`**`|
|Modulus|`mod()`|`%`|

Let's see the examples.

```
import numpy as np

first_array = np.array([1, 3, 5, 7])
second_array = np.array([2, 4, 6, 8])

# using the add() function
result2 = np.add(first_array, second_array)
print("Using the add() function:",result2) 
```



**Output**

Using the add() function: [ 3  7 11 15]

In the above example, first we created two arrays named: first_array and second_array. Then, we used the `add()` function to perform element-wise addition respectively.

---

## 3. Rounding Functions

We use rounding functions to round the values in an array to a specified number of decimal places.

Here's a list of commonly used NumPy rounding functions:

|Rounding Functions|Functions|
|---|---|
|`round()`|returns the value rounded to the desired precision|
|`floor()`|returns the values of array down to the nearest integer that is less than each element|
|`ceil()`|returns the values of array up to the nearest integer that is greater than each element.|

Let's see an example.

```
import numpy as np

numbers = np.array([1.23456, 2.34567, 3.45678, 4.56789])

# round the array to two decimal places
rounded_array = np.round(numbers, 2)

print(rounded_array)

# Output: [1.23 2.35 3.46 4.57]
```


Here, we used the `round()` function to round the values of array numbers. Notice the line,

```
np.round(numbers, 2)
```

We've given two arguments to the `round()` function.

- numbers - the array whose values are to be rounded
- **2** - denotes the number of decimal places to which the array is rounded

Now, let's see the example of other NumPy rounding functions.

```
import numpy as np

array1 = np.array([1.23456, 2.34567, 3.45678, 4.56789])

print("Array after floor():", np.floor(array1))

print("Array after ceil():", np.ceil(array1))
```
**Output**

Array after floor(): [1. 2. 3. 4.]
Array after ceil(): [2. 3. 4. 5.]

In the above example, the `floor()` function rounds the values of array1 down to the nearest integer that is less than or equal to each element.

Whereas, the `ceil()` function rounds the values of array1 up to the nearest integer that is greater than or equal to each element.

# Numpy Constants

NumPy constants are the predefined fixed values used for mathematical calculations.

For example, `np.pi` is a mathematical constant that returns the value of pi (π), i.e. 3.141592653589793.

Using predefined constants makes our code concise and easier to read.

We'll discuss some common constants provided by Numpy library.

---

## Numpy Constants

In Numpy, the most commonly used constants are `pi` and `e`.

## np.pi

`np.pi` is a mathematical constant that returns the value of pi(π) as a floating point number. Its value is approximately **3.141592653589793**.

Let's see an example.

```
import numpy as np

radius = 2
circumference = 2 * np.pi * radius
print(circumference)
```
**Output**

12.566370614359172

Here, the `np.pi` returns the value **3.141592653589793**, which calculates the circumference.

Instead of the long floating point number, we used the constant `np.pi`. This made our code look cleaner.

**Note:** As `pi` falls under the Numpy library, we need to import and access it with `np.pi`.

---

## np.e

`np.e` is widely used with exponential and logarithmic functions. Its value is approximately **2.718281828459045**.

Let's see an example.

```
import numpy as np

y = np.e

print(y)
```
**Output**

2.718281828459045

In the above example, we simply printed the constant `np.e`. As we can see, it returns its value **2.718281828459045**.

However, this example makes no sense because that's not how we use the constant `e` in real life.

We usually use the constant `e` with the function `exp()`. `e` is the base of exponential function, `exp(x)`, which is equivalent to `e^x`.

Let's see an example.

```
import numpy as np

x = 1
y = np.exp(x)

print(y)
```
**Output**

2.718281828459045

As you can see, we got the same output like in the previous example. This is because

```
np.exp(x) 
```

is equivalent to

```
np.e ^ x
```

The value of x is **1**. So, `np.e^x` returns the value of the constant `e`.

---

## Arithmetic Operations with Numpy Constants and Arrays

We can use arithmetic operators to perform operations such as addition, subtraction, and division between a constant and all elements in an array.

Let's see an example.

```
import numpy as np

array1 = np.array([1, 2, 3])

# add each array element with the constant pi
y = array1 + np.pi

print(y)
```
**Output**

[4.14159265 5.14159265 6.14159265]

In this example, the value **3.141592653589793** (π) is added with each element of array1.

# NumPy Statistical Functions

Statistics involves gathering data, analyzing it, and drawing conclusions based on the information collected.

NumPy provides us with various statistical functions that can perform statistical data analysis.

---

## Common NumPy Statistical Functions

Here are some of the statistical functions provided by NumPy:

|Functions|Descriptions|
|---|---|
|`median()`|return the median of an array|
|`mean()`|return the mean of an array|
|`std()`|return the standard deviation of an array|
|`percentile()`|return the nth percentile of elements in an array|
|`min()`|return the minimum element of an array|
|`max()`|return the maximum element of an array|

Next, we will see examples using these functions.

---

## Find Median Using NumPy

The median value of a numpy array is the middle value in a **sorted array**.

In other words, it is the value that separates the higher half from the lower half of the data.

Suppose we have the following list of numbers:

```
1, 5, 7, 8, 9, 12, 14
```

Then, median is simply the middle number, which in this case is **8**.

It is important to note that if the number of elements is

- **Odd**, the median is the middle element.
- **Even**, the median is the average of the two middle elements.

Now, we will learn how to calculate the median using NumPy for arrays with odd and even number of elements.

---

## Example 1: Compute Median for Odd Number of Elements

```
import numpy as np

# create a 1D array with 5 elements
array1 = np.array([1, 2, 3, 4, 5])
                                                                                                           
# calculate the median
median = np.median(array1)

print(median) 

# Output: 3.0
```

In the above example, the array named array1 contains an odd number of elements (**5** elements).

So, `np.median(array1)` returns the median of `array1` as **3**, which is the middle value of the sorted array.

---

## Example 2: Compute Median for Even Number of Elements

```
import numpy as np

# create a 1D array with 6 elements
array1 = np.array([1, 2, 3, 4, 5, 7])

# calculate the median
median = np.median(array1)
print(median) 

# Output: 3.5
```


Here, since the array1 array has an even number of elements (**6** elements), the median is calculated as the average of the two middle elements (**3** and **4)** i.e. **3.5.**

---

## Median of NumPy 2D Array

Calculation of the median is not just limited to 1D array. We can also calculate the median of the 2D array.

In a 2D array, median can be calculated either along the horizontal or the vertical axis individually, or across the entire array.

When computing the median of a 2D array, we use the `axis` parameter inside `np.median()` to specify the axis along which to compute the median.

If we specify,

- `axis = 0`, median is calculated along vertical axis
- `axis = 1`, median is calculated along horizontal axis

If we don't use the `axis` parameter, the median is computed over the entire array.

---

### Example: Compute the median of a 2D array

```
import numpy as np

# create a 2D array
array1 = np.array([[2, 4, 6], 
                   [8, 10, 12], 
                   [14, 16, 18]])

# compute median along horizontal axis 
result1 = np.median(array1, axis=1)

print("Median along horizontal axis :", result1)

# compute median along vertical axis
result2 = np.median(array1, axis=0)

print("Median along vertical axis:", result2)

# compute median of entire array
result3 = np.median(array1)

print("Median of entire array:", result3)
```
**Output**

Median along horizontal axis : [ 4. 10. 16.]
Median along vertical axis: [ 8. 10. 12.]
Median of entire array: 10.0

In this example, we have created a 2D array named array1.

We then computed the median along the horizontal and vertical axis individually and then computed the median of the entire array.

- `np.median(array1, axis=1)` - median along horizontal axis, which gives `[4. 10. 16.]`
- `np.median(array1, axis=0)` - median along vertical axis, which gives `[8. 10. 12.]`
- `np.median(array1)` - median over the entire array, which gives `10.0`

To calculate the median over the entire 2D array, first we flatten the array to `[ 2, 4, 6, 8, 10, 12, 14, 16, 18]` and then find the middle value of the flattened array which in our case is **10**.

---

## Compute Mean Using NumPy

The mean value of a NumPy array is the average value of all the elements in the array.

It is calculated by adding all elements in the array and then dividing the result by the total number of elements in the array.

We use the `np.mean()` function to calculate the mean value. For example,

```
import numpy as np

# create a numpy array
marks = np.array([76, 78, 81, 66, 85])

# compute the mean of marks
mean_marks = np.mean(marks)

print(mean_marks)

# Output: 77.2
```



In this example, the mean value is **77.2**, which is calculated by adding the elements (**76, 78, 81, 66, 85**) and dividing the result by **5** (total number of array elements).

---

## Example 3: Mean of NumPy N-d Array

```
import numpy as np

# create a 2D array
array1 = np.array([[1, 3], 
                 [5, 7]])

# calculate the mean of the entire array
result1 = np.mean(array1)
print("Entire Array:",result1)  # 4.0

# calculate the mean along vertical axis (axis=0)
result2 = np.mean(array1, axis=0)
print("Along Vertical Axis:",result2)  # [3. 5.]

# calculate the mean along  (axis=1)
result3 = np.mean(array1, axis=1)
print("Along Horizontal Axis :",result3)  # [2. 6.]
```
**Output**

Entire Array: 4.0
Along Vertical Axis: [3. 5.]
Along Horizontal Axis : [2. 6.]

Here, first we have created the 2D array named array1. We then calculated the mean using `np.mean()`.

- `np.mean(array1)` - calculates the mean over the entire array
- `np.mean(array1, axis=0)` - calculates the mean along vertical axis
- `np.mean(array1, axis=1)` calculates the mean along horizontal axis

---

## Standard Deviation of NumPy Array

The standard deviation is a measure of the spread of the data in the array. It gives us the degree to which the data points in an array deviate from the mean.

- Smaller standard deviation indicates that the data points are closer to the mean
- Larger standard deviation indicates that the data points are more spread out.

In NumPy, we use the `np.std()` function to calculate the standard deviation of an array.

---

### Example: Compute the Standard Deviation in NumPy

```
import numpy as np

# create a numpy array
marks = np.array([76, 78, 81, 66, 85])

# compute the standard deviation of marks
std_marks = np.std(marks)
print(std_marks)

# Output: 6.803568381206575
```
In the above example, we have used the `np.std()` function to calculate the standard deviation of the `marks` array.

Here, `6.803568381206575` is the standard deviation of `marks`. It tells us how much the values in the `marks` array deviate from the mean value of the array.

---

## Standard Deviation of NumPy 2D Array

In a 2D array, standard deviation can be calculated either along the horizontal or the vertical axis individually, or across the entire array.

Similar to mean and median, when computing the standard deviation of a 2D array, we use the `axis` parameter inside `np.std()` to specify the axis along which to compute the standard deviation.

---

### Example: Compute the Standard Deviation of a 2D array.

```
import numpy as np

# create a 2D array
array1 = np.array([[2, 5, 9], 
                 [3, 8, 11], 
                 [4, 6, 7]])

# compute standard deviation along horizontal axis
result1 = np.std(array1, axis=1)
print("Standard deviation along horizontal axis:", result1)

# compute standard deviation along vertical axis
result2 = np.std(array1, axis=0)
print("Standard deviation  along vertical axis:", result2)

# compute standard deviation of entire array
result3 = np.std(array1)
print("Standard deviation of entire array:", result3)
```


**Output**

Standard deviation along horizontal axis: [2.86744176 3.29983165 1.24721913]
Standard deviation along vertical axis: [0.81649658 1.24721913 1.63299316]
Standard deviation of entire array: 2.7666443551086073

Here, we have created a 2D array named array1.

We then computed the standard deviation along horizontal and vertical axis individually and then computed the standard deviation of the entire array.

---

## Compute Percentile of NumPy Array

In NumPy, we use the `percentile()` function to compute the nth percentile of a given array.

Let's see an example.

```
import numpy as np

# create an array
array1 = np.array([1, 3, 5, 7, 9, 11, 13, 15, 17, 19])

# compute the 25th percentile of the array
result1 = np.percentile(array1, 25)
print("25th percentile:",result1)

# compute the 75th percentile of the array
result2 = np.percentile(array1, 75)
print("75th percentile:",result2)
```
**Output**

25th percentile: 5.5
75th percentile: 14.5

Here,

- **25%** of the values in array1 are less than or equal to **5.5**.
- **75%** of the values in array1 are less than or equal to **14.5**.

**Note**: To learn more about percentile, visit _NumPy Percentile_.

---

## Find Minimum and Maximum Value of NumPy Array

We use the `min()` and `max()` function in NumPy to find the minimum and maximum values in a given array.

Let's see an example.

```
import numpy as np

# create an array
array1 = np.array([2,6,9,15,17,22,65,1,62])

# find the minimum value of the array
min_val = np.min(array1)

# find the maximum value of the array
max_val = np.max(array1)

# print the results
print("Minimum value:", min_val)
print("Maximum value:", max_val)
```
**Output**

Minimum value: 1
Maximum value: 65

As we can see `min()` and `max()` returns the minimum and maximum value of array1 which is **1** and **65** respectively.

**Note**: To learn more about `min()` and `max()`, visit _NumPy min()_ and _NumPy max()_.
# NumPy String Functions

In addition to NumPy's numerical capabilities, it also provides several functions that can be applied to strings represented in NumPy arrays.

For example, we can add two strings, change the contents of a string, case conversion, padding, trimming, and so on.

---

## Common NumPy String Functions

Here are some of the string functions provided by NumPy:

|Functions|Descriptions|
|---|---|
|`add()`|concatenates two strings|
|`multiply()`|repeats a string for a specified number of times|
|`capitalize()`|capitalizes the first letter of a string|
|`lower()`|converts all uppercase characters in a string to lowercase|
|`upper()`|converts all lowercase characters in a string to uppercase|
|`join()`|joins a sequence of strings|
|`equal()`|checks if two strings are equal or not|


---

## NumPy String add() Function

In NumPy, we use the `np.char.add()` function to perform element-wise string concatenation for two arrays of strings. For example,

```
import numpy as np

array1 = np.array(['iPhone: ', 'price: '])
array2 = np.array(['15', '$900'])

# perform element-wise array string concatenation
result = np.char.add(array1, array2)

print(result)
```
**Output**

['iPhone: 15' 'price: $900']

In this example, we have defined two NumPy arrays: array1 and array2, with string elements `'iphone: '` and `'price: '` and `'15'` and `'$900'` respectively.

We then used `np.char.add(array1, array2)` to concatenate the elements of array1 and array2 element-wise.

Finally, we have stored the concatenated string in `result`, which in our case are `'iPhone: 15'` and `'price: $900'`.

---

## NumPy String multiply() Function

The `np.char.multiply()` function is used to perform element-wise string repetition. It returns an array of strings with each string element repeated a specified number of times.

Let's see an example.

```
import numpy as np  

# define array with three string elements
array1 = np.array(['A', 'B', 'C']) 

#  repeat each element in array1 two times 
result = np.char.multiply(array1, 2)  

print(result)  

# Output: ['AA' 'BB' 'CC']
```
Here, `np.char.multiply(array1, 2)` repeats each element in array1 two times.

---

## NumPy String capitalize() Function

In NumPy, the `np.char.capitalize()` function is used to capitalize the first character of each string element in a given array. For example,

```
import numpy as np  

# define an array with three string elements
array1 = np.array(['eric', 'paul', 'sean'])  

# capitalize the first letter of each string in array1 
result = np.char.capitalize(array1)  

print(result) 

# Output: ['Eric' 'Paul' 'Sean']
```



In this example, `np.char.capitalize(array1)` capitalizes the first character of the string element in the array1 array.

---

## NumPy String upper() and lower() Function

NumPy provides two string functions for converting the case of a string: `np.char.upper()` and `np.char.lower()`.

Let's see an example.

```
import numpy as np

array1 = np.array(['nEpalI', 'AmeriCAN', 'CaNadIan'])

# convert all string elements to uppercase
result1 = np.char.upper(array1)

# convert all string elements to lowercase
result2 = np.char.lower(array1)

print("To Uppercase: ",result1)
print("To Lowercase: ",result2)
```
**Output**

To Uppercase:  ['NEPALI' 'AMERICAN' 'CANADIAN']
To Lowercase:  ['nepali' 'american' 'canadian']

Here,

- `np.char.upper(array1)` - convert all strings in array1 to uppercase
- `np.char.lower(array1)` - convert all strings in array1 to lowercase

---

## NumPy String join() Function

In NumPy, we use the `np.char.join()` function to join strings in an array with a specified delimiter. For example,

```
import numpy as np

# create an array of strings
array1 = np.array(['hello', 'world'])

# join the strings in the array using a dash as the delimiter
result = np.char.join('-', array1)

print(result)

# Output: ['h-e-l-l-o' 'w-o-r-l-d']
```



In this example, the `np.char.join('-', array1)` function is used to join the strings in array1 using dash `-` as the delimiter.

The resulting strings have each character separated by a dash.

---

## NumPy String equal() Function

The `np.char.equal()` function is used to perform element-wise string comparison between two string arrays.

Let's see an example.

```
import numpy as np

# create two arrays of strings
array1 = np.array(['C', 'Python', 'Swift'])
array2 = np.array(['C++', 'Python', 'Java'])

# check if each element of the arrays is equal
result = np.char.equal(array1, array2)

print(result)

# Output: [False True False]
```



Here, `np.char.equal(array1, array2)` checks whether the corresponding elements of array1 and array2 are equal or not.

The resulting boolean array `[False True False]` indicates that the first and third elements of array1 and array2 are not equal, while the second element is equal.
# Numpy Broadcasting

In NumPy, we can perform mathematical operations on arrays of different shapes. An array with a smaller shape is expanded to match the shape of a larger one. This is called broadcasting.

Let's see an example.

```
array1 = [1, 2, 3]
array2 = [[1], [2], [3]]
```

array1 is a 1-D array and array2 is a 2-D array. Let's perform addition between these two arrays of different shapes.

```
result = array1 + array2
```

Here, NumPy automatically broadcasts the size of a 1-D array array1 to perform element-wise addition with a 2-D array array2.

---

### Example: NumPy Broadcasting

```
import numpy as np

# create 1-D array
array1 = np.array([1, 2, 3])

# create 2-D array
array2 = np.array([[1], [2], [3]])

# add arrays of different dimension
# size of array1 expands to match with array2
sum = array1 + array2

print(sum)
```


**Output**

[[2 3 4]
 [3 4 5]
 [4 5 6]]

In the example, we added two arrays with different dimensions. Numpy automatically expands the size of 1-D array array1 to match with the size of 2-D array array2.

Then, the element-wise addition is performed between two 2-D arrays.

---

## Compatibility Rules for Broadcasting

Broadcasting only works with compatible arrays. NumPy compares a set of array dimensions from right to left.

Every set of dimensions must be compatible with the arrays to be broadcastable. A set of dimension lengths is compatible when

- one of them has a length of **1** or
- they are equal

Let's see an example.

```
array1 = shape(6, 7)
array2 = shape(6, 1)
```

Here, array1 and array2 are arrays with different dimensions `(6,7)` and `(6,1)` respectively.

The dimension length **7** and **1** are compatible because one of them is **1**.

Similarly, **6** and **6** are compatible since they are the same.

As both sets of dimensions are compatible, the arrays are broadcastable.

---

### Examples of Broadcastable Shapes

Now, we'll see the list of broadcastable and non-broadcastable shapes.

**Broadcastable Shapes**

- `(6, 7)` and `(6, 7)`
- `(6, 7)` and `(6, 1)`
- `(6, 7)` and `(7, )`

Two arrays need not have the same number of dimensions to be broadcastable.

The last set of shapes is broadcastable because the right-most dimensions are both **7**.

**Non-Broadcastable Shapes**

- `(6, 7)` and `(7, 6)`
- `(6, 7)` and `(6, )`

The last set of shapes is not broadcastable because the right-most dimensions are not the same.

---

## Broadcasting with Scalars

We can also perform mathematical operations between arrays and scalars (single values). For example,

```
import numpy as np

# 1-D array
array1 = np.array([1, 2, 3])

# scalar
number = 5

# add scalar and 1-D array
sum = array1 + number

print(sum)
```
**Output**

[6 7 8]

In this example, NumPy automatically expands the scalar number to an 1-D array and then performs the element-wise addition.

# NumPy Matrix Operations

A matrix is a two-dimensional data structure where numbers are arranged into rows and columns. For example,

A matrix is a two-dimensional data structure.

The above matrix is a **3x3** (pronounced "three by three") matrix because it has **3** rows and **3** columns.

---

## NumPy Matrix Operations

Here are some of the basic matrix operations provided by NumPy.

|Functions|Descriptions|
|---|---|
|`array()`|creates a matrix|
|`dot()`|performs matrix multiplication|
|`transpose()`|transposes a matrix|
|`linalg.inv()`|calculates the inverse of a matrix|
|`linalg.det()`|calculates the determinant of a matrix|
|`flatten()`|transforms a matrix into 1D array|

---

## Create Matrix in NumPy

In NumPy, we use the `np.array()` function to create a matrix. For example,

```
import numpy as np

# create a 2x2 matrix
matrix1 = np.array([[1, 3], 
                   [5, 7]])

print("2x2 Matrix:\n",matrix1)

# create a 3x3  matrix
matrix2 = np.array([[2, 3, 5],
             	    [7, 14, 21],
                    [1, 3, 5]])
                    
print("\n3x3 Matrix:\n",matrix2)
```
**Output**

2x2 Matrix:
[[1 3]
 [5 7]]

3x3 Matrix:
 [[ 2  3  5]
 [ 7 14 21]
 [ 1  3  5]]

Here, we have created two matrices: **2x2** matrix and **3x3** matrix by passing a list of lists to the `np.array()` function respectively.

---

## Perform Matrix Multiplication in NumPy

We use the `np.dot()` function to perform multiplication between two matrices.

Let's see an example.

```
import numpy as np

# create two matrices
matrix1 = np.array([[1, 3], 
             		[5, 7]])
             
matrix2 = np.array([[2, 6], 
                    [4, 8]])

# calculate the dot product of the two matrices
result = np.dot(matrix1, matrix2)

print("matrix1 x matrix2: \n",result)
```
**Output**

matrix1 x matrix2: 
[[14 30]
 [38 86]]

In this example, we have used the np.dot(matrix1, matrix2) function to perform matrix multiplication between two matrices: matrix1 and matrix2.

To learn more about Matrix multiplication, please visit _NumPy Matrix Multiplication_.

**Note**: We can only take a dot product of matrices when they have a common dimension size. For example, For `A = (M x N)` and `B = (N x K)` when we take a dot product of `C = A . B` the resulting matrix is of size `C = (M x K)`.

---

## Transpose NumPy Matrix

The transpose of a matrix is a new matrix that is obtained by exchanging the rows and columns. For 2x2 matrix,

```
Matrix:
a11    a12    
a21    a22    

Transposed Matrix:
a11    a21
a12    a22
```

In NumPy, we can obtain the transpose of a matrix using the `np.transpose()` function. For example,

```
import numpy as np

# create a matrix
matrix1 = np.array([[1, 3], 
             		[5, 7]])

# get transpose of matrix1
result = np.transpose(matrix1)

print(result)
```
**Output**

[[1 5]
 [3 7]]

Here, we have used the `np.transpose(matrix1)` function to obtain the transpose of matrix1.

**Note**: Alternatively, we can use the `.T` attribute to get the transpose of a matrix. For example, if we used `matrix1.T` in our previous example, the result would be the same.

---

## Calculate Inverse of a Matrix in NumPy

In NumPy, we use the `np.linalg.inv()` function to calculate the inverse of the given matrix.

However, it is important to note that not all matrices have an inverse. Only square matrices that have a non-zero determinant have an inverse.

Now, let's use `np.linalg.inv()` to calculate the inverse of a square matrix.

```
import numpy as np

# create a 3x3 square matrix
matrix1 = np.array([[1, 3, 5], 
             		[7, 9, 2],
                    [4, 6, 8]])

# find inverse of matrix1
result = np.linalg.inv(matrix1)

print(result)
```
**Output**

[[-1.11111111 -0.11111111  0.72222222]
 [ 0.88888889  0.22222222 -0.61111111]
 [-0.11111111 -0.11111111  0.22222222]]

**Note**: If we try to find the inverse of a non-square matrix, we will get an error message: `numpy.linalg.linalgerror: Last 2 dimensions of the array must be square`

---

## Find Determinant of a Matrix in NumPy

We can find the determinant of a square matrix using the `np.linalg.det()` function to calculate the determinant of the given matrix.

Suppose we have a **2x2** matrix `A`:

```
a b
c d
```

So, the determinant of a **2x2** matrix will be:

```
det(A) = ad - bc
```

where **a, b, c,** and **d** are the elements of the matrix.

Let's see an example.

```
import numpy as np

# create a matrix
matrix1 = np.array([[1, 2, 3], 
             		[4, 5, 1],
                    [2, 3, 4]])

# find determinant of matrix1
result = np.linalg.det(matrix1)

print(result)
```
**Output**

-5.00

Here, we have used the `np.linalg.det(matrix1)` function to find the determinant of the square matrix matrix1.

---

## Flatten Matrix in NumPy

Flattening a matrix simply means converting a matrix into a 1D array.

To flatten a matrix into a 1-D array we use the `array.flatten()` function. Let's see an example.

```
import numpy as np

# create a 2x3 matrix
matrix1 = np.array([[1, 2, 3], 
             		[4, 5, 7]])

result = matrix1.flatten()
print("Flattened 2x3 matrix:", result)
```
**Output**

Flattened 2x3 matrix: [1 2 3 4 5 7]

Here, we have used the `matrix1.flatten()` function to flatten matrix1 into a 1D array, without compromising any of its elements

# NumPy Set Operations

A set is a collection of unique data. That is, elements of a set cannot be repeated.

NumPy set operations perform mathematical set operations on arrays like union, intersection, difference, and symmetric difference.

---

## Set Union Operation in NumPy

The union of two sets **A** and **B** include all the elements of set **A** and **B**.


Set Union in NumPy

In NumPy, we use the `np.union1d()` function to perform the set union operation in an array. For example,

```
import numpy as np

A = np.array([1, 3, 5])
B = np.array([0, 2, 3])

# union of two arrays
result = np.union1d(A, B)

print(result)  

# Output: [0 1 2 3 5]
```



In this example, we have used the `np.union1d(A, B)` function to compute the union of two arrays: A and B.

Here, the function returns unique elements from both arrays.

**Note**: `np.union1d(A,B)` is equivalent to `A ⋃ B` set operation.

---

## Set Intersection Operation in NumPy

The intersection of two sets **A** and **B** include the common elements between set **A** and **B**.

Set Intersection in NumPy

We use the `np.intersect1d()` function to perform the set intersection operation in an array. For example,

```
import numpy as np

A = np.array([1, 3, 5])
B = np.array([0, 2, 3])

# intersection of two arrays
result = np.intersect1d(A, B)

print(result)  

# Output: [3]
```



**Note**: `np.intersect1d(A,B)` is equivalent to `A ⋂ B` set operation.

---

## Set Difference Operation in NumPy

The difference between two sets **A** and **B** include elements of set **A** that are not present on set **B**.

Set Difference in NumPy

We use the `np.setdiff1d()` function to perform the difference between two arrays. For example,

```
import numpy as np

A = np.array([1, 3, 5])
B = np.array([0, 2, 3])

# difference of two arrays
result = np.setdiff1d(A, B)

print(result)  

# Output: [1 5]
```



**Note**: `np.setdiff1d(A,B)` is equivalent to `A - B` set operation.

---

## Set Symmetric Difference Operation in NumPy

The symmetric difference between two sets **A** and **B** includes all elements of **A** and **B** without the common elements.

Set Symmetric Difference in NumPy

In NumPy, we use the `np.setxor1d()` function to perform symmetric differences between two arrays. For example,

```
import numpy as np

A = np.array([1, 3, 5])
B = np.array([0, 2, 3])

# symmetric difference of two arrays
result = np.setxor1d(A, B)

print(result)  

# Output: [0 1 2 5]
```
---

## Unique Values From a NumPy Array

To select the unique elements from a NumPy array, we use the `np.unique()` function. It returns the sorted unique elements of an array. It can also be used to create a set out of an array.

Let's see an example.

```
import numpy as np

array1 = np.array([1,1, 2, 2, 4, 7, 7, 3, 5, 2, 5])

# unique values from array1
result = np.unique(array1)

print(result)  

# Output: [1 2 3 4 5 7]
```



Here, the resulting array `[1 2 3 4 5 7]` contains only the unique elements of the original array array1.
# NumPy Vectorization

NumPy vectorization involves performing mathematical operations on entire arrays, eliminating the need to loop through individual elements.

We will see an overview of NumPy vectorization and demonstrate its advantages through examples.

---

## NumPy Vectorization

We've used the concept of vectorization many times in NumPy. It refers to performing element-wise operations on arrays.

Let's take a simple example. When we add a number with a NumPy array, it adds up with each element of the array.

```
import numpy as np

array1 = np.array([1, 2, 3, 4, 5 ])
number = 10

#  number sums up with each array element
result = array1 + number

print(result)
```
**Output**

[11 12 13 14 15]

Here, the number **10** adds up with each array element. This is possible because of vectorization.

Without vectorization, performing the operation would require the use of loops.

---

### Example: Numpy Vectorization to Add Two Arrays Together

```
import numpy as np

# define two 2D arrays
array1 = np.array([[1, 2, 3], [4, 5, 6]])
array2 = np.array([[0, 1, 2], [0, 1, 2]])

# add two arrays (vectorization)
array_sum = array1 + array2

print("Sum between two arrays:\n", array_sum)
```
**Output**

Sum between two arrays:
[[1 3 5]
 [4 6 8]]

In this example, we have created two 2D arrays array1 and array2, and added them together.

This is a vectorized operation, where corresponding elements of two arrays are added together element-wise.

---

## NumPy Vectorization Vs Python for Loop

Even though NumPy is a Python library, it inherited vectorization from C programming. As C is efficient in terms of speed and memory, NumPy vectorization is also much faster than Python.

Let's compare the time it takes to perform a vectorized operation with that of an equivalent loop-based operation.

**Python for loop**

```
import time

start = time.time()

array1 = [1, 2, 3, 4, 5]

for i in range(len(array1)):
    array1[i] += 10

end = time.time()

print("For loop time:", end - start)
```
**Output**

For loop time: 4.76837158203125e-06

**NumPy Vectorization**

```
import numpy as np
import time

start = time.time()

array1 = np.array([1, 2, 3, 4, 5 ])

result = array1 + 10

end = time.time()

print("Vectorization time:", end - start)
```
**Output**

Vectorization time: 1.5020370483398438e-05

Here, the difference in execution time between vectorization and a for loop is significant, even for simple operation.

This comparison illustrates the performance benefits of vectorization, especially when working with large datasets.

---

## NumPy Vectorize() Function

In NumPy, every mathematical operation with arrays is automatically vectorized. So we don't always need to use the `vectorize()` function.

Let's take a scenario. You have an array and a function that returns the square of a positive number.

```
import numpy as np

# array
array1 = np.array([-1, 0, 2, 3, 4])

# function that returns the square of a positive number
def find_square(x):
    if x < 0:
        return 0
    else:
        return x ** 2
```
Now, to apply the function `find_square()` to array1, we have two options: use a loop or vectorize the operation.

Since loops are complicated and slow by nature, it's efficient and convenient to use `vectorize()`.

Let's see an example.

```
import numpy as np

# array whose square we need to find
array1 = np.array([-1, 0, 2, 3, 4])

# function to find the square
def find_square(x):
    if x < 0:
        return 0
    else:
        return x ** 2
        
# vectorize() to vectorize the function find_square()
vectorized_function = np.vectorize(find_square)

# passing an array to a vectorized function
result = vectorized_function(array1)

print(result)
```
**Output**

[ 0  0  4  9 16]

In this example, we used the `vectorize()` function to vectorize the `find_square()` function. We then passed array1 as a parameter to the vectorized function.

# NumPy Boolean Indexing

In NumPy, boolean indexing allows us to filter elements from an array based on a specific condition.

We use boolean masks to specify the condition.

Before we learn about boolean indexing, we need to know about boolean masks.

---

## Boolean Masks in NumPy

Boolean mask is a numpy array containing truth values (True/False) that correspond to each element in the array.

Suppose we have an array named array1.

```
array1 = np.array([12, 24, 16, 21, 32, 29, 7, 15])
```

Now let's create a mask that selects all elements of array1 that are greater than **20**.

```
boolean_mask = array1 > 20
```

Here, `array1 > 20` creates a boolean mask that evaluates to `True` for elements that are greater than **20**, and `False` for elements that are less than or equal to **20**.

The resulting mask is an array stored in the boolean_mask variable as:

```
[False, True, False, True, True, True, False, False]
```

---

## 1D Boolean Indexing in NumPy

Boolean Indexing allows us to create a filtered subset of an array by passing a boolean mask as an index.

The boolean mask selects only those elements in the array that have a `True` value at the corresponding index position.

Let's create a boolean indexing of the boolean mask in the above example.

```
array1[boolean_mask]
```

This results in

```
[24, 21, 32, 29]
```

Now let's see another example.

We'll use the boolean indexing to select only the odd numbers from an array.

```
import numpy as np

# create an array of numbers
array1 = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# create a boolean mask
boolean_mask = array1 % 2 != 0

# boolean indexing to filter the odd numbers
result = array1[boolean_mask]

print(result)

# Output: [ 1  3  5  7 9]
```


In this example, we have used the boolean indexing to select only the odd numbers from the array1 array.

Here, the expression `numbers % 2 != 0` is a boolean mask. If the elements of array1 meet the condition specified in the boolean mask, it replaces the element (odd numbers) with `True`, and even numbers with `False`.

With boolean indexing, a filtered array with only the `True` valued elements is returned. Hence, we get an array with odd numbers.

---

### Example: 1D Boolean Indexing in NumPy

```
import numpy as np

# create an array of integers
array1 = np.array([1, 2, 4, 9, 11, 16, 18, 22, 26, 31, 33, 47, 51, 52])

# create a boolean mask using combined logical operators
boolean_mask = (array1 < 10) | (array1 > 40)

# apply the boolean mask to the array 
result = array1[boolean_mask]

print(result)

# Output: [ 1  2  4  9 47 51 52]
```



Here, we have created a boolean mask using the `|` operator to select all the elements in array1 that are less than **10** or greater than **40**.

---

## Modify Elements Using Boolean Indexing

In NumPy, we can use boolean indexing to modify elements of the array. For example,

```
import numpy as np

# create an array of numbers
numbers = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# make a copy of the array
numbers_copy = numbers.copy()

# change all even numbers to 0 in the copy
numbers_copy[numbers % 2 == 0] = 0

# print the modified copy
print(numbers_copy)

# Output: [1 0 3 0 5 0 7 0 9 0]
```

Here, `numbers_copy[numbers % 2 == 0]` accesses all even numbers of the array and then we have assigned **0** to those numbers.

---

## 2D Boolean Indexing in NumPy

Boolean indexing can also be applied to multi-dimensional arrays in NumPy.

Let's see an example.

```
import numpy as np

# create a 2D  array
array1 = np.array([[1, 7, 9], 
                    [14, 19, 21], 
                    [25, 29, 35]])

# create a boolean mask based on the condition 
# that elements are greater than 9
boolean_mask = array1 > 9

# select only the elements that satisfy the condition
result = array1[boolean_mask]

print(result)
```
**Output**

[14 19 21 25 29 35]

In this example, we have applied boolean indexing to the 2D array named array1.

We then created boolean_mask based on the condition that elements are greater than **9**. The resulting mask is,

```
[[False, False, False], 
 [ True,  True,  True], 
 [ True,  True,  True]]
```

We then use this boolean mask to index array1, which returns a flattened 1D array containing only the elements that satisfy the condition.

```
[14, 19, 21, 25, 29, 35]
```

# NumPy Fancy Indexing

In NumPy, fancy indexing allows us to use an array of indices to access multiple array elements at once.

Fancy indexing can perform more advanced and efficient array operations, including conditional filtering, sorting, and so on.

---

## Select Multiple Elements Using NumPy Fancy Indexing

```
import numpy as np

# create a numpy array
array1 = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# select elements at index 1, 2, 5, 7
select_elements = array1[[1, 2, 5, 7]]

print(select_elements)

# Output: [2 3 6 8]
```
In this example, the resulting array select_elements contains the elements of array1 that correspond to the indices `[1, 2, 5, 7]` which are **2, 3, 6**, and **8** respectively.

---

### Example: NumPy Fancy Indexing

```
import numpy as np

array1 = np.array([1, 2, 3, 4, 5, 6, 7, 8])

# select a single element
simple_indexing = array1[3]

print("Simple Indexing:",simple_indexing)   # 4

# select multiple elements
fancy_indexing = array1[[1, 2, 5, 7]]

print("Fancy Indexing:",fancy_indexing)   # [2 3 6 8]
```
**Output**

Simple Indexing: 4
Fancy Indexing: [2 3 6 8]


---

## Fancy Indexing for Sorting NumPy Array

Fancy indexing can also sort a NumPy array. Let's see an example.

```
import numpy as np

array1 = np.array([3, 2, 6, 1, 8, 5, 7, 4])

# sort array1 using fancy indexing
sorted_array = array1[np.argsort(array1)]

print(sorted_array)

# Output: [1, 2, 3, 4, 5, 6, 7, 8]
```
Here, we are using the fanc
We could also use fancy indexing to sort the array in descending order.

```
import numpy as np

array1 = np.array([3, 2, 6, 1, 8, 5, 7, 4])

# sort array1 using fancy indexing in descending order
sorted_array = array1[np.argsort(-array1)]

print(sorted_array)

# Output: [8 7 6 5 4 3 2 1]
```
Here, first we multiplied array1 by **-1** to sort in descending order and then used the fancy indexing to return the sorted array.

---

## Fancy Indexing to Assign New Values to Specific Elements

We can also assign new values to specific elements of a NumPy array using fancy indexing. For example,

```
import numpy as np

array1 = np.array([3, 2, 6, 1, 8, 5, 7, 4])

# create a list of indices to assign new values
indices = [1, 3, 6]

# create a new array of values to assign
new_values = [10, 20, 30]

# use fancy indexing to assign new values to specific elements
array1[indices] = new_values

print(array1)

# Output: [ 3 10  6 20  8  5 30  4]
```
In this example, first we have created a list of indices called indices which specifies the elements of array1 that we want to assign new values to.

Then we created the array for new values called new_values that we want to assign to the specified indices.

Finally, we used fancy indexing with the list of indices to assign the new values to the specified elements of array1.

---

## Fancy Indexing on N-d Arrays

We can also use fancy indexing on multi-dimensional arrays.

Let's see an example to select specific rows using fancy indexing.

```
import numpy as np

# create a 2D array
array1 = np.array([[1, 3, 5], 
                [11, 7, 9], 
                [13, 18, 29]])

# create an array of row indices
row_indices = np.array([0, 2])

# use fancy indexing to select specific rows
selected_rows = array1[row_indices, :]

print(selected_rows)
```
**Output**

[[ 1  3  5]
 [13 18 29]]

Here, we have created a 2D array named array1 and an array of row indices named row_indices.

Then, we used fancy indexing to select the rows with indices **0** and **2** from array1.



# Numpy Random

In NumPy, we have a module called `random` which provides functions for generating random numbers.

These functions can be useful for generating random inputs for testing algorithms.

---

## Generate Random Integer in NumPy

As discussed earlier, we use the `random` module to work with random numbers in NumPy.

Let's see an example.

```
import numpy as np

# generate random integer from 0 to 9
random_number = np.random.randint(0, 10)

print(random_number)

# Output: 7
```
In this example, we have used the `random` module to generate a random number. The `random.randint()` function takes two arguments,

- **0** - a lower bound (inclusive)
- **10** - an upper bound (exclusive)

Here, `random.randint()` returns a random integer between **0** and **9**.

Since the output will be a randomly generated integer between **0** and **9**, we will see different outputs each time the code is run.

**Note**: We can also import and use the `random` module like this:

```
from numpy import random

random_number = random.randint(0, 10)

print(random_number)
```
Here, the syntax is slightly different but the output will be the same as above, we will get a random integer between **0** and **9**.

---

## Generate Random Float in NumPy

We can also generate a random floating-point number between **0** and **1**. For that we use the `random.rand()` function. For example,

```
import numpy as np

# generate random float-point number between 0 and 1
random_number = np.random.rand()

print(random_number)

# Output: 0.7696638323107154
```

Here, `random.rand()` generates a random floating-point number between **0** and **1**.

Since the number is generated randomly, the output value can vary each time the code is run.

---

## Generate Random Array in NumPy

NumPy's random module can also be used to generate an array of random numbers. For example,

```
import numpy as np

# generate 1D array of 5 random integers between 0 and 9
integer_array = np.random.randint(0, 10, 5)

print("1D Random Integer Array:\n",integer_array)

# generate 1D array of 5 random numbers between 0 and 1
float_array = np.random.rand(5)

print("\n1D Random Float Array:\n",float_array)

# generate 2D array of shape (3, 4) with random integers
result = np.random.randint(0, 10, (3,4))

print("\n2D Random Integer Array:\n",result)
```
**Output**

1D Random Integer Array:
[9 7 8 4 2]

1D Random Float Array:
 [0.7877579  0.01723754 0.93995075 0.17126388 0.69913594]

2D Random Integer Array:
 [[0 5 3 8]
 [3 9 2 1]
 [8 7 1 2]]

Here,

- `np.random.randint(0, 10, 5)` - generates a 1D array of **5** random integers between **0** and **9**.
- `np.random.rand(5)` - generates a 1D array of **5** random numbers between **0** and **1**.
- `np.random.randint(0, 10, (3,4))` - generates a 2D array of shape **(3, 4)** with random integers between **0** and **9**.

---

## Choose Random Number from NumPy Array

To choose a random number from a NumPy array, we can use the `random.choice()` function.

Let's see an example.

```
import numpy as np

# create an array of integers from 1 to 5
array1 = np.array([1, 2, 3, 4, 5])

# choose a random number from array1
random_choice = np.random.choice(array1)

print(random_choice)

# Output: 3
```
In the above example, the `np.random.choice(array1)` function chooses a random number from the array1 array.

It is important to note that the output will be a single random number from array1, which will be different each time the code is run.

# Numpy Linear Algebra

Linear algebra deals with mathematical concepts related to linear equations and their representations using matrices.

NumPy provides us with functions for performing common linear algebra tasks, such as array multiplication, solving linear systems, and more.

---

## NumPy Linear Algebra Functions

Here's a list of various functions for performing linear algebra tasks in NumPy.

|Operators|Descriptions|
|---|---|
|`dot()`|calculates product of two arrays|
|`inner()`|calculates inner product of arrays|
|`outer()`|calculates outer product of arrays|
|`det()`|calculates determinant of a matrix|
|`solve()`|solves linear matrix equation|
|`inv()`|calculates the multiplicative inverse of the matrix|
|`trace()`|calculates the sum of diagonal elements|

---

## NumPy dot() Function

We can use the `dot()` function available in NumPy's linear algebra module to calculate the product of two arrays. For example,

```
import numpy as np

array1 = np.array([1, 3, 5])
array2 = np.array([2, 4, 6])

# use of dot() to perform array multiplication
result = np.dot(array1, array2)

print(result)

# Output: 44
```


In this example, the `dot(array1, array2)` function computes the dot product of array1 and array2, which is equal to **1*2 + 3*4 + 5*6 = 44**.

---

## NumPy inner() Function

In NumPy, the `inner()` function computes the inner product of two arrays, which is the sum of the products of their corresponding entries.

Let's see an example of `inner()` with 2D arrays.

```
import numpy as np

array1 = np.array([[1, 3], 
                   [5, 7]])
array2 = np.array([[2, 4], 
                   [6, 8]])

# inner() for 2D arrays
result = np.inner(array1, array2)

print(result)
```
**Output**

[[14 30]
 [38 86]]

In the above example, `inner()` first _flattens_ 2D arrays to 1D arrays and then computes the inner product of those flattened arrays.

The resulting 2x2 matrix is the reshaped version of the flattened result.

Here, the inner product is calculated as:

```
1*2+3*4        1*6+3*8
5*2+7*4        5*6+7*8
```

**Note:** For 1D arrays, `inner()` is equivalent to `dot()`.

---

## NumPy outer() Function

The `outer()` function in NumPy computes the outer product of two arrays, which is the product of all possible pairs of their entries.

Let's see an example.

```
import numpy as np

array1 = np.array([1, 3, 5])
array2 = np.array([2, 4, 6])

# outer() to perform outer multiplication
result = np.outer(array1, array2)

print(result)
```


**Output**

[[ 2  4  6]
 [ 6 12 18]
 [10 20 30]]

Here, the outer product is calculated as:

```
1*2      1*4       1*6        
3*2      3*4       3*6
5*2      5*4       5*6
```

---

## NumPy det() Function

In NumPy, we use the `det()` function from the NumPy `linalg` module to calculate the determinant of a square matrix. For example,

```
import numpy as np

# define a square matrix
array1 = np.array([[1, 3], 
                  [5, 7]])

# compute the determinant of array1
result = np.linalg.det(array1)


print(result)
 
# Output: -7.9999999
```


Here, we have used the `det()` function from the `linalg` module to calculate the determinant of the square matrix named array1.

---

## NumPy solve() Function

In NumPy, we use the `solve()` function to solve a system of linear equations.

For a given matrix `A` and a vector `b`, `solve(A, b)` finds the solution vector `x` that satisfies the equation `Ax = b`.

Let's see an example.

```
import numpy as np

# define the coefficient matrix A
A = np.array([[2, 4], 
             [6, 8]])

# define the constant vector b
b = np.array([5, 6])

# solve the system of linear equations Ax = b
x = np.linalg.solve(A, b)

print(x)

# Output: [-2.  2.25]
```


In this example, we have used the `solve()` function from the `linalg` module to solve the system of linear equations.

Here, the output is `[-2. 2.25]`, which is the solution to the system of linear equations **2x + 4y = 5** and **6x + 8y = 6**.

**Note**: The `solve()` function only works for square matrices, and it assumes that the matrix `A` has a non-zero determinant, else `solve()` will raise a `LinAlgError` exception.

---

## NumPy inv() Function

We use the `inv()` function from the `linalg` module in NumPy to find the inverse of a square matrix. For example,

```
import numpy as np

# define a 2x2 matrix
array1 = np.array([[2, 4], 
                  [6, 8]])

# compute the inverse of the matrix
result = np.linalg.inv(array1)

print(result)
```
**Output**

[[-1.    0.5 ]
 [ 0.75 -0.25]]

Here, we have used the `linalg.inv()` function to calculate the inverse of the array1 matrix.

**Note**: Not all matrices are invertible and if you try to compute the inverse of a matrix having determinant zero `inv()` will raise the `LinAlgError` exception.

---

## NumPy trace() Function

In NumPy, we use the `trace()` function to compute the sum of the diagonal elements of a matrix. For example,

```
import numpy as np

# define a 3x3 matrix
array1 = np.array([[6, 3, 5], 
                   [9, 2, 1], 
                   [7, 8, 4]])

# compute the trace of the matrix
result = np.trace(array1)

print(result)

# Output: 12
```


In this example, the diagonal elements of the matrix are **6**, **2**, and **4**, so the sum of these elements is **12**. So, the `trace()` function returns this value as the output.
# NumPy Histogram

NumPy histograms is a graphical representation of the distribution of numerical data. Using functions like `histogram()` and `plt()`, we can create and plot histograms.

We'll take a closer look at histograms and how they can be created and plotted in NumPy.

---

## NumPy Histogram

NumPy has a built-in function `histogram()` that takes an array of data as a parameter.

In histogram, a bin is a range of values that represents a group of data. `bin` is an optional parameter.

Let's see an example.

```
import numpy as np

# create an array of data
data = np.array([5, 10, 15, 18, 20])

# create bin to set the interval
bin = [0,10,20,30]

# create histogram
graph = np.histogram(data, bin)

print(graph)
```
**Output**

(array([1, 3, 1]), array([ 0, 10, 20, 30]))

In this example, we have used the `histogram()` function to calculate the frequency distribution of data. We have passed two parameters: data and bin.

The `histogram()` function returns a tuple containing two arrays:

- the first array contains the frequency counts of the data within each bin, and
- the second array contains the bin edges.

From the resulting output, we can see that:

- Only **1** data point (i.e., **5**) from the array data lies between the bin edges **0** and **10**
- **3** data points (i.e., **10, 15, 18**) lie between **10** and **20**, and
- **1** data point (i.e., **20**) lies between **20** and **30**.

---

### Example: NumPy Histogram

```
import numpy as np

# create an array of data
data = np.array([1, 2, 3, 4, 5, 6, 7, 8, 1, 2, 3])

# create bin to set the interval
bin = [0, 5, 10]

# create histogram
graph = np.histogram(data, bin)

print(graph)
```
**Output**

(array([7, 4]), array([ 0,  5, 10]))

Here, the `histogram()` functions returns a tuple of arrays. Analyzing the output, **7** data points from the array data lie within the bin edges **0** and **5**, and **4** data points lie within **5** and **10**.

---

## Plot the Histogram

We can use the `plt()` function to plot the numerical value returned by the histogram.

The `plt()` is a function provided by Matplotlib. To use `plt()`, we need to import the Matplotlib.

Let's see an example.

```
import numpy as np
from matplotlib import pyplot as plt

# create an array of data
data = np.array([5, 10, 15, 18, 20])

# create bin to set the interval
bins = [0,10,20,30]

# create histogram
graph = np.histogram(data, bins)
print(graph)

# plot histogram 
plt.hist(data, bins)

plt.show()
```

**Output**

(array([1, 3, 1]), array([ 0, 10, 20, 30]))

Plotting a Histogram

In the above example, we used the `histogram()` function to calculate the frequency distribution of data and then plotted the resulting histogram using the `plt.hist()` function from the matplotlib library.

# NumPy Interpolation

In NumPy, interpolation estimates the value of a function at points where the value is not known.

Let's suppose we have two arrays: day representing the day of the week and gold_price representing the price of gold per gram.

```
day = np.array([2, 4, 7])
gold_price = np.array([55, 58, 65])
```

With the given data set, we can say the price of the gold on day 2 is 55. But we do not know the price of gold on day 3.

In such a case, we use interpolation to estimate the price of the gold at any day within the data points.

---

## NumPy Interpolation

NumPy provides an `interp()` function to work with interpolation. Let's see an example.

```
import numpy as np

day = np.array([2, 4, 7])
gold_price = np.array([55, 58, 65])

# find the value of gold on day 3
day3_value = np.interp(3, day, gold_price)

print("The value of gold on day 3 is", day3_value)
```


**Output**

The value of gold on day 3 is 56.5

Here, we used the `interp()` function to find the value of gold on day 3.

We have sent 3 arguments to the `interp()` function:

- **3**: coordinate whose value needs to be interpolated
- day: x-ordinate of the data points that represent days of the week
- gold_price: y-coordinates of the data points that represent the gold price

---

## Example: NumPy Interpolation

```
import numpy as np

day = np.array([2, 4, 7, 10])
gold_price = np.array([55, 58, 65, 70])

# days whose value is to be interpolated
interpolate_days = np.array([1, 3, 5, 6, 8, 9])

interpolated_price= np.interp(interpolate_days, day, gold_price)

print(interpolated_price)
```


**Output**

[55.   56.5   60.33333333   62.66666667   66.66666667   68.33333333]

In this example, we have used the `interp()` function to interpolate the values in the array interpolate_days.

The resulting array is the estimated price of gold on day 1, 3, 5, 6, 8, and 9.

---

## Graph the Interpolated Values

To plot the graph, we need to import the `pyplot` from the `matplotlib` module. Let's see an example.

```
import numpy as np
import matplotlib.pyplot as plt

# arrays with random data points
x = np.array([0, 1, 2, 3, 4, 5])
y = np.array([0, 3, 4, 5, 7, 8]) 

# generate evenly spaced values between the minimum and maximum x values
x_interp = np.linspace(x.min(), x.max(), 100)

# interp() to interpolate y values
y_interp = np.interp(x_interp, x, y)

# plot the original data points and the interpolated values
plt.plot(x, y, 'bo')
plt.plot(x_interp, y_interp, 'r-')

plt.show()
```

**Output**
Graph of Interpolated Values

In this example, we have plotted the graph of the interpolated values in y_interp.

First, we generated 100 evenly spaced values between the minimum and maximum of x using the `linspace()` function.

Then we used the `interp()` function to interpolate the y values and plotted the interpolated values using `plot()` function.
# NumPy Files

A file is a container in computer storage devices used for storing data.

In the context of NumPy, a file can be thought of as a container used for storing NumPy arrays in computer storage devices.

---

## Save Single NumPy Array File

In NumPy, we use the `save()` function to save a single NumPy array to a binary file in the `.npy` format.

Here's the syntax of the `save()` function.

```
np.save(file, array)
```

- `file` - specifies the file name (along with path if required)
- `array` - specifies the NumPy array to save

Now, let's see an example.

```
import numpy as np

array1 = np.array([[2, 4, 6], 
                  [8, 10, 12]])

# save the array to a file
np.save('file1.npy', array1)
```

Here, we saved the NumPy array array1 to the binary file `file1.npy` in our current directory.

**Note**: The .npy extension is automatically appended to the file name if it's not already present.

---

## Load Single NumPy Array File

In the previous example, we saved an array to a binary file. Now we'll load that saved file using the `load()` function.

Let's see an example.

```
import numpy as np

# load the saved NumPy array
loaded_array = np.load('file1.npy')

# display the loaded array
print(loaded_array)
```

**Output**

[[ 2  4  6]
 [ 8  10 12]]

Here, we have used the `load()` function to read a binary file `file1.npy`. This is the same file we created and saved using `save()` function in the last example.

---

## Save Multiple NumPy Array File

To save multiple NumPy arrays into a single file we use the `savez()` function.

The `savez()` function is similar to the `save()` function, but it can save multiple arrays at once in the `.npz` format.

Here's the syntax of the `savez()` function.

```
np.savez(file, *args, **kwds)
```

- `file` - name of the file where the arrays will be saved
- `*args` - list of arrays to be saved (comma-separated)
-
Now, let's see an example.

```
import numpy as np

# create two NumPy arrays
array1 = np.array([2, 6, 10])
array2 = np.array([4, 8, 12])

# save the two arrays into a single file
np.savez('file2.npz', file1 = array1, file2 = array2)
```

In this example, we have used the `np.savez()` function to save the two NumPy arrays array1 and array2 into a single file named `file2.npz`.

The `file1` and `file2` are the names given to the arrays using keyword arguments.

**Note**: We can `savez_compressed()` to save multiple arrays in a compressed file format. This function is similar to `savez()` but uses compression to reduce the size of the saved file.

---

## Load Multiple NumPy Array File

In the previous example, we saved multiple arrays to a single file. Now we'll load that saved file using the `load()` function.

```
import numpy as np

# load the saved arrays 
load_data = np.load('file2.npz')

# retrieve the arrays using their names
array1 = load_data['file1']
array2 = load_data['file2']

# display the loaded arrays
print(array1)
print(array2)
```

**Output**

[ 2  6 10]
[ 4  8 12]

In the above example, first we loaded the saved arrays from the file using the `np.load()` function.

Then, we retrieved the arrays using their names `file1` and `file2` (mentioned in the previous example) as: `data['file1']` and `data['file2']`, respectively.

Finally, we displayed the loaded arrays.
# Numpy Error Handling

An error or exception is an unexpected event that occurs during program execution. It affects the flow of the program instructions which can terminate the program abnormally.

Responding or handling exceptions is called **Exception Handling.**

NumPy provides various ways to handle exceptions that occur during array operations.

---

## Handle Floating-Point Errors in NumPy

In NumPy, the `seterr()` function sets the way floating-point errors are handled.

It takes several parameters:

1. `divide`: specifies the behavior for division by zero or infinity
2. `over`: specifies the behavior for floating-point overflow
3. `under`: specifies the behavior for floating-point underflow
4. `invalid`: specifies the behavior for invalid floating-point operations such as **0/0**, **inf-inf**, and **sqrt(-1)**

**Note**: Possible values of all these parameters are `"ignore"`, `"warn"`, `"raise"`, or `"call"`. The default behavior for all types of errors is `"warn"`.

---

### Example 1: NumPy seterr() Function

```
import numpy as np

# set behavior for division by zero to 'raise'
np.seterr(divide='raise')

# divide array1 by array2
array1 = np.array([1, 2, 3])
array2 = np.array([0, 2, 0])
result = np.divide(array1, array2)

print(result)
```
**Output**

FloatingPointError: divide by zero encountered in true_divide

In this example, we have set the behavior for division by zero errors to `raise` using `np.seterr(divide='raise')`.

This means when `np.divide()` encounters division by zero during the calculation, it will raise the `FloatingPointError` error.

If we had set the behavior for division by zero to

- `divide='ignore'` - it doesn't raise an error or print a warning message and the output would be `[inf 1. inf]`
- `divide='warn'` - it prints a warning message and also runs the program and the output would be `[inf 1. inf]`

---

### Example 2: The over Parameter in NumPy seterr() Function

```
import numpy as np

# set behavior for floating-point overflow to 'raise'
np.seterr(over='raise')

calc1 = np.exp(1000)

print(calc1)
```
**Output**

FloatingPointError: overflow encountered in exp

In the above example, we set the behavior for floating-point overflow to `raise`.

We then calculated `np.exp(1000)`, which results in a floating-point overflow because the result of the calculation is too large to be represented by the floating-point data type.

This raises an exception: `FloatingPointError: overflow encountered in exp`.

**Note**: If we set `np.seterr(under='raise')` and calculate `np.exp(-1000)`, this raises an exception: `FloatingPointError: underflow encountered in exp`.

---

### Example 3: The invalid Parameter in NumPy seterr() Function

In Numpy, we can use the `invalid` parameter in `seterr()` to raise an exception when an invalid floating-point operation occurs. For example,

```
import numpy as np

# set the invalid parameter to 'raise'
np.seterr(invalid='raise')

# try taking the square root of a negative number
x = np.sqrt(-1)

# Output: FloatingPointError: invalid value encountered in sqrt
```


Here, we attempted to take the square root of **-1**, which is an invalid floating-point operation.

As we have set the `invalid='raise'`, NumPy will raise a `FloatingPointError`.

---

## NumPy try-catch Block

We can use the `try...except` block in NumPy to handle an error. Here's the syntax of `try...except`:

```
try:
    # code that may cause exception
except:
    # code to run when exception occurs
```

Here, we have placed the code that could potentially raise an exception within the `try` block. When an exception occurs in the `try` block, it's caught by the `except` block.

The `try` and `except` block must work together to handle the exception.

Let's see an example.

```
import numpy as np

array1 = np.array([1, 4, 3])
array2 = np.array([0, 2, 0])

# try to divide the arrays
try:
    result = array1/array2

except ZeroDivisionError as e:
    print("Error: Cannot divide by zero")
```
**Output**

runtimewarning: divide by zero encountered in divide
# NumPy Date and Time

NumPy provides functionality for working with dates and times.

The `datetime64()` function in Numpy stores date and time information as a 64-bit integer `datetime64` object.

---

### Example 1: Get Current Date and Time in NumPy

```
import numpy as np

# get the current date and time 
result = np.datetime64('now')

print("Current date and time:")
print(result)
```
Current date and time:
2023-04-29T04:00:05

In this example, we have used the `datetime64()` function with the `now` argument to get the current date and time.

The output above indicates that the current date and time is **April 29th, 2023**, at **4:00:05 AM**.

---

### Example 2: Get Current Date in NumPy

```
import numpy as np

# get the current date
date_today = np.datetime64('today', 'D')

print("Today's date:")
print(date_today)
```
**Output**

Today's date:
2023-04-29

Here, we have used the `datetime64()` function with the `today` and `D` argument to get the current date.

- The `today` argument specifies the current date.
- The `D` argument specifies resolution of one day.

---

### Example 3: Use datetime64() For Different Time Units

```
import numpy as np

# use datetime64() for different time units
year = np.datetime64('2023', 'Y')
month = np.datetime64('2023-04', 'M')
day = np.datetime64('2023-04-29', 'D')
hour = np.datetime64('2023-04-29T10', 'h')
minute = np.datetime64('2023-04-29T10:30', 'm')
second = np.datetime64('2023-04-29T10:30:15', 's')

print("Year: ", year)
print("Month: ", month)
print("Day: ", day)
print("Hour: ", hour)
print("Minute: ", minute)
print("Second: ", second)
```
**Output**

Year:  2023
Month:  2023-04
Day:  2023-04-29
Hour:  2023-04-29T10
Minute:  2023-04-29T10:30
Second:  2023-04-29T10:30:15

In the above example, we have used the `datetime64()` to create the `datetime64` objects for different time units.

**Note**: Even though it is not strictly necessary to specify the time unit, it's a good practice to specify them while creating the `datetime64` objects.

---

## Convert datetime64 Objects

In NumPy, it is possible to convert `datetime64` objects to and from other data types.

### 1. Convert datetime64 to Python datetime Object
 For example,

```
import numpy as np
from datetime import datetime

# create a datetime64 object
dt64 = np.datetime64('2023-04-29T12:34:56')

# convert datetime64 to datetime object
dt = dt64.astype(datetime)

# print the datetime object
print(dt)
```
**Output**

2023-04-29 12:34:56

### 2. Convert Python datetime Object to datetime64

Here's how we can convert Python's `datetime` object to the `datetime64` object:

```
import numpy as np
from datetime import datetime

# create a datetime object
dt = datetime(2023, 4, 29, 12, 34, 56)

# convert datetime to datetime64 object
dt64 = np.datetime64(dt)

# print the datetime64 object
print(dt64)
```



**Output**

2023-04-29T12:34:56

---

## Create a Range of Dates

In NumPy, we use the `arange()` function to create a range of dates. For example,

```
import numpy as np

# create a range of dates from 2023-04-01 to 2023-04-10
dates = np.arange('2023-04-01', '2023-04-11', dtype='datetime64[D]')

# print the dates
print(dates)
```
**Output**

['2023-04-01' '2023-04-02' '2023-04-03' '2023-04-04' '2023-04-05'
 '2023-04-06' '2023-04-07' '2023-04-08' '2023-04-09' '2023-04-10']

In this example, we have used the `arrange()` function to create a range of dates from April 1st, 2023 to April 10th, 2023.

Here, `dtype='datetime64[D]'` indicates that each date in the range should have a resolution of one day.

---

## Arithmetic Operations on NumPy datetime64 Objects

We can perform arithmetic operations like addition, subtraction on NumPy's `datetime64` objects.

Let's see an example.

```
import numpy as np

# create a datetime64 object for today
today = np.datetime64('today')

# add one day to today's date
tomorrow = today + np.timedelta64(1, 'D')

# create datetime64 objects for two dates
date1 = np.datetime64('2023-05-01')
date2 = np.datetime64('2023-04-01')

# calculate the number of days between the two dates
num_days = date1 - date2

# display the results
print("Today's date:", today)
print("Tomorrow's date:", tomorrow)
print("Number of days between", date1, "and", date2, "is", num_days)
```



**Output**

Today's date: 2023-04-29
Tomorrow's date: 2023-04-30
Number of days between 2023-05-01 and 2023-04-01 is 30 days

In the above example, we have used `np.datetime64('today')` to create the `datetime64` object for today's date.

Then we added one day to today's date using `today + np.timedelta64(1, 'D')` to get tomorrow's date.

Notice the code,

```
date1 - date2
```

Here, we have performed an arithmetic subtraction operation to calculate the number of days between the two dates.

**Note**: `timedelta()` is a Python function that is part of the `datetime` module. 

---

## NumPy busday() Function

In NumPy, the `np.busday()` function is used to calculate the number of business days (i.e., weekdays excluding holidays) between two dates.

Let's see an example.

```
import numpy as np

# create datetime64 objects for two dates
date1 = np.datetime64('2023-04-01')
date2 = np.datetime64('2023-05-01')

# calculate the number of business days between the two dates
num_business_days = np.busday_count(date1, date2)

# display the number of business days between the two dates
print("Number of business days between", date1, "and", date2, "is", num_business_days)
```



**Output**

Number of business days between 2023-04-01 and 2023-05-01 is 20

Here, we have used `np.busday_count()` to calculate the number of business days between date1 and date2.
# NumPy Data Visualization

NumPy provides several techniques for data visualization like line plots, scatter plots, bar graphs, and histograms.

Data visualization allows us to have a visual representation of large amounts of data quickly and efficiently.

Let's learn about visualization techniques in NumPy.

---

## Dataset For Data Visualization

We'll be using the dataset of cars to visualize data.

|Car|Weight|
|---|---|
|Caterham|0.48 tons|
|Tesla|1.7 tons|
|Audi|2 tons|
|BMW|2 tons|
|Ford|2.5 tons|
|Jeep|3 tons|

---

## Line Plot For Data Visualization

In Numpy, line plot displays data as a series of points connected by a line. It has a `plot()` function to line plot the data, which takes two arguments; x and y coordinate.

Let's see an example.

```
import numpy as np
import matplotlib.pyplot as plt

car = np.array(["Caterham", "Tesla", "Audi",  "BMW", "Ford", "Jeep"])
weight = np.array([0.48, 1.7, 2, 2, 2.3, 3 ])

plt.plot(car, weight)
plt.show()
```

**Output**

Here, we have used the `plot()` function to line plot the given dataset. We set the `x` and `y` coordinate of `plot()` as the car and weight arrays.

---

## Scatter Plots For Data Visualization

Scatter Plot displays data as a collection of points. It has a `scatter()` function to plot the data points. For example,

```
import numpy as np
import matplotlib.pyplot as plt

car = np.array(["Caterham", "Tesla", "Audi",  "BMW", "Ford", "Jeep"])
weight = np.array([0.48, 1.7, 2, 2, 2.3, 3 ])

plt.scatter(car, weight)
plt.show()
```

**Output**


In this example, we used `scatter()` function to plot the given data points. We sent two arguments car and weight as its x and y coordinates.

However, in a scatter plot, we can also send `c` and `s` arguments to set the color and sizes of the points. For example,

```
import numpy as np
import matplotlib.pyplot as plt

car = np.array(["Caterham", "Tesla", "Audi",  "BMW", "Ford", "Jeep"])
weight = np.array([0.48, 1.7, 2, 2, 2.3, 3 ])

# set colors and sizes
colors = np.array([0, 1, 2, 3, 4, 5])
sizes = np.array([20, 40, 60, 80, 100, 120])

plt.scatter(car, weight, c=colors, s=sizes)
plt.show()
```
---

## Bar Graphs For Data Visualization

Bar Graphs represent data using rectangular boxes. Numpy has a `bar()` function to plot data in a bar graph.

Let's see an example.

```
import matplotlib.pyplot as plt
import numpy as np

car = np.array(["Caterham", "Tesla", "Audi",  "BMW", "Ford", "Jeep"])
weight = np.array([0.48, 1.7, 2, 2, 2.3, 3 ])

# create a bar graph
plt.bar(car, weight)

plt.title('Bar Graph')

plt.show()
```

**Output**

Here, we have used the `bar()` function to plot the bar graph and passed two arrays car and weight as its argument.

---

## Histograms For Data Visualization

We use `hist()` to create histograms in NumPy. Let's see an example.

```
import numpy as np
import matplotlib.pyplot as plt

weight = np.array([0.48, 1.7, 2, 3])

plt.hist(weight)
plt.show()
```



## NumPy Universal Functions

The universal functions in NumPy include

- Trigonometric functions like `sin()`, `cos()`, and `tan()`

- Arithmetic functions like `add()`, `subtract()`, and `multiply()`

- Rounding functions like `floor()`, `ceil()` and `around()`

- Aggregation functions like `mean()`, `min()`, and `max()`.

Let's see some examples.

### Example: Trigonometric Functions

```
import numpy as np

# array of angles in radians
angles = np.array([0, 1, 2])
print("Angles:", angles)

# compute the sine of the angles
sine_values = np.sin(angles)
print("Sine values:", sine_values)

# compute the inverse sine of the angles
inverse_sine = np.arcsin(angles)
print("Inverse Sine values:", inverse_sine)
```



**Output**

Angles: [0 1 2]
Sine values: [0.         0.84147098 0.90929743]
Inverse Sine values: [0.         1.57079633        nan]

In this example, we have used universal functions `sin()` and `arcsin()` to compute the sine and inverse sine values respectively.

When we perform the `sin()` function to the array angles, an element-wise operation is performed to entire elements of the array. This is called vectorization.

---

### Example: Arithmetic Functions

```
import numpy as np

first_array = np.array([1, 3, 5, 7])
second_array = np.array([2, 4, 6, 8])

# using the add() function
result2 = np.add(first_array, second_array)
print("Using the add() function:",result2) 
```


**Output**

Using the add() function: [ 3  7 11 15]

Here, we used the universal function `add()` to add two arrays, first_array and second_array.

---

### Example: Rounding Functions

```
import numpy as np

numbers = np.array([1.23456, 2.34567, 3.45678, 4.56789])

# round the array to two decimal places
rounded_array = np.round(numbers, 2)

print("Array after round():", rounded_array)
```



**Output**

Array after round(): [1.23 2.35 3.46 4.57]

Here, we used the universal function `round()` to round the values of array numbers.


---

### Example: Statistical Functions

```
import numpy as np

array1 = np.array([1, 2, 3, 4, 5])

# calculate the median
median = np.median(array1)
print("Median is:",median)

# find the largest element
max = np.max(array1)
print("Largest element is", max)
```
**Output**

Median is: 3.0
Largest element is 5

In this example, we have used the universal functions `median()` and `max()` to find the median and largest element of array1.