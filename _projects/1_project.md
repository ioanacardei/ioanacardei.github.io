---
layout: page
title: Jellyfish Classification
description: Convolutional Neural Networks for Jellyfish Classification. Used deep learning tools including Keras, SkLearn, and TensorFlow.
img: assets/img/jelly.jpg
importance: 1
category: work
related_publications: false
---

Deep learning for classification of 6 types of jellyfish (Barrel, Blue, Compass, Lions Mane, Mauve Stinger and Moon) using sklearn, keras, and tensorflow in addition to numpy and matplotlib for plotting
6 different models were implemented- simple_CNN, reg_CNN and batch_CNN with 3x3 filters and 5x5 filters. 
Simple_CNN - Has three convolutional layers, each followed by a max pooling layer, a flatten layer, a fully connected dense layer, and an output layer with softmax activation for multi-class classification.
Reg_CNN- includes dropout layers to regularize the model and prevent overfitting, potentially making it more robust but possibly requiring more training time and data to achieve optimal performance.
Batch_CNN- Uses batch normalization to stabilize and potentially speed up training by normalizing activations. Has a batch normalization after each convolutional layer
First, I created three data generators for the training, validation, and test dataset using the flow_from_directory method. Each instance reads images from the respective directories, resizes them to 150x150 pixels, rescales the pixel values, and yields batches of images and their corresponding labels (labels are one-hot encoded for categorical classification tasks).


</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.



The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:


