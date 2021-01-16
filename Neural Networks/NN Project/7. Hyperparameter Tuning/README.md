# Hyperparameter Tuning

For hyperparameter tuning, we split it up into 4 runs to reduce the number of combinations to search through. The assumption made here is that the hyperparameters to be tuned across different runs are independent of each other.

We searched for the optimal hyperparameters using grid search, with the help of the [sweep function from Weights and Biases](https://docs.wandb.ai/sweeps/quickstart). For each combination of hyperparameters, the model is trained for 20 epochs.
## Batch Size, Neurons and Learning Rate Sweep
![first_sweep](https://i.imgur.com/XivMX8C.jpg)

## Decay Sweep
![second_sweep](https://i.imgur.com/SObQg23.jpg)

## Dropout Sweep
![last_sweep](https://i.imgur.com/mSdUl2t.jpg)
