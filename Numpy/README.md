Introduction to NumPy and its functions
----------------------------------------
NumPy is the fundamental package for scientific computing with python.It contains among other things
.a powerful n-dimensional array object
.sophisticated(broadcasting) functtions
.tools for integrating C/C++ and Fortran code.
.useful linear algebra, fourier transform and random number capabilities

NumPy can also be used as an efficient multi-dimensional container of generic data.
Arbitrary data-types can be defined.This allows NumPy to seamlessly and speedly integrate with a variety of databases.
Array can either be a vector or matrix
import numpy as np

np.array function convert list to array
np.arange function to create range of values starting from particular point until to the upper limit
np.zeros(100)
np.ones(100)
np.linespace(0,20,10) returns evenly spaced numbers
np.eye returns 2-D array with ones on the diagonal and zero elsewhere also called identity matrix
np.random.rand(3,2) creates uniform distribution of values between o and 1(0 inclusive), rand uses
random logic on a uniform distribution of values
np.random.randn(3,2) - randn uses logic of randomness on a normally distributed set of values.
np.random.randint(5,20) -creates set of random integers between low and high specified 
np.random.randint(5,20,10)- creates 10 random integers
sample_array.reshape(5,6)
sample_arry.shape
sample_array.dtype
Transposing a matrix
a = np.eye(5)
a.T

How to select  group of objects from a particular array

Indexing a matrix

Selection techniques
--------------------
universal array functions -squareroot, exponential, mean
np.sqrt(sample_array)
np.exp(sample_array)
np.max(sample_array)
np.min(sample_array)
np.argmin(sample_array)
np.argmax(sample_array)
np.sin(sample_array)
np.cos(sample_array)
np.tan(sample_array)
np.square(sample_array)
array = np.random.randn(6,6)
np.round(array)
np.round(array, decimals = 2)
np.std(sample_array)
np.mean(array)
sports = np.array(['golf','cric','football','cric','Cric','fooseball'])
np.unique(sports)



Input and Output options saving files
-------------------------------------
np.save('sample_array', sample_array) - it wil save in the disk(working directory)

np.savez('2_arrays.npz', a = sample_array b = simple_array) -archived repository which stores more than one array

How to load the files that has been saved
np.load('sample_array.npy')

np.savetxt('text_file.txt', sample_array)- will save the array in text file
np.savetxt('text_file1.txt', sample_array, delimiter=',')

To load text file
np.loadtxt('text_file.txt')