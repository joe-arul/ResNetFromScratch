# ResNetFromScratch
Training various CNN architectures on the CIFAR10 dataset (/notebooks/ResNetFromScratch.ipynb)

### Summary of Results :
- VGG16 architecture (15 layers, 75 training epochs) achieved 90.05% accuracy on test data with loss 0.317.
- ResNet architecture (48 layers, 35 training epochs) achieved 82% accuracy on training before I ran out of compute units and lost access to the runtime and the model.

### Final Model Architecture :

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