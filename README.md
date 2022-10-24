# Dog Breed Classifier

This is my capstone project in the Udacity Data Science Nano Degree.

communicates the libraries used, the motivation for the project, the files in the repository with a small description of each, a summary of the results.

## Motivation for the Project

The purpose of this fun application is to distinguish photos showing human faces from photos showing dogs, estimating the actual breed of the dog (one of 133) and even finding a canine breed that resembles the human face provided on a photo.

## Technical Challenge

The project makes use of a number of technologies that are being refined with getting better and better result -  pretrained Convolutional Neural Networks being the most advanced technology to find the dog breeds.

To identify whether a human face or a dog is shown in the picture, OpenCV (cv2) is utilized. For this purpose the haarcascade_frontalface classifier is used.

In order to find dogs the pretrained RESNET-50 from Kera is used.

Data is preprocessed using the Python imaging library (PIL)

In the next step a simple CNN based on Keras is set up from scratch and trained. It yields an accuracy of slightly over 4%.

Finally a pretrained network for feature extraction is combined with an classifier. This approach is called transfer learning. The network for feature extraction has been trained with great effort already beforehand, so the accuracy is now at over 70%.

An a last step a function is created, that first decides whether a dog or a human is in an input picture, then estimates either the breed of the dog or the dog breed that is most similar to the human.

## Dependencies

The project runs on Python in a Jupyter Notebook.

The following libraries and frameworks must be deployed:

- Scikit Learn (sklearn)
- Keras (with Tensorflow as backend)
- Numpy
- Glob
- Matplotlib
- OpenCV (cv2)
- tqdm (Python progress bar)
- PIL (Python imaging library)

For training to execute in a bearable amount of time, a GPU that supports Tensorflow should be present.

## Files in the repository

- README.md: this file
- dog_app.ipynb: Jupyter notebook that contains the application
- dog_app.html: A HTML version of the notebook for review
- images/own: some images used for testing

As per the Udacity project submission guideline, data files have not been added to this project repository.

However you can obtain these according to the following description (provided by Udacity):

- Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`. 
- Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`.  If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder. 
- Donwload the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz) for the dog dataset.  Place it in the repo, at location `path/to/dog-project/bottleneck_features`.

## Execution

Open the Ipython notebook file and execute cell by cell.

Note: The pretrained VGG-19 network must be downloaded manually, this link is contained in the notebook.

## Blog Post

A more detailled look at the project is available from this link: https://christopherrauh.github.io/Dog-Breed-Classifier/

