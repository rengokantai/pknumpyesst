#### pknumpyesst
#####2 The numpy ndarray object
same object
```
x= np.random.rand(10,10)  //only positive
y=x[:5,:]
np.may_share_memory(x,y) #True
```

create a seperate object
```
x = np.random.randn(10,10)   // positive and negative
y = np.empty([5,10])
y[:]=x[:5,:]
np.may_share_memory(x,y) #False 
```

######creating arrays
```
x = np.random.randint(low,high,size=10)
```
##### 3 Using numpy array
```
x=np.arange(5,10)  # 5-9
np.square(x)
```
minimum and min
```
np.minimum(x,7) # (5,6,7,7,7)
np.min(x)  # 7
```
repeat
```
z=np.repeat(x,3)  //([[5,5,5],[6,6,6],..)
np.median(z,axis=0)
```
outer
```
>>> x
array([5, 6, 7, 8, 9])
>>> np.multiply.outer(x,x)
array([[25, 30, 35, 40, 45],
       [30, 36, 42, 48, 54],
       [35, 42, 49, 56, 63],
       [40, 48, 56, 64, 72],
       [45, 54, 63, 72, 81]])
```
######Broadcasting and shape manipulation
```
>>> x = np.array([[0,0,0],[10,10,10]])
>>> y = np.array([1,2,3])
>>> x + y
array([[ 1,  2,  3],
       [11, 12, 13]])
```
1*3 + 3*1
```
>>> x = np.array([[0],[10],[20]])
>>> x+y
array([[ 1,  2,  3],
       [11, 12, 13],
       [21, 22, 23]])
```
resize
```
x = np.arange(3)
np.resize(x,(8,))  #[0,1,2,0,1,2,0,1]
```
hstack, vstack dstack
######A boolean mask
```
x = np.array([1,2,3,-1)]
mask = (x<0)
mask  #array([False,False,False,True])
```
set value
```
x[mask]=0
x  # array([1,2,3,0])
```
######help utility
```
help(), dir(),
np.lookfor('resize')
```
#####4 Numpy Core
#####5 Linear Algebra
######The matrix class
```
ndarray = np.arange(9).reshape(3,3)
x = np.matrix(ndarray)
y = np.mat(np.identity(3))  #mat is same as numpy.matrix(data,copy=False)
```
