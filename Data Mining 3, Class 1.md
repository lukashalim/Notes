Unit Root Tests: http://www4.stat.ncsu.edu/~dickey/Analytics/Datamine/Powerpoints/Review%20of%20Unit%20Root%20Testing.ppt

Added up-next section: http://www4.stat.ncsu.edu/~dickey/Analytics/Datamine/up_next.txt

### Finishing off topics from previous module.

(1) Finish 
  Categorical inputs
  Polynomials (self study)

### Neural Nets
(2)  Intro to Neural Nets - 

  Chapter 5 in book

  [Neural_draw_tanh.sas](http://www4.stat.ncsu.edu/~dickey/Analytics/Datamine/SAS_code/Neural_draw_tanh.sas):   
      Relate Htan function to Logistic curve.

  Neural1.sas             
      Show construction and behavior of the model 
      Show least squares way to estimate the model from data

  Neural2.sas             
      Show a different basis set (radial basis functions)

#### Model Essentials
- Predict New Cases
 - y is predicted by a linear combination of the predictors
 ![img](pics/neural_nets_1.png)
 - y hat can be continuous response or it can be a logit
 - the tanh function is called the activiation function.  This is because it was originally designed as analogous to the firing of a neural.
 - each hidden layer can have another hidden layer behind it.  This gives neural netwrok a greater flexibilty
 ![img](pics/neural_nets_2.png)
- Select Useful Inputs
- Optimize Complexity
