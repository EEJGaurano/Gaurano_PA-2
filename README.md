Normalization Problem 
``` python
import numpy as np #Import numerical python Library

X = np. random. rand(5, 5) #Create random 5x5 array

Z = (X - X.mean()) /X.std() #Function for Normalized Values

np. save("X_normalized.npy", Z) #save Normalized values as X_nomatized. ny

print ("Original Value: \n", X, "\n Normalized Value: \n", Z) #Print X and Z
#end

Original Value: 
 [[0.55009258 0.24130825 0.21725547 0.45176506 0.48020317]
 [0.72545317 0.76488057 0.95996251 0.4206211  0.88139489]
 [0.65358639 0.84128453 0.73721841 0.17541719 0.82836089]
 [0.88774418 0.12989297 0.05398463 0.93952104 0.48383686]
 [0.50673001 0.08642024 0.46358467 0.91763411 0.97377561]] 
 Normalized Value: 
 [[-0.08438219 -1.1356777  -1.21756843 -0.41915071 -0.32232957]
 [ 0.51265523  0.64689084  1.31107208 -0.52518429  1.04357865]
 [ 0.26797564  0.90701783  0.55271148 -1.36001217  0.86301764]
 [ 1.06519559 -1.51500517 -1.77344477  1.24147652 -0.30995821]
 [-0.23201557 -1.66301359 -0.37890936  1.16695966  1.35810054]]
```

Divisible by 3 Problem
``` python
import numpy as np


n = np.arange(1,101) #Create an array of the first 100 positive integers


A_squared = np.square(n) #Square every element

A = A_squared.reshape(10,10) #Resize into a 10x10 ndarray

Div_by_3 = A[A % 3 == 0] #Determine the elements divisible by 3

np.save('div_by_3.npy', Div_by_3) #Save the result as div_by_3.npy

print("A =\n", A, "\nElements divisible by 3:\n", Div_by_3) #Print the output of "A" and "div_by_3"

A =
 [[    1     4     9    16    25    36    49    64    81   100]
 [  121   144   169   196   225   256   289   324   361   400]
 [  441   484   529   576   625   676   729   784   841   900]
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]] 
Elements divisible by 3:
 [   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
 2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
 7569 8100 8649 9216 9801]
