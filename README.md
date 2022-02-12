# TlResNet
transfer learning, ResNet34


prgorams:
model.py    # Building the model framework structure
train.py    # training the final model: combined with a specific transfer learning strategy to fine-tune the parameters of pre-trained model to obtain the final model
predict.py  # predicting the class of microsomal fossils using the final model


datas:
data_set    # train, validation and test set images of 9 taxon microsomal fossils

models：
-pre.pth    # pre-training model
.pth        # final Model


operating steps:
train.py -> predict.py
1. introduce the ImageNet pre-trained model parameters file；
2. Modify the code of the transfer strategy in the train.py file according to specific needs, i.e. freeze some layers of the pre-trained model；
3. use 9 microfossil datasets to retrain based on the pre-trained model and migration strategy to get the final model and save it；
4. use the trained final model to predict the microfossil classes in the test set and output the results.
