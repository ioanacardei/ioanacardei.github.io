---
layout: page
title: Jellyfish Classification
description: Convolutional Neural Networks for Jellyfish Classification. Used deep learning tools including Keras, SkLearn, and TensorFlow.
img: assets/img/jelly.jpg
importance: 1
category: work
related_publications: false
---

My project is on deep learning for classification of 6 types of jellyfish (Barrel, Blue, Compass, Lions Mane, Mauve Stinger and Moon) using sklearn, keras, and tensorflow in addition to numpy and matplotlib for plotting. This data set is from kaggle- https://www.kaggle.com/datasets/anshtanwar/jellyfish-types
<br>
<br>
6 different models were implemented- simple_CNN, reg_CNN and batch_CNN with 3x3 filters and 5x5 filters
<br>
<br>
Simple_CNN - Has three convolutional layers, each followed by a max pooling layer, a flatten layer, a fully connected dense layer, and an output layer with softmax activation for multi-class classification.
<br>
<br>
Reg_CNN- includes dropout layers to regularize the model and prevent overfitting, potentially making it more robust but possibly requiring more training time and data to achieve optimal performance.
<br>
<br>
Batch_CNN- Uses batch normalization to stabilize and potentially speed up training by normalizing activations. Has a batch normalization after each convolutional layer
<br>
<br>
First, I created three data generators for the training, validation, and test dataset using the flow_from_directory method. Each instance reads images from the respective directories, resizes them to 150x150 pixels, rescales the pixel values, and yields batches of images and their corresponding labels (labels are one-hot encoded for categorical classification tasks).
<br>
<br>
code below
<br>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


5 subplots of the moon Jelly using matplotlib
<br>
<br>
code and plot

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Labeling the Classes

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The the types of CNN models

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Training on the 6 CNN models using 3x3 and 5x5 filters 
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_7.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Plotting results (Accuracy and Loss)
<br>
<br>
Code
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_8.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Plots
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_9.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_10.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Testing/Results
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_12.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Highest test accuracy
<br>
Test Accuracy: 0.6499999761581421 for 5x5 no dropout CNN
<br>
F1 Score: is 0.17067307692307693 for 5x5 no dropout CNN
<br>
<br>
<br>

Visualizing feature detection at different convolutional layers using VGG16 
<br>
<br>
code
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_13.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Visualization of a 3x3  filter CNN no drop out, blue_jellyfish photo
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jelly_14.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
 This image depicts which parts of the image are being activated by different filters in the convolutional layers, providing insights into what the model is learning!!





<!-- <div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above: -->


