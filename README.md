# **Understanding NumPy Library**
## Introduction

NumPy (Numerical Python) is a core library for scientific computing in Python. It provides a high-performance multidimensional array object and tools for working with these arrays. It is the foundation for many other scientific computing libraries such as SciPy, Pandas, and Matplotlib.
1. **Why NumPy over Python :**
   
   Using NumPy over plain Python offers several advantages:
   · Performance: NumPy is faster due to its implementation in C.

   · Memory Efficiency: NumPy arrays consume less memory than Python lists.

   · Convenience: Provides extensive functionality for mathematical, logical, shape manipulation, sorting, selecting, I/O, and more.

   · Interoperability: Compatible with other scientific libraries like SciPy, Pandas, and TensorFlow.
   

2. **Different Functions in NumPy :**

   NumPy provides a wide array of functions:

   · Array Creation: `np.array(), np.zeros(), np.ones(), np.empty(), np.arange(), np.linspace()`

   · Mathematical Operations: `np.add(), np.subtract(), np.multiply(), np.divide(), np.dot(), np.sqrt()`

   · Statistical Operations: `np.mean(), np.median(), np.std(), np.var()`

   · Random Number Generation: `np.random.rand(), np.random.randn(), np.random.randint()`

3. **Properties of ndarrays :**

   · *Shape:* The dimensions of the array.

       arr = np.array([[1, 2, 3], [4, 5, 6]])

       print(arr.shape) # (2, 3)
   

     *Size:* The total number of elements in the array.

       print(arr.size) # 6

   · *Data Type:* The type of elements stored in the array.

        print(arr.dtype) # dtype('int64')

4. **NumPy Data Types :**

   NumPy supports a variety of data types:

   · Integer types: `np.int8, np.int16, np.int32, np.int64`

   · Unsigned integer types: `np.uint8, np.uint16, np.uint32, np.uint64`

   · Floating-point types: `np.float16, np.float32, np.float64`

   · Complex types: `np.complex64, np.complex128`

   · Boolean type: `np.bool_`

   · Object type: `np.object_`

5. **Different Arithmetic Operations :**

   · Element-wise Operations:

         arr1 = np.array([1, 2, 3])

         arr2 = np.array([4, 5, 6])

         print(arr1 + arr2) # [5 7 9]

         print(arr1 * arr2) # [4 10 18]

   · Dot Product:

         print(np.dot(arr1, arr2)) # 32

   · Square root and Exponential :

         print(np.sqrt(arr1)) # [1. 1.41421356 1.73205081]

         print(np.exp(arr1)) # [ 2.71828183 7.3890561 20.08553692]

6. **Indexing and Slicing for 2D and 3D Arrays :**

   · 2D Array:

         arr = np.array([[1, 2, 3], [4, 5, 6]])

         print(arr[0, 1]) # 2

         print(arr[:, 1]) # [2 5]

   · 3D Array:

         arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

         print(arr[0, 1, 1]) # 4

         print(arr[:, 1, :]) # [[3 4] [7 8]]

7. **Transposing Arrays :**

   Transpose changes the axes of the array.



         arr = np.array([[1, 2, 3], [4, 5, 6]])

         print(arr.T) # [[1 4]

                   # [2 5]

                   # [3 6]]

8. **Swapping Arrays :**

   Swap two axes of an array.

        arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

        print(np.swapaxes(arr, 0, 1)) # [[[1 2] [5 6]]

                                      # [[3 4] [7 8]]]

9. **Pseudo Random Arrays :**

   Generate arrays with random numbers.

        random_arr = np.random.rand(2, 3) # 2x3 array of random floats between 0 and 1

        random_int_arr = np.random.randint(0, 10, (2, 3)) # 2x3 array of random integers between 0

10. **Masking in Arrays :**

   Masking is useful for filtering elements.

    arr = np.array([1, 2, 3, 4, 5])

    mask = arr > 3

    print(arr[mask]) # [4 5]

12. **Universal Functions :**

   · Arithmetic Functions: `np.add(), np.subtract(), np.multiply(), np.divide()`

   · Trigonometric Functions: `np.sin(), np.cos(), np.tan()`

   · Exponential and Logarithmic Functions: `np.exp(), np.log(), np.log10()`

   · Statistical Functions: `np.mean(), np.median(), np.std(), np.var()`

   · Comparison Functions: `np.greater(), np.less(), np.equal(), np.not_equal()`

   · Broadcasting: Allows operations on arrays of different shapes.


      arr = np.array([1, 2, 3])

      scalar = 2

      print(arr + scalar) # [3 4 5]

13. **Playing with Shapes :**

   · Reshape:

    arr = np.array([[1, 2, 3], [4, 5, 6]])

    reshaped_arr = arr.reshape((3, 2))

   · Resize:

    arr.resize((3, 2))

   · Ravel and Flatten:

    print(arr.ravel()) # [1 2 3 4 5 6]

    print(arr.flatten()) # [1 2 3 4 5 6]

   · Squeeze and Expand_dims:

    arr = np.array([[[1, 2, 3]]])

    print(arr.squeeze()) # [1 2 3]

    print(np.expand_dims(arr, axis=0).shape) # (1, 1, 1, 3)

14. **Splitting and Joining Arrays :**

   · Splitting:

    arr = np.array([1, 2, 3, 4, 5, 6])

    split_arr = np.split(arr, 3) # [array([1, 2]), array([3, 4]), array([5, 6])]

   · Joining:

    arr1 = np.array([1, 2])

    arr2 = np.array([3, 4])

    print(np.concatenate((arr1, arr2))) # [1 2 3 4]

15. **Basic Information on Arrays :**

   · Creation:

    arr = np.array([1, 2, 3])

   · Attributes: shape, size, dtype

   · Methods: `reshape(), flatten(), ravel(), transpose()`
