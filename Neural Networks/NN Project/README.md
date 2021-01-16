# Project Description
![sample_images](https://i.imgur.com/vinysJt.jpg)

Automatic gender classification has been used in many applications including image analysis on social platforms. The goal of this project is to **classify the gender of faces in an image**. One can design a convolutional neural network to achieve this goal. Tasks:
1. Modify some previously published architectures e.g., increase the network depth, reducing their parameters, etc.
2. Consider age and gender recognition simultaneously to take advantage of the gender-specific age characteristics and age-specific gender characteristics inherent to images
3. Consider pre-training using the [CelebA dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
# Overview
![overview](https://i.imgur.com/yOFv0OE.png)

# Dataset Size
![dataset_size](https://i.imgur.com/baj0a66.jpg)

# File Directory
Refer to [File Directory.md](https://github.com/Todayisagreatday/CZ4042-Neural-Nets/blob/main/Neural%20Networks/NN%20Project/File%20Directory.md) for the full list of files with description.

# Running Notebooks
There are 2 ways of running the notebooks. 

### Method 1
**Use wandb library.**
1. Create a free account on https://www.wandb.com/
2. Install the wandb library using pip - ```pip install wandb```
3. Run the cell in the notebook
4. When prompted for the API code, paste the api code and press Enter to login
5. Ensure that the directory path to ```aligned_gender.txt``` is correct when loading the dataframe using ```pd.readcsv()```
6. Ensure that the image path is correctly added to the dataframe

### Method 2 
**Delete all the wandb code.**
1. Delete ```wandb.init()``` and ```config = wandb.config```
2. Remove the defaults dictionary and use variables instead for the hyperparameters
3. Remove the ```[WandbCallback()]``` parameter under ```model.fit()```
4. Replace all ```config.``` to '' as they are not needed unless you're using wandb
5. Ensure that the directory path to ```aligned_gender.txt``` is correct when loading the dataframe using ```pd.readcsv()```
6. Ensure that the image path is correctly added to the dataframe

# Additional Notes
*Hyperparameter sweeps are exclusive to wandb. Method 2 will not be able to run sweeps.* 

*Most notebooks are done in Google Colab and downloaded on Google Drive.* 

*In the event that you are unable to run it, do add .ipynb to the file name*
