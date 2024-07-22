# Design-of-Model-Predictive-RBFN-Controller-for-non-linear-plants

![Type](https://img.shields.io/badge/Type-Course_Project-yellow)
![Concepts](https://img.shields.io/badge/Concepts-Industrial_Control,_Machine_Learning-blue)
![Language](https://img.shields.io/badge/Language-MATLAB-red)
![Libraries](https://img.shields.io/badge/Libraries-Simulink-green)

This repository contains files related to designing of model predictive RBFN controller for non-linear plants modelled using U-model, using Simulink (MATLAB).
The project aims to develop a model predictive RBFN controller for non-linear plant modelled using U-model.

Elaborate details regarding the project can be found in the [Project Report](https://drive.google.com/file/d/1PXgjmmPS2wIvdBZJKlpJ_-K1X9XZsg-e/view?usp=share_link)

Team Members - Parth Goyal, Utkarsh Kedia, Neelabh Sinha

## Simulation Setup -
 The simulation setup of the entire project can be described as follows on a block level -
 
 <img src="/Visualizations/Simulation Setup.PNG"/>

Plant and plant' are same plant models placed in parallel to analyse relative difference in performance with and without the controller. 
The neural network architecture of the controller is that of a standard RBFN with 1 hidden layer (having Gaussian Activation function) and 1 output layer, and can be visualized as follows -

<img src="/Visualizations/Model.PNG"/>

The two plant models can be seen as follows -

1st Degree Plant -

<img src="/Visualizations/Degree 1 Plant/Plant 1.PNG"/>

4th Degree Plant -

<img src="/Visualizations/Degree 4 Plant/Plant 2.PNG"/>

## Description of the repository -
- Plants - Containes model files of plants
- Setups - Contains complete simulation setups
- Visualizations - Contains various graphs and diagrams related to the model and training results 
- Report - Contains complete report of the project

## Training -

Training was done by generating random data sample from the plant and training the network using them. The NN Predictive Controller block was used for training, which can be described as follows -

- Develop the model file in Simulink
- Define Hyperparameters of the neural network training process
- Generate Random data points from the model of the plant
- Train the model on the dataset that is generated
- Simulate the system to obtain input and output.

Sampling period was taken to be 0.2 seconds to accommodate a more realistic scenario.

## Results -

The results of 1st degree plant is only shown here. Complete details for both plants can be seen in the Project Report.

Training Results -

<img src="Visualizations/Degree 1 Plant/Performance (Plant 1).png" width="50%"/>

<img src="/Visualizations/Degree 1 Plant/Regression (Plant 1).png" width="50%"/>

After the training process, the final output comes out to be (Y(k) is with controller and Y'(k) is without controller) -

<img src="/Visualizations/Degree 1 Plant/Results (Plant 1).png"/>
