# Feedforward Neural Networks
*Refer to [File Directory.md](https://github.com/Todayisagreatday/CZ4042-Neural-Nets/blob/main/Neural%20Networks/NN_Assignment/File%20Directory.md) for full list of files with description*

[View Report](https://github.com/Todayisagreatday/CZ4042-Neural-Nets/blob/main/Neural%20Networks/NN_Assignment/5.%20Report%20and%20Diagrams/NN%20Assignment%20Report.pdf)
## Classification - Part A Introduction
This project aims at building neural networks to classify the [Cardiotocography dataset](https://archive.ics.uci.edu/ml/datasets/Cardiotocography) containing measurements of fetal heart rate (FHR) and uterine contraction (UC) features on 2126 cardiotocograms classified by expert obstetricians. The objective is to **design a feedforward neural network that classifies the fetal cardiotocograms according to the fetal state class code** (N= normal; S=suspect; P=pathologic).

### Overview - Part A
<br>

![overview](https://i.imgur.com/2G9nIWr.jpg)

---
## Regression - Part B Introduction

This project uses the [Graduate Admissions dataset](https://www.kaggle.com/mohansacharya/graduate-admissions). The dataset contains several parameters like GRE score (out of 340), TOEFL score (out of 120), university Rating (out of 5), strengths of
Statement of Purpose and Letter of Recommendation (out of 5), undergraduate GPA (out of 10), research experience (either 0 or 1), that are considered important during the application for Master Programs. The objective is to **design a feedforward neural network that predicts the probability of a student
getting admitted into the master’s program**. The predicted parameter is the chance of getting an admit. (ranging from 0 to 1)

### Overview - Part B

<br>

![overview](https://i.imgur.com/MVKo8iV.jpg)

## Running python files
For folders Part A Sweeps and Part B, [wandb](https://towardsdatascience.com/logging-with-weights-biases-da048e3cbc8b) was used to log the results. There are two methods of running the files in these folders.  

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
