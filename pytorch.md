# PyTorch

* Not a framework, a library

## Components

### Dataloader

Must inherint Dataset:  
> class ThisLoader(Dataset):

Functions to implement:  
> def \_\_init\_\_(self, ...)  
> def \_\_len\_\_(self)  
> def \_\_getitem\_\_(self, index)  

### Training

#### Train

For each epoch, we want to:
* Perform validation by checking our relative loss on a set of data that was not used for training, and report this
* Save a copy of the model


#### Train One Epoch

* Gets a batch of training data from the DataLoader
* Zeros the optimizer's gradients
* Performs an inference - that is, gets predictions from the model for an input batch
* Calculates the loss for that set of predictions vs. the labels on the dataset
* Calculates the backward gradients over the learning weights
* Tells the optimizer to perform one learning step - that is, adjust the model's learning weights based on the observed gradients for this batch, according to the optimization algorithm we chose
* It reports on the loss for every 1000 batches.
* Finally, it reports the average per-batch loss for the last 1000 batches, for comparison with a validation run

