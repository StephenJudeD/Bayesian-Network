# Bayesian-Network
Bayesian Network using “Lymphography” data set (https://archive.ics.uci.edu/ml/datasets/Lymphography)

After importing and loading the dataset, I completed some key data preparation steps – checking for null values, checking the datatypes, and visualising the data with a correlation plot.
The dataset had four classes. Which I reduced to two as per the requirements.
 
I then converted the remaining classes to binary – 0 & 1.
Class 0 = Metastases
Class 1 = Malign Lymph

I tried several ‘feature selection’ options – PCA, LDA and Feature Importance’s. In the end the one that worked best was Chi2. I completed two different methodologies and got the same result. (Figure 3). I initially tried 5 features, as value of significance, alpha =0.05, was equal to the bottom 5, p value <= alpha. In the end I went with 8 as it worked better, with greater accuracy from the model (displayed below in part B). I then completed the training and testing split (70% as requested). I then imported the necessary libraries - pgmpy, a python library for working with graphical models. Loading estimators to build our model, I tried both maximum likelihood and Bayesian - which is essentially a fight between frequentist and Bayesian probability. 
The Hill Climbing Algorithm is a local search algorithm that continuously moves towards increasing heights/values to find the top of a mountain or the best solution to a problem. Using this methodology, I could then view the conditional probability distributions (CPDs) of the nodes given values of their parents.
 
After I built CPD, I was able to produce the DAG that forms the foundation of my model. I tried a variety of estimators and discovered that they generated a simpler DAG but were less accurate when running the model. Using the Class Indicator, I then inferred the evidence obtained from the Hillclimb search and DAG. I then used scikit-learn libraries to test the accuracy. 

I used keras for the ANN, and I experimented with various parameters (relu, sigmoid, softmax, tanh, and SGD optimisers) and batch quantities and epochs. The parameters I chose in the notebook appeared to be the most important. I also experimented with batch quantities and epochs and came to a decision of 32 batches and 50 epochs.

