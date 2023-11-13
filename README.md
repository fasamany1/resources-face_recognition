# Portfolio Project: FaceRec - Face Recognition Tool With Python

This is a typical CLI project but offers some awesome functionalities. The following content illustrates how this face recognition tool was developed using Python.

## Introduction

This project was not just a coding endeavor but a personal journey inspired by a genuine fascination with the intersection of technology and human connection.

The spark for this face recognition tool ignited when I wondered, how am I able to unlock my phone with my face. So, I asked myself; how does that work? This made me think; What if I can build my own face recognizer? Then I started reading and researching how this could be made possible. And so came to be the idea of developing a face recognition tool.

As I embarked on this adventure, each line of code became a testament to my passion for innovation and problem-solving.

### Explore the Project
This project isn't merely an assignment; it's a Portfolio Project for <a href="https://www.holbertonschool.com/">Holberton School</a>, where I am honing my skills to become a versatile and adept developer.

Dive into the code and explore the intricacies of my face recognition tool on GitHub. Your feedback and collaboration are always welcome as we continue to refine and enhance this project. Connect with me on <a href="https://www.linkedin.com/in/forster-asamany-886907144/">LinkedIn</a>, <a href="https://github.com/fasamany1">GitHub</a>, or <a href="https://twitter.com/FAsamany">Twitter</a>, and let's share our journey in the world of software development. 

## Dependencies To Install

* `dlib` requires both CMake and a C compiler to be installed before using it. It's also advisable to install python3-dev tools
Refer to the [CMake documentation](https://cmake.org/install/) and that of your preferred C++ compiler for 
installation instructions.
* `face_recognition` is a Python library required for face recognition tasks.
* `Pillow` required for comprehensive image handling, manipulation, and format conversion capabilities. 
* `numpy` required for robust numerical and array processing capabilities.

The script will make use of the `training/`, `output/`, and `validation/` directories, so be sure to create them before running the code.

## Process

* In step 1, I'll create the project environment, install the necessary dependencies, and set the stage for your application.

                           Projects directory system
![architecture](https://github.com/fasamany1/resources-face_recognition/assets/9413367/1b704590-7594-4117-bc8e-265b3948cc25)




* In step 2, I'll start writing the code. This code will load the training data and start training the model. By the  end of this step, the training data would have been loaded, detected faces in each image, and saved as encodings.
* In step 3, I’ll build the recognize_faces() function, which recognizes faces in images that don’t have a label.
* Now comes step 4, to draw on the input image! This will help the user see which face is being identified and what it’s being identified as. This will be accomplished by using a popular technique which is to draw a bounding box around the face and give it a label. To do this, I’ll use Pillow, a high-powered image-processing library for Python. 
* Step 5 uses the model validation technique that tests the trained model by providing data that it hasn’t seen before but that I have. Knowing the correct label for each image allows me to get an idea of the model’s performance on new data. 
* Step 6 has users in mind so that users can access the app’s functionality. I’ll build a command-line interface for the script using the standard library’s argparse module. 
* Now that project is built, it’s time to actually perform face recognition. I might have saved and played with the program already, but it’s always worthwhile to take it for another spin. That way, I can diagnose bugs, uncover different uses, and more. 

![facerec1](https://github.com/fasamany1/resources-face_recognition/assets/9413367/8aa2a1d7-2134-48af-ade3-b03fd28bcbc4)


## Usage

The three major phases of the machine learning workflow are represented by the program's three switches:
- `--help`: Show you a list of options, a description of what each of them does, and any arguments that they take.
- `--train`: Initiate the model training process.
- `--validate`: Run a trained model on images stored in the `validation` directory. The faces in these images should be known to you so you can debug the model's performance. 
- `--test`: Run a trained model on an image with an unknown face in it. The script will use the model to detect and attempt to identify the face in the image.
- `-m`: Specify the type of model architecture you want to use. `"hog"` is the default and best for CPU-based training, while `"cnn"` is better for GPU training and will generally give better performance.

- ![facerec2](https://github.com/fasamany1/resources-face_recognition/assets/9413367/35d50a9c-4776-4805-a6d8-6f4e0207b0c6)


## Contributing

Feel free to dive in! Open an issue or submit PRs.

## Relate Projects

* Find a related project <a href="https://github.com/ageitgey/face_recognition">here</a>

## Licensing

* Yet to...
