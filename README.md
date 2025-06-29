# numpy_notes

Comprehensive notes on NumPy, including attributes, functions, datatypes, operators, mathematical operations, statistical operations, and more.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Array Creation](#array-creation)
- [Array Attributes](#array-attributes)
- [Datatypes](#datatypes)
- [Indexing & Slicing](#indexing--slicing)
- [Operators](#operators)
- [Mathematical Operations](#mathematical-operations)
- [Statistical Operations](#statistical-operations)
- [Broadcasting](#broadcasting)
- [Reshaping & Manipulation](#reshaping--manipulation)
- [Aggregation Functions](#aggregation-functions)
- [Random Module](#random-module)
- [Linear Algebra](#linear-algebra)
- [Saving & Loading Arrays](#saving--loading-arrays)
- [Useful Functions](#useful-functions)
- [References](#references)

---

## Introduction

NumPy is the fundamental package for scientific computing with Python. It provides support for large, multi-dimensional arrays and matrices, along with a collection of mathematical functions.

## Installation

```sh
pip install numpy
```

## Array Creation

- `np.array()`
- `np.zeros()`
- `np.ones()`
- `np.arange()`
- `np.linspace()`
- `np.eye()`
- `np.full()`
- `np.random.rand()`, `np.random.randn()`, `np.random.randint()`

## Array Attributes

- `ndim` (number of dimensions)
- `shape` (dimensions of array)
- `size` (total number of elements)
- `dtype` (data type)
- `itemsize` (size of each element in bytes)

## Datatypes

- `int32`, `int64`, `float32`, `float64`, `complex`, `bool`, etc.

## Indexing & Slicing

- 1D, 2D, 3D indexing
- Slicing arrays
- Boolean indexing
- Fancy indexing

## Operators

- Arithmetic: `+`, `-`, `*`, `/`, `//`, `%`, `**`
- Comparison: `>`, `<`, `==`, `!=`, `>=`, `<=`
- Logical: `np.logical_and`, `np.logical_or`, `np.logical_not`

## Mathematical Operations

- `np.add()`, `np.subtract()`, `np.multiply()`, `np.divide()`
- `np.power()`, `np.sqrt()`
- Trigonometric: `np.sin()`, `np.cos()`, `np.tan()`
- Exponential & Logarithmic: `np.exp()`, `np.log()`

## Statistical Operations

- `np.mean()`, `np.median()`, `np.std()`, `np.var()`
- `np.min()`, `np.max()`, `np.sum()`, `np.prod()`
- `np.percentile()`, `np.quantile()`
- `np.argmin()`, `np.argmax()`

## Broadcasting

- Operations on arrays of different shapes

## Reshaping & Manipulation

- `np.reshape()`
- `np.ravel()`, `np.flatten()`
- `np.transpose()`
- `np.concatenate()`, `np.vstack()`, `np.hstack()`
- `np.split()`, `np.array_split()`

## Aggregation Functions

- `np.sum()`, `np.mean()`, `np.cumsum()`, `np.cumprod()`

## Random Module

- `np.random.seed()`
- `np.random.rand()`, `np.random.randn()`, `np.random.randint()`
- `np.random.shuffle()`, `np.random.permutation()`

## Linear Algebra

- `np.dot()`, `np.matmul()`
- `np.linalg.inv()`, `np.linalg.det()`
- `np.linalg.eig()`, `np.linalg.svd()`

## Saving & Loading Arrays

- `np.save()`, `np.load()`
- `np.savetxt()`, `np.loadtxt()`

## Useful Functions

- `np.where()`
- `np.unique()`
- `np.sort()`
- `np.clip()`

## References

- [NumPy Documentation](https://numpy.org/doc/)# numpy_notes
numpy notes like attributes,functions,datatype,operators ,mathematical operations,statistical operations and many more
