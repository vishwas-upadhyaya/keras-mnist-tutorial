# keras-mnist-tutorial

## Project Overview
This project is a simple quick-start tutorial on performing digit recognition using a neural network built with Keras. Originally created for a tutorial at the University of Toronto, it demonstrates how to build, train, and evaluate a Multilayer Perceptron (MLP) on the popular MNIST dataset. The tutorial guides the user through installing prerequisites, loading and formatting data, building a 3-layer neural network, compiling it, training it, and evaluating its performance on predicting handwritten digits.

## Deep Technical Details (Architecture, Pipeline)

### Architecture
The model uses a 3-layer fully connected Neural Network (Multilayer Perceptron):
- **Input Layer:** Takes a 784-dimensional vector (flattened 28x28 image).
- **Hidden Layer 1:** Dense layer with 512 units and `ReLU` activation, followed by a `Dropout` layer (rate of 0.2) to prevent overfitting.
- **Hidden Layer 2:** Dense layer with 512 units and `ReLU` activation, followed by a `Dropout` layer (rate of 0.2).
- **Output Layer:** Dense layer with 10 units (for the 10 digit classes) and `Softmax` activation to output a valid probability distribution.
- **Loss Function:** Categorical Crossentropy.
- **Optimizer:** Adam.

### Data Pipeline
1. **Loading Data:** Fetches the MNIST dataset consisting of 60,000 training and 10,000 testing images.
2. **Reshaping:** Converts each 28x28 image into a single 784-dimensional vector.
3. **Normalization:** Scales input pixel values from the `[0, 255]` range to `[0, 1]` by converting data types to `float32` and dividing by 255.
4. **Target Encoding:** Applies one-hot encoding to the target labels (e.g., class `0` becomes `[1, 0, 0, ... 0]`) to prepare them for categorical crossentropy loss calculation.

## Tech Stack
- **Python** (Tested on Python 3)
- **Keras** (Deep Learning library)
- **NumPy** (Numerical operations and matrix transformations)
- **Matplotlib** (Data visualization)
- **Jupyter Notebook** (Interactive environment)