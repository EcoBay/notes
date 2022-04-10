# Array

An array is a contiguous collections of multiple variables of the same data type. In most programming language array are referenced type meaning that mutation can be done to the array passed to a function. Elements of array can be access using an index or subscript which is typically zero-based, meaning it start from zero.

## Dimensions of array

Dimensions of array specify how many index you need to access and elements. So for single dimension array, which is the most common requires only one index to access, while for 2D array which is also common for matrix or spatial data requires 2 index, usually for denoted as row and column index, to access its elements. Higher dimensions arrays are also possible like 3D, 4D, and so on but are rarely used. The dimensions of array are sometimes limited for example [C#](c-sharp.md) which only support up to 32D array.

```c#
int[] = new int[5];     // A 1D array of 5 ints
int[,] = new int[5,5];  // A 2D array of 5x5 ints
```

Multidimensional array are typically stored in row-major order, meaning elements with lower level first index are stored first. So it is good practice to access ND array with it last index first as they are closer together in memory and can benefit to caching.

Another way to store a 2D array is by using an 'array of array' wherein an array contains pointer to an array. This offers more flexibility allowing for jagged array or a ND array with variable lengths. At the expense of some performance as they are not stored in a single block of memory.

```c#
int[][] jagged_array = new int[3][];
jagged_array[0] = new int[1] {1};
jagged_array[2] = new int[2] {3,4};
jagged_array[3] = new int[3] {5,6,7};
```
