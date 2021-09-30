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
- [Notebook](Back_Prop_NN.ipynb.ipynb) and [Excel Sheet](Book1.xlsx)

## Q 1.d Major Steps
There are 3 major steps in this exercise
a. 
## Q 1.e. Error graph with different learning rate [0.1, 0.2, 0.5, 0.8, 1.0, 2.0] 

![](./images/Error_vs_steps_for_different_learning_rates.png)

Note
- With higher learning rate, we are reaching global minima for the weights faster. (assuming simple problem and the error function will be concave with one only minima)
