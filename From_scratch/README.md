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
> Next, we are going to assign random weights to the input features. Note that our model is going to modify these weight values to be optimum. At this point, we are taking these values randomly or zeros. Here we have two four features, so we are going to take four weight values.
```
# Initialize the wights - randomly or with zeroes
# w = np.random.random((4, 1))
# or,
w = np.zeros((4, 1))
```

### **Applying a Sigmoid Function**
- Activation
> Once we have our weight values and input features, we are going to send it to the main function that predicts the output. Now notice that our input features and weight values can be anything, but here we want to classify data, so we need the output between 0 and 1. For such, we are going to a sigmoid function. 
- Derivative 
> we are going to need the derivative of the sigmoid function.
```
def sigmoid(z, derive=False):
  derivative
  if derive == True:
    return z*(1-z)
    
  # sigmoid rule
  return 1/(1+np.exp(-z))
```
### `<main>` **predicting output and updating the weight values**
```
# Training the ANN (perceptron)... Setting No. of Iteration (epochs)
for iter in range(1000):
  # Forward Propagation: to Predict output (y_hat)
  z = np.dot(X, w)
  y_hat = sigmoid(z)
  # print(y_hat)

  # simple 'cost' calculation
  cost = y - y_hat

  # Back-propagtion (future studies)
  dy_hat = sigmoid(y_hat, derive=True)
  delta_w = cost * dy_hat

  # update weights
  w += np.dot(X.T, delta_w)
```
### **Predicting values**
> Since we have trained our model, we can start to make predictions from it.
```
# Test Set
T = np.array([[1, 0, 1, 1],
              [1, 1, 1, 0]])

# Final Predictions on the Test Set
y_hat = sigmoid(np.dot(T, w))

print("\nTest Predictions...")
print(y_hat)
````

---
> more updates will be included soon . . .
---

> **Reference link :** 
* [*Towards AI*](https://pub.towardsai.net/building-neural-networks-from-scratch-with-python-code-and-math-in-detail-i-536fae5d7bbf)
* [*Logic Gate*](https://en.wikipedia.org/wiki/Logic_gate)
* [*Roberto Iriondo*](https://www.linkedin.com/in/robiriondo/)