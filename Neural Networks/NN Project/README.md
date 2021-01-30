# Gender Classification using CelebA & Adience Dataset
![sample_images](https://i.imgur.com/vinysJt.jpg)

Automatic gender classification has been used in many applications including image analysis on social platforms. The goal of this project is to **classify the gender of faces in an image from the [Adience Dataset](https://talhassner.github.io/home/projects/Adience/Adience-data.html)**. One can design a convolutional neural network to achieve this goal. 

### Tasks:
1. Modify some previously published architectures e.g., increase the network depth, reducing their parameters, etc.
2. Consider age and gender recognition simultaneously to take advantage of the gender-specific age characteristics and age-specific gender characteristics inherent to images
3. Consider pre-training using the [CelebA dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)

### Group Members

1. [Ng Chen Ee Kenneth](https://github.com/Todayisagreatday)
2. [Ngo Jun Hao Jason](https://github.com/NgoJunHaoJason)
3. [Goh Yong Wei](https://github.com/YongWei12)

# Overview
![overview](https://i.imgur.com/yOFv0OE.png)

# Highlights
### Dataset Size
![dataset_size](https://i.imgur.com/baj0a66.jpg)

### Plotting Acc/Loss Graphs in wandb
Accuracy             |  Loss
:-------------------------:|:-------------------------:
![acc](https://i.imgur.com/WdK8vG8.jpg)  |  ![loss](https://i.imgur.com/ZrySfPg.jpg)

*Blue line is continuation of red line*

### Final Results
| Model                   | Test Accuracy | Test Loss | Epochs |
| ----------------------- | ------------- | --------- | ------ |
| Baseline MNV2           | 0.8827        | 0.5182    | 20     |
| MNV2 Pretrained         | 0.9147        | 0.1865    | 50     |
| MNV2 Tuned              | 0.934         | 0.06276   | 50     |
| MNV2 Tuned + Pretrained | 0.9287        | 0.7237    | 50     |

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

- *Hyperparameter sweeps are exclusive to wandb. Method 2 will not be able to run sweeps.* 
- *Most notebooks are done in Google Colab and downloaded on Google Drive.* 
- *In the event that you are unable to run it, do add .ipynb to the file name*

# Resources

[Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems](https://www.amazon.sg/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1492032646)

[Transfer learning & fine-tuning in Keras](https://keras.io/guides/transfer_learning/)

[Data Augmentation in Keras](https://keras.io/api/preprocessing/image/#imagedatagenerator-class)

[Loading Data using flow_from_dataframe method](https://keras.io/api/preprocessing/image/#flowfromdataframe-method)

[Recording model results using wandb](https://wandb.ai/site)
