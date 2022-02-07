# Differential_equation_predictor

This is a repository for my project on classifying the outcome of a set of nonlinear ordinary differential equations (ODEs) using a neural network. The code is provided as a Jupyter notebook and there is a folder ("Label_SS") with csv files of all the data used. 
Each file is for a particular set of parameters used for the ODEs and contains the final output for 1000 different random inputs.

The inspiration for this project is that for some nonlinear ODEs, there can be multiple steady-states, i.e., final outputs, for a certain set of parameters. For example, the ODEs studied in this project (displayed in equations.pdf) can have two different outputs. This phenomenon is known in physics as Bistability and is of particular interest in many physical systems, including cold atom physics.

Having two possible outputs is similar to a classification problem. Therefore, I was curious if it was possible to train a dense neural network to predict which of the final outputs a given input will result in, rather than just solving the ODEs numerically. It turns out the answer is yes - the model in the notebook can predict the output with a 97% accuracy for many different parameters. 

While this project so far has mainly just been proof of principle and interest, a more practical application is that for larger numbers of ODEs, it can take several minutes or even hours to obtain the final output for a given input. While this would have to be done many many times to obtain the data needed to train a neural network, the final trained model could eventually be used to obtain the output of the ODEs instead, which would be much faster, and also useful if the output of the ODE was needed in some external application.
