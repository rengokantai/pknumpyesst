#### pknumpyesst
#####2 The numpy ndarray object
same object
```
x= np.random.rand(10,10)
y=x[:5,:]
np.may_share_memory(x,y) #True
```

create a seperate object
```
x = np.random.randn(10,10)
y = np.empty([5,10])
y[:]=x[:5,:]
np.may_share_memory(x,y) #False 
```
