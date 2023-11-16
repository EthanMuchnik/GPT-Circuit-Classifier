# GPT Visual Language Classifier

### What Is This?

This is research Code For Utilizing merging Computer Vision Algorithms mixed with the GPT API to interpret images containing visual "languages" like circuits.

Essentially while ChatGPT is the state of the art at interpreting a text input, it is not good at giving meaningful feedback for images. Until November of 2023, it couldn't even process images and now it is unable to give complex answers about the state of a circuit when an image of it is given. This is remedied through the use of PyTorch Scene Classifiers, the YOLO CNN framework, and the use of the GPT API. Below are the steps involved in the algorithm.

### Steps To Algorithm

1. Figure out if an image is a circuit or not. If yes, go to step 5 with a generic prompt. Otherwise, go to step 2.
2. Use custom-trained YOLO CNN to predict bounding boxes around all the components of the circuit.
![Description](Data/Generated-Results/trainSet/Circuit-10_png.rf.5ec2533d162796743891fa863956a79e.jpg)
4. Generate a GPT prompt via custom-created algorithm so that the circuit is adequately described.
5. If came from step 3, funnel prompt to GPT api. Otherwise funnel a mix of the image with a generic prompt to GPT API.

### Future Improvements/Features

- A chrome web extension is currently in the works.
- Segmentation is currently being tested.

