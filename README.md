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

## Usage

The croppying.ipynb should be ran frist which will allow for a simple GUI to appear that will allow for you to choose what images you want to be cropped. There will be the option to normalize your image, what folder you want to save the resulting photos at and the name you want them the photos to be. The resulting photos should be saved into a folder that will be the training data and a folder that will be that validation. The suggested split is 70 training 30 validation.

The project.ipynb should be ran next which allow for you to preform transfer learning. The option to save your model is given at the end.

pollen_model.pt is also provided which allows for you to use the resulting model created with data from pollen from around bernard field station.
