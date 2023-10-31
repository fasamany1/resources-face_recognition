# Portfolio Project - Face Recognition Tool With Python

This is a small CLI project  on how I built a face recognition tool using Python. 

## Dependencies To Install

* `dlib` requires both CMake and a C++ compiler to be installed before using it. Its also advisable to install python3-dev
Refer to the [CMake documentation](https://cmake.org/install/) and that of your preferred C++ compiler for 
installation instructions.
* `face_recognition` a python library required for recognition tasks.
* `Pillow` required for comprehensive image handling, manipulation, and format conversion capabilities. 
* `numpy` required for robust numerical and array processing capabilities.

The script will make use of `training/`, `output/` and `validation/` directories, so be sure to create them before running the code.

## Process

* In step 1, I'll create the project environment, install necessary dependencies, and set the stage for your application.
* In step 2, I'll start writing the code. This code will load the training data and start training the model. By the  end of this step, the training data would have been loaded, detected faces in each image, and saved them as encodings.
* In step 3, I’ll build the recognize_faces() function, which recognizes faces in images that don’t have a label.
* Now comes step 4, to draw on the input image! This will help the user see which face is being identified and what it’s being identified as. This will be accomplished by using a popular technique which is to draw a bounding box around the face and give it a label. To do this, I’ll use Pillow, a high-powered image processing library for Python. 
* Step 5 uses the model validation technique that tests the trained model by providing data that it hasn’t seen before but that I have. Knowing the correct label for each image allows me to get an idea of the model’s performance on new data. 
* Step 6 has users in mind, that users can access the app’s functionality. I’ll build a command-line interface for the script using the standard library’s argparse module. 
* Now that project is built, it’s time to actually perform face recognition. I might have saved and played with the program already, but it’s always worthwhile to take it for another spin. That way, I can diagnose bugs, uncover different uses, and more. 

## Usage

The three major phases of the machine learning workflow are represented by the program's three switches:

- `--train`: Initiate the model training process.
- `--validate`: Run a trained model on images stored in the `validation` directory. The faces in these images should be known to you so you can debug the model's performance. 
- `--test`: Run a trained model on an image with an unknown face in it. The script will use the model to detect and attempt to identify the face in the image.
- `-m`: Specify the type of model architecture you want to use. `"hog"` is the default and best for CPU-based training, while `"cnn"` is better for GPU training and will generally give better performance.
