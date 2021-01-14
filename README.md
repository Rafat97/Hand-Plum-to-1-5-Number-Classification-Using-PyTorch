# Hand-Plum-to-1-5-Number-Classification-Using-PyTorch

 Developing  a  program  that  will  classify  the  number  of  fingers  from  animage of a hand palm.The main goal of this task is that an image of a hand palm will be givenas input.  The output should be the number of fingers in that image.  Wecan say this is a classification problem.  We have to classify the image from1 to 5 based on the finger.

# Brief description of the methodology 

We used Google Colab. Also, we used CUDA for
completing all the tasks. We divided the whole process into six different
parts. They are-

**Load Data from external URL :**

In this part, we loaded the dataset from Hands.zip and extracted
into ./content/Hands folder.

**Image pre-processing & Data augmentation :**

After loading data from an external URL, we defined the training and
validation directory. Then, checked if the image is loaded correctly
or not. After doing this, we transformed the image using factors
like center crop, resize, color, converting tensor, and many more.
Also, We resized our image into 128 x 128 pixels. And, We set the
batch size as 32. Because we didn’t want to load full datasets at a
time. Finally, we loaded data into two different parts, the first one
is training and the second one is validation. Also, we created five
classes in the dataset. The dataset looks like this after preprocessing

<p align="center"><img src="https://raw.github.com/Rafat97/Hand-Plum-to-1-5-Number-Classification-Using-PyTorch/main/Images/barch_of_image.png" title="Image pre-processing & Data augmentation" alt="Image pre-processing & Data augmentation"></p>



**Creating Own Model :**

This was the most challenging part of our task. We had to do a
lot of fine-tuning to finalize this model that performs well in our
current dataset. We created this model using four convolution layers,
four linear layers, two dropout layers, and Re-Lu as an activation
function. The model looks like this -

<p align="center"><img src="https://raw.github.com/Rafat97/Hand-Plum-to-1-5-Number-Classification-Using-PyTorch/main/Images/Image.png" title="Image pre-processing & Data augmentation" alt="Image pre-processing & Data augmentation"></p>


**Training Process :**

To create this model, we used Categorical Cross entropy for loss
function. And Adam as an optimizer. We used these because more
than two classes had to be classified. That’s why we went for this
approach. We set the optimizer learning rate to 0.001. Then we set
the training epoch or iteration to 64. After setting all the variables,
finally, we started training and observed the training loss, training
accuracy, validation loss, validation loss.


**Output Visualization & Saving model :**

One eternity later, the training was completed and we got some
pretty good results. The result we got is -

| Name      | Percentage |
| :---        |    :----:   |
| Last Training Accuracy      | ≈96%       |
| Last Validation Accuracy   | ≈94%        |



Then we visualized every training step of accuracy and testing in the
graph. The graph visualization look likes this -

<p align="center"><img src="https://raw.github.com/Rafat97/Hand-Plum-to-1-5-Number-Classification-Using-PyTorch/main/Images/4_2.png" title="Image pre-processing & Data augmentation" alt="Image pre-processing & Data augmentation"></p>


**Testing Model :**

We implemented two types of testing. They are -

- Testing data from the dataset
- Using colab file upload option


<p align="center"><img src="https://raw.github.com/Rafat97/Hand-Plum-to-1-5-Number-Classification-Using-PyTorch/main/Images/testing_img.png" title="Image pre-processing & Data augmentation" alt="Image pre-processing & Data augmentation"></p>

