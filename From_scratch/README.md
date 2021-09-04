# Neural Network From scratch 

## Implementation of a Neural Network 
### **Import Required libraries**
> First, we are going to import Python libraries. We are using NumPy for the calculations:
```
import numpy as np
```
### **Assign Input values**
> Next, we are going to take input values for which we want to train our neural network. Here we can see that we have taken four input features. In actual data sets, the value of the input features is mostly high.
```
# Training Set
X = np.array( [[1, 0, 0, 0],
               [1, 0, 0, 1],
               [1, 0, 1, 0],
               [1, 1, 0, 1],
               [1, 1, 0, 0],
               [1, 1, 1, 1]] )
```
### **Target Output**
> For the input features, we want to have a specific output for specific input features. It is called the target output. We are going to train the model that gives us the target output for our input features.
```
# Gold/Actual Label or Output
y = np.array([[0],
              [0],
              [0],
              [0],
              [0],
              [1]])
```
### **Assign the Weights**
>Next, we are going to assign random weights to the input features. Note that our model is going to modify these weight values to be optimum. At this point, we are taking these values randomly or zeros. Here we have two four features, so we are going to take four weight values.
```
# Initialize the wights - randomly or with zeroes
# w = np.random.random((4, 1))
# or,
w = np.zeros((4, 1))
```
