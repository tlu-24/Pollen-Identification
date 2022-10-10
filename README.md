# Pollen-Identification
Pollen Identification system using Resnet18. The model can identify 23 different species of pollen local to Bernard Field Station. It first crops out individual pollen from a photo(there may be many pollen in a single photo) which will be used to training data. The cropping is done with a GUI created with Tkinter allowing for mutiple photos to be cropped and named at once. Transfer learning was then done allowing for the model to be created. Although we did not have enough data for the model to be reliable, it served as a proof of concept. Data argumentation techniques were also done to hopefully combat the lack of data.

## Requirements
This code uses Python 3.7+. For more information on checking your python version and upgrading or installing see [here](https://realpython.com/installing-python/). Other requirements are below.

- [OpenCV](https://pypi.org/project/opencv-python/)
- [MatPlotLib](https://matplotlib.org/stable/users/installing.html)
- [numpy](https://numpy.org/install/)
- [Tkinter](https://docs.python.org/3/library/tkinter.html)
- [numpy](https://numpy.org/install/)
- [torch](https://pypi.org/project/torch/)
- [torchvision](https://pytorch.org/vision/)
- [time](https://docs.python.org/3/library/time.html)
- [os](https://docs.python.org/3/library/os.htmlcop)
- [copy](https://docs.python.org/3/library/copy.html)

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
