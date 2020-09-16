# Election-Prediction-using-machine-Learning

Project Report
for
Google Stock Price Prediction 

Deep Learning


Project By- Shreyas Chate

Introduction

Several studies have been the subject of using machine learning in quantitative finance, predicting prices of managing and constricting the entire portfolio of assets, as well as investment process, and many other operations can be covered by machine learning algorithms. In general machine learning is a term used for all algorithm’s methods using computers to reveal patterns based only on data and not using any programming instructions. For quantitative finance and specially assets selections several models supply a large number of methods that can be used with machine learning to forecast future assets value. This type of model offers a mechanism that combines weak sources of information and makes it a strange tool that can be used efficiently. Here I aim to use ML algorithms based on LSTM RNN to forecast the adjusted closing prices for a portfolio of assets, the main objective here is to obtain the most accurate trained algorithm, to predict future values for our portfolio..


Understand and Define the Problem

In order to create a neural network capable of making predictions, I will use what is known as an LSTM (Long Short-Term Memory models)

Following are the steps involved in this stage of the project.

Importing Modules
Importing Datasets For Training and Testing.
Datasets Preprocessing.
Training Of Dataset into X_Train, Y_Train.
Creating a LSTM RNN model.
Fit the model using X_train, Y_train.
Prediction Of Testing Data
Visualizing the Prediction  



Dataset Preparation and Preprocessing

In this stage of project implementation, focus is put on data collection, data selection, data preprocessing, and data transformation.

Data collection

There are two datasets in csv format for training and testing.
Training dataset contains Stock Prices of Google From 2012 to 2016.
Testing dataset contains random Stock Prices of 2017, from which we have to predict the whole year's stock highs and lows.

Sample Data Structure for training data

              
Date
Open
High
Low
Close
Volume
0
1/3/2012
325.25
332.83
324.97
663.59
7,380,500
1
1/4/2012
331.27
333.87
329.08
666.45
5,749,400
2
1/5/2012
329.83
330.75
326.89
657.21
6,590,300
3
1/6/2012
328.34
328.77
323.68
648.24
5,405,900
4
1/9/2012
322.04
322.29
309.46
620.76
11,688,800

Data Visualization

Data Visualization is done by using MatPlotLib.


Box Plot:
A box plot shows the distribution of quantitative data in a way that facilitates comparisons between variables or across levels of a categorical variable. It can give all the stats provided in dataset .describe in a single plot. If the dataset is too large and the range of value is too big then it shows some values as outliers based on an inter-quartile function.


Data 
Transformation

In this stage, the data is transformed into the form which is appropriate for machine learning. The scaling and normalization is usually used to transform the data.


Using sklearn library, from sklearn.preprocessing import StandardScaler:
StandardScaler is that it will transform your data such that its distribution will have a mean value 0 and standard deviation of 1.

Model Training

In this stage, the training data is fed to the DL algorithm to build and train a model. The purpose of training is to develop a model.

Long Short-Term Memory (LSTM) is one of many types of Recurrent Neural Network RNN, it’s also capable of catching data from past stages and use it for future predictions. In general, an Artificial Neural Network (ANN) consists of three layers: 
1) input layer,
2) Hidden layers,
3) output layer.
In a NN that only contains one hidden layer the number of nodes in the input layer always depend on the dimension of the data, the nodes of the input layer connect to the hidden layer via links called ‘synapses’. The relation between every two nodes from (input to the hidden layer), has a coefficient called weight, which is the decision maker for signals. The process of learning is naturally a continuous adjustment of weights, after completing the process of learning, the Artificial NN will have optimal weights for each synapse. The hidden layer nodes apply a sigmoid or tangent hyperbolic (tanh) function on the sum of weights coming from the input layer which is called the activation function, this transformation will generate values, with a minimized error rate between the train and test data using the SoftMax function. The values obtained after this transformation constitute the output layer of our NN, these value may not be the best output, in this case a back propagation process will be applied to target the optimal value of error, the back propagation process connect the output layer to the hidden layer, sending a signal conforming the best weight with the optimal error for the number of epochs decided. This process will be repeated trying to improve our predictions and minimize the prediction error. After completing this process, the model will be trained.

RNN can’t store long time memory, so the use of the Long Short-Term Memory (LSTM) based on “memory line” proved to be very useful in forecasting cases with long time data. In a LSTM the memorization of earlier stages can be performed trough gates with along memory line incorporated

Model Testing and Evaluation

The data consist of the daily opening prices of stocks covering the period going from 1/1/2012 to 31/12/2016 . To build our model we are going to use the LSTM RNN, our model uses 80% of data for training and the other 20% of data for testing. For training we use mean squared error to optimize our model. Also, in this different Epochs for training data ( 25 epochs, 50 epochs and 100 epochs)  our model will be structured as follow: 

25 Epoch and Batch_size=32
Epoch 25/25
38/38 [==============================] - 4s 115ms/step - loss: 0.0034

50 Epoch and Batch_size=32
Epoch 50/50
38/38 [==============================] - 4s 115ms/step - loss: 0.0022

100 Epoch and Batch_size=32
Epoch 100/100
30/30 [==============================] - 4s 124ms/step - loss: 0.0016


Model Deployment

When the reliable model is selected and validated, the model is put into production. Model Deployment means putting the model in use (production).

In most cases, the deployment is done by translating the Model written in Python language to other languages like Java, C, C++, PHP etc. Then the Alpha and Beta testing is done.

There are various ways of deploying the model. The actual deployment depends on the DL Team size and the IT infrastructure available with the company/business.

This project can also be deployed and integrated in a website or in a software or any mobile application further.

Web Service based Deployment: In this type, the prediction is done continuously. Mostly the private or public cloud is used for deployment.
Real-time based Deployment: In this type, the prediction is done in real time. The data comes from IOT devices or Websites.

Conclusion and Further Development

Deep learning has evolved in recent times to become more reliable with complex functions. The repeated analysis of massive datasets eradicates errors and discrepancies in findings which eventually leads to a reliable conclusion.We can develop real time applications which predict future results according to the user by considering past dataset of the selected company.
