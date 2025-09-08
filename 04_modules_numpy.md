# NUMPY
- numerical python library
- library - collection of predefined functions and adules to perform some operations
- every library has it's own purpose to use

# IMPORTING NUMPY
import numpy as np

# SOME FUNCTIONS
- np.sqrt(36)  -> 6
- np.log10(100) -> 2.0
- np.log2(100) -> 6.64
- np.sin(90) -> 0.89
- np.tan(90)  ->-1.99
- print(np.max([45,5,6,4,5,4,5]))  -> 45
- print(np.min([45,5,6,4,5,4,5]))  -> 4

  # DIFFERENCE BETWEEN LIST AND ARRAY
  - list -> contains element of different datatype
  - arrays -> contains element of same datatype

  # CRUD OPERATIONS
  - creating a array -> A=np.array([3,4,2,5,6])
  - creating a dimensional array -> zero=np.array(6)   zero
  - to know number of rows and coluns -> zero.shape  //you must think zero should have (1,1) shape but as long as we dont put 6 in []...it is considered empty
  - to check dimension of array  -> zero.ndim

  # CREATING 1-D ARRAY
  - one=np.array([6,5,4,3,5,3,4])
 
  # CREATING 2-D ARRAY
  - two=np.array([[6,5,4,3,4,5,3,4],[6,5,4,3,4,5,3,4]])
 
  # CONVERSION FROM LIST TO ARRAY
  li=[4,5,3,32,23]
  np.array(li)

  li=[3,"hrell",6.65,True,5,3,3,2]
  np.array(li)  ->  we know array has same datatype elemnts so converts all the elements to string type

  # CREATING ARRAYS WITH SOME BUILT IN FUNCTIONS
  - np.zeros((3,6)) -> create an array of zeroes with 3 rows and 6 columns
  - np.ones((3,6))  -> create an array of ones with 3 rows and 6 columns
  - np.ones((4,4))*5 -> output will be array of 5 element
 
  # CREATING RANDOM ARRAYS
  - np.random.randint(low=1,high=9,size=100)  -> will create random array of numbers from low to high having size 100
  - np.random.randint(1,9,size=(3,3)) -> you can write it without writig size

  # CREATING ARRAY WITH SOME SEQUENCE
  - use arange()
  - np.arange(1,10,2) -> 1 , 10 is the range and 2 means skip

  # CHANGING THE SHAPE OF MATRIX
  - A=np.arange(1,10)
    print(A)
    A.shape  -> [1 2 3 4 5 6 7 8 9]
                (9,)

    now if we do
    A.reshape(9) -> array([1, 2, 3, 4, 5, 6, 7, 8, 9])

    # SEQUENCE WITH EQUAL GAPS
    - np.linspace(1,10,10)
   
    # SLICING IN 2D ARRAYS
    - A2=np.random.randint(1,9,size=(3,3))
      A2
      print(A2[1:3,1:3])  ->  [[7 6]
                               [1 3]]
      print(A2[1:,1:])    -> [[7 6]
                              [1 3]]

    # UPDATING THE ARRAYS
    new_A[3,3]=500
    new_A

    # DELETING THE ARRAYS
    A1=np.random.randint(1,9,size=(10))
    A1=np.delete(A1,4)
    A1

    # FLATTEN FUNCTION
    - removed dimension of arrays and make it 1D
    - A.flatten()
    - In delete function the flatening will be done automatically if we tries to delete any specific index values
    - np.delete(A2,2,axis=0)  # To remove the rows use axis=0
    - np.delete(A2,2,axis=1)  # To remove the column use axis=1
   
    # MATRIX
    - Creating Matrix
      m=np.array([[1,2,3],[4,5,6],[7,8,9]])
      m  -> array([[1, 2, 3],
       [4, 5, 6],
       [7, 8, 9]])

    - Scaler operations -> m+2 , m-2 , m/2 , m*2
   
    - Matrix to matrix operations can be done
      #condition that the shape of both the matrix should be same
      m1=np.random.randint(1,10,(3,3))
      m2=np.random.randint(1,10,(3,3))

    # VECTOR
    - Creating vector 
      v1=np.array([1,2,3])
      v2=np.array([4,5,6])

    - dot product
      #condition - vectors that no of column of first vector should be equal to no of rows of second
      np.dot(v1,v2)

    - cross product
      np.cross(v1,v2)

   # For advanced linear algebra concepts we have to import functions from linalg module of numpy
    - determinant
      A=np.random.randint(1,5,(3,3))
      A
      np.linalg.det(A)

    - transpose
      np.transpose(A)  or A.T

    - inverse
      np.linalg.inv(A)

    - eigen value , eigner vector
      eig_val,eig_vector=np.linalg.eig(A)

  

    
    
      
