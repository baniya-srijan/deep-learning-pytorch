# deep-learning-pytorch

Learning deep learning by building, not just reading
Each folder contains hands-on experiments per concept.

## Progress
- [X] Feedforward Neural Networks — FashionMNIST
- [X] Convolutional Neural Networks (CNNs)
- [ ] Transformers

## Structure
01_feedforward_networks/ — FF nets, activation functions, training loops
02_cnns/                 — Conv layers, pooling, classic architectures
03_transformers/         — Attention, building GPT from scratch

## Key Projects

### FashionMNIST Classifier — Feedforward NN
Trained a 3-layer feedforward neural network on FashionMNIST from scratch in PyTorch.
Key finding: model struggles to distinguish visually similar categories 
(Shirt/T-shirt/Pullover/Coat). Next: CNN version to compare.
[View notebook](01_fashionmnist_feedforward_.ipynb)

### FashionMNIST Classifier — CNN
Built a 2-block CNN (Conv2d + ReLU + MaxPool2d) with a linear classifier head, 
trained on FashionMNIST with a proper train/validation/test split.

**Result:** 89.1% test accuracy — modest improvement over feedforward baseline.

**Key finding:** Hypothesized CNNs would resolve Shirt/T-shirt/Coat/Pullover 
confusion via localized feature detection (collars, button plackets, front 
openings). Improvement was smaller than expected — T-shirt classification 
improved modestly, but Shirt/Coat/Pullover confusion persisted. Suggests the 
model may lack sufficient depth to detect these fine-grained features, or 
these classes have genuinely overlapping visual signatures at 28x28 resolution.

**Next step:** Test with deeper architecture and stronger regularization to 
see if capacity was the limiting factor.

[View notebook](02_fashionmnist_cnns.ipynb)

### MNIST Classifier - CNN
Built and trained a convolution neural network to accurately classify handwritten digits. 
The project focused on implementing the complete CNN workflow including convolution layers, activations,
pooling, forward pass, loss computation, backward pass, optimization and validation
 
Result: 98.82% test accuracy - extremely well but showed a little sign of overfitting

Key finding: CNN was highly effective at learning spatial features from handwritten digits, thus achieving extremely
high performance from a simple architecture. 

[View notebook](cnn/mnist_cnns.ipynb)


### CIFAR-10 Classifier - CNN
Moving on from grayscale 28 * 28 dimension images to RGB images with size 32 * 32. CIFAR-10 contains 3 color channel images across 10 different classes. These RGB color channels contain more complex spatial pattern, thus making use of CNN more important.
Experiments would be done through how convolutional layers transform feature maps, how number of channels change throughout a network, effect of pooling on spatial dimensions, effect of Batch Normalization, Dropout and Data Augmentation followed by forward pass, loss computation, backward pass or back propagation, optimization and validation.

Result: 

Key finding: 




