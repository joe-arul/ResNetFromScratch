# Convolute 
### (Exploring Image Recognition concepts using ConvNets)

## Purpose of the Project
- Train a deep neural network model that recognizes images in a CIFAR10 dataset
- Test ConvNet hyperparameters 
- Explore techniques to better model accuracy on image data
- Achieve high accuracy on CIFAR10 in deep learning class competition at USF (**Achieved highest in class - 90.05% on test set**)

## Techniques tried to better accuracy
- Dropout
- Batch Normalization
- Data Augmentation
- Hyperparameter tuning
- Residual Learning
- Designed several architectures from scratch (LeNet, AlexNet, VGG16, ResNet)

## Infra
- Tensorflow with Keras
- NVIDIA A100 GPU on Colab

### **Project Available here :  [Notebook](notebooks/convolute.ipynb>)**

## Summary of Results :
- VGG16 architecture (15 layers, 75 training epochs) achieved 90.05% accuracy on test data with loss 0.317.
- ResNet architecture (48 layers, 35 training epochs) achieved 82% accuracy on training before I ran out of compute units and lost access to the runtime and the model.

## ResNet Model Architecture :

- 48 layers in total (including 4 convolutions for identity blocks)
- 3 layers in each identity block
- 4 layers in each convolution block
- 14 blocks stacked one by one
- No pooling after each convolution
- 1 FC layer with dropout
- Data Augmentation on training data
- Batch Normalization between hidden and activation layers
- Dropout 50% before the dense layer to avoid overfitting
- Adam optimizer with learning rate = 0.001
- Batch size of train =32 and val = 8 
- Epochs : 50
