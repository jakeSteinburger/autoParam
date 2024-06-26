# AutoParam
Automatically choose model hyperparameters and train a feedforward neural network based on nothing but a CSV.

## Introduction
AutoParam accepts data from a csv file and chooses the optimal hyperparameters automatically, including the:
- Number of epochs
- Learning rate
- Model size
Then, the model automatically trains on the csv training data file given.

AutoParam is based on TensorFlow, and is written in Python. After training, it stores the model in a folder of saved models, which can then be run. AutoParam is a terminal application.

*Please note that models generated by AutoParam are **not** always accurate, and can make mistakes often. It is up to your data to ensure that it's accurate.* Models trained by human professionals will always likely be more accurate.

## Limitations
AutoParam currently **only works with a single output**.

This means that it can output a single number based on inputs, or output a single True or False boolean based on the inputs, but it can **not** calculate a probability out of several options, or calculate several different numbers. 

## Installation
To install AutoParam, ensure you have installed git, then run in your terminal:
```
git clone https://github.com/jakeSteinburger/autoParam
```
Unzip the project and continue to the **Usage** section's instructions.

You'll also need to install the requirements before usage during installation. AutoParam required PyTorch to be installed, but nothing else is needed. You can install PyTorch using pip. On Linux and Unix-based systems, you can run in your terminal:

```
pip3 install torch
```

and on Windows, you can run in your terminal:

```
pip install torch
```

You'll also need to have the Python interpreter installed (Using version 3+).

## Usage
Once you've installed AutoParam, go into the project directory and run `autoparam.py`, and follow the instructions in the terminal.

You should get told to read in the README how to format the csv training data file, so here's an example on how to do it:

|Label        |Input 1|Input 2|Any other inputs...   |Output|
|-------------|-------|-------|----------------------|------|
|Patient 1    |49     |32     |Any other input values|92    |
|Patient 2    |82     |16     |Any other input values|26    |
|Patient 3    |12     |38     |Any other input values|85    |

The first whole row should simply be labels of the input types, eg. names of symptoms that could be used for diagnosis. The first cell of the first row doesn't really matter, but you can just set it to `Label`. The last cell of the first row should either simply say `output` or label the exact thing that's being calculated. 

In each other row, the first cell is a text label for the training example. It doesn't matter too much, so you can leave that empty if you want. The last cell of each element should contain the output of the training example, and all the other rows should be parameter values. Each row (beside the first one) corresponds to one training example.

## Project
### Future
This project is quite a short term project that I don't intend to work on a lot more in the future, however I would like to at some point add functionality for multiple outputs and give it a GUI server.
### License
AutoParam is under the MIT license. See LICENSE.md for more information.
### Issues
Besides the limitations that I have already stated, please feel free to report bugs or issues in the `issues` tab. You can also contact me directly at [jake.stbu@gmail.com](mailto:jake.stbu@gmail.com).
