# neural_memory
Image reproduction in Tensorflow

## What is this?
This is a script I wrote to demonstrate a potential scheme for visual information storage and reproduction via neural processing. 

I wanted to explore some potential ideas relating to information compression and reproduction using neural processing. This sample script creates and trains a neural network on a 20x34 pixel sample grayscale image (provided) and then uses this trained network to reproduce the image (of course, without any information from the original image itself). 

To run, just clone the repo into a local directory, cd into it, and then run python neural_memory.py

NOTE: The included picture is a .PNG, but it is converted to a .BMP file and processed as such

This kind of approach has a lot of potential applications, particularly in the field of lossless and near-lossless image compression. Instead of sending a full pixel-value matrix, one would only have to train a network locally on a sample image, store/transmit the weights and biases associated, and then have the receiver locally reproduce the image using a network fitted with the received weights/biases.

Another area of application worth looking into is image reconstruction.

## So does this compress images?
No, at least not in its current state. I am new to Tensorflow, and am still working out ways to circumvent some of the limitations which stem from how Tensorflow actually stores information about a trained network in memory.

## Upcoming Features
This scheme makes use of a multi-layer perceptron, or DNN. This technique was chosen because of its efficiency in training and prediction time, which is important for practicality and scalability. 

In terms of raw accuracy, some recent additional reading on the subject has convinced me that use of Recurrent networks, with Long Short Term Memory neurons, used in the context of time-series prediction, is likely the best way to go. Implementing such a scheme is definitely on my to-do list, and I will update this repo when I have had the chance to make some progress in that area.

## Further Reading 
Here are some papers that I found interesting/useful/inspirational for starting this project:

http://www.wseas.us/e-library/conferences/2008/tenerife/CD-CSECS/papers/CSECS21.pdf

http://mattmahoney.net/dc/mmahoney00.pdf

http://arxiv.org/pdf/1308.0850.pdf

http://arxiv.org/pdf/1511.06085v5.pdf

If you want to help improving or using this code or some derivative in another application, feel free to fork this repo.
