# TSAI - END3 Session 2 Assignment
*Group Members: Dhruba Adhikary, Phani Nandula, Prateek Maheshwari, Sujit Ojha*

# Assignment Objective
1. Rewrite the whole excel sheet showing backpropagation. Explain each major step, and write it on Github.  
   a. Use exactly the same values for all variables as used in the class  
   b. Take a screenshot, and show that screenshot in the readme file  
   c. Excel file must be there for us to cross-check the image shown on readme (no image = no score)  
   d. Explain each major step  
   e. Show what happens to the error graph when you change the learning rate from [0.1, 0.2, 0.5, 0.8, 1.0, 2.0]   


# Solution
## Q 1. Rewrite the whole excel sheet showing backpropagation. Explain each major step.
- [Notebook](Back_propogation_NN.ipynb) and [Excel Sheet](Book1.xlsx)

## Q 1.a Use exactly the same values for all variables as used in the class
![MicrosoftTeams-image (2)](https://user-images.githubusercontent.com/30425824/135452661-f635d214-bcaa-4c65-9958-771653c7f35c.png)

## Q 1.d Major Steps
Below are the defined major steps in this exercise  
   a. Initialization - Weights of the neural network are initialized as : w1 = 0.15, w2 = 0.2, w3 = 0.25, w4 = 0.3, w5 = 0.4, w6 = 0.45, w7 = 0.5, w8 = 0.55  
   b. Utility functions - Sigmoid Activation function  : This is used to squash all the values between 0 and 1  
   c. Forward propagation - Given the weights and inputs this function calculates the predicted output of the netowrk  
   d. Error Calculation - Calculate ```0.5* Squared Error``` between predicted output and target values  
   e. Gradient functions for each weights of the netowrk - These functions calculate the gradients of Error with respect to each weights in the network. This determines the direction and size of step we could take in the direction of minima. Two gradient functions are defined one for each layer. ```gradient_layer1``` function updates the weights that connect the input layer to the hidden layer. ```gradient_layer2``` function updates the weights that connect the hidden layer to output layer.     
   f. Updation of weights - We have incorporated updation of weights for each iteration in a ```for loop```. Each weight is updated by taking only a fraction of step size. The fraction here is defined using learning rate. Higher the learning rate greater the step we take. As a common practice learning rates are in the range between 0 to 1.    
   g. All the above steps are run for different learning rates in a for loop.   

Below images shows the paths that contribute to the updation of weight **w1** 
![Untitled](https://user-images.githubusercontent.com/30425824/135589121-9998bcd5-e94b-44d3-b07d-776d94ed3399.jpg)

Below image shows the paths that contribute to the updation of weight **w8**
![IMG-0138](https://user-images.githubusercontent.com/30425824/135589178-5146e5fd-c986-49ca-a04c-7025ced5bbff.jpg)

## Q 1.e. Error graph with different learning rate [0.1, 0.2, 0.5, 0.8, 1.0, 2.0] 

![](./images/Error_vs_steps_for_different_learning_rates.png)

Note
- With higher learning rate, we are reaching global minima for the weights faster. (assuming simple problem and the error function will be concave with one only minima)
