# Pollen-Identification
Pollen Identification system using Resnet18.
Provided is the notebook for cropping data to augument the data. The notebook can be run as is
and it will pop up a simple GUI that will allow you to crop the data you like, name the data,
choose the location you want to save  it and if you like to normalized the output. Also provided
is the notebook for transfer learning for retraining the network, the saved best model, the name
of the classes in a textfile as well as thepredict function which allows you to use the model to
predict your output.The predict model is in the last block of the transfer learning function and 
takes in the class_name.txt, the model you want to use(you can use the provided pollen_model.txt) 
and path to the image you want to predict.Inorder for the transfer learning to work you need to 
set open a folder that contains a folder call train(where your training data is) and val(where 
your training data is). Inside both the train and val folder you will need a folderfor each one 
of your classes and inside those folders you will put the data you want to train the model or 
vadilate the model on. You will need to load this folder into the dataloader.
