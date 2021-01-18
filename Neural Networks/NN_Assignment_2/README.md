# Assignment 2

- [View assignment report](https://github.com/Todayisagreatday/CZ4042-Neural-Nets/blob/main/Neural%20Networks/NN_Assignment_2/5.%20Report%20and%20Diagrams/Ng_Chen_Ee_Kenneth_A2_report.pdf)

- [View assignment objectives](https://github.com/Todayisagreatday/CZ4042-Neural-Nets/blob/main/Neural%20Networks/NN_Assignment_2/7.%20Assignment_2_objectives.pdf)

## Object Recognition with CNN - Part A

### Introduction 

<p align="center">
  <img width="470" height="365" src="https://i.imgur.com/TIjrg8H.jpg)">
</p>

The [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) dataset consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.

The dataset is divided into five training batches and one test batch, each with 10,000 images. The test batch contains exactly 1000 randomly selected images from each class. The training batches contain the remaining images in random order, but some training batches may contain more images from one class than another. Between them, the training batches contain exactly 5000 images from each class.

For the purpose of this assignment, the **training sample has been reduced to 10000 training samples and 2000 test samples.**

## Highlights

### Extracting feature maps using Keract
![feature_maps](https://i.imgur.com/8lpCtpO.jpg)

### Comparing accuracy and loss between optimizers

![p_coords_graph](https://i.imgur.com/sJVUr69.png)

## Text Classification with CNN/RNN - Part B

### Introduction

The dataset used in this project contains the first paragraphs collected from Wikipage entries and the corresponding labels about their category.
The training and test datasets are read from ‘train_medium.csv’ and ‘test_medium.csv’ files. The training dataset contains 5600 entries and test dataset contains 700 entries. The label of an entry is one of the 15 categories such as people, company, schools, etc.

The purpose of this project is to **perform text classification using CNN and RNN to predict the category of the line of text.**

## Highlights

### Comparing between different RNN and CNN models 

![graph](https://i.imgur.com/ZBwgse5.png)

### Table of Results

![table](https://i.imgur.com/XVkPBiu.jpg)

---

## File Directory

For a full list of files with description, do refer to [File Directory.md](https://github.com/Todayisagreatday/CZ4042-Neural-Nets/blob/main/Neural%20Networks/NN_Assignment_2/File_Directory.md)

## Running Notebooks
There are 2 ways of running the notebooks. 

### Method 1
**Use wandb library.**
1. Create a free account on https://www.wandb.com/
2. Install the wandb library using pip - ```pip install wandb```
3. Run the cell in the notebook
4. When prompted for the API code, paste the api code and press Enter to login
5. Ensure that the directory path is correct when loading the data

### Method 2 
**Delete all the wandb code.**
1. Delete ```wandb.init()``` and ```config = wandb.config```
2. Remove the defaults dictionary and use variables instead for the hyperparameters
3. Remove the ```[WandbCallback()]``` parameter under ```model.fit()```
4. Replace all ```config.``` to '' as they are not needed unless you're using wandb
5. Ensure that the directory path is correct when loading the data

- *Hyperparameter sweeps are exclusive to wandb. Method 2 will not be able to run sweeps.* 
- *Most notebooks are done in Google Colab and downloaded on Google Drive.* 
- *In the event that you are unable to run it, do add .ipynb to the file name*
