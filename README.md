# AutoEncoder

AutoEncoder are really usefull in many applications, in this repo their appication in anomaly detection is put to the test. As its known AutoEncoders are really good way to learn pattern that made up the data , this quality of Autoencoders make them really usefull in anomaly detection like in case of Fraud-Detection where data is highly unbalanced. 

## How AutoEncoders are used for anomaly detection

AutoEncoders are made up of two parts an Encoder and a Decoder. Encoder part takes the input and represent it in a dense manner usually called as Dense Representation and Decoder part does the opposite. Which means the input and the output of an autoencoder is the same, and the error function that steers the trainig process is Reconstruction error which compares the input and the output of the AutoEncoder.

In anomaly detection we train the AutoEncoder on the larger class (normal transaction class in this example) doing so it make sense of the patterns in the normal class . When after training the smaller class (fraud class) is fed to the AutoEncoder it gives high Reconstruction Error which conveys that this example does not conform with the pre learnt patterns. 


## Code Overview

This repo is a basic implementation of four layered autoencoder ,Where both parts encoder and decoder has 2 layers each.

Notebook starts by loading data into the dataframe and check how balanced the data is 

Fraud Transactions: 242   Normal Transaction: 113681

This is a higly unbalanced data.

Input and out outputs are separated in X and Y respectivly. 

Rest of the code contains information about the implementing the encoder and decoder whcih later combined and compiled to come up with the autoencoder. 

