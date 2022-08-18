# p3-datascience-2022

## Example Notebook.

The end goal of the model is to be able to determine wearables based on a greyscale image of 28 x 28.

The data in `data` folder is obtained from [here with the download links in the README](https://github.com/zalandoresearch/fashion-mnist).

The data is then extracted using `gzip` library which is built-in to Python and follows the data byte format as mentioned [in this site](http://yann.lecun.com/exdb/mnist/) for MNIST handwriting.

Please make sure you fully ran the `make-model.ipynb` notebook first before jumping to `use-model.ipynb` because the needed files are not there when the repository is cloned. Do note that the second last notebook cell in `make-model.ipynb` can take a while to finish depending on your computer specs.

This notebook setup comes with tensorboard support.

Run
```
tensorboard --logdir output/logs/
```
to see output logs of model performance. You can run the command before running `make-model.ipynb` notebook and watch your model performance as your model trains. Important part to look at is the `epoch_loss` and analyse the shapes of the graphs.

It is not recommended to run both notebooks at the same time. There is a chance that you would encounter an error message like this (for NVIDIA GPUs) if doing so:
```
Attempting to perform BLAS operation using StreamExecutor without BLAS support
```
Ensure only one of those notebooks run at a time to avoid this error.

## Good learning resources for Neural Network:

1. [Choosing activation functions.](https://machinelearningmastery.com/choose-an-activation-function-for-deep-learning/)

2. [Determine the number of layers and neurons in the hidden layer.](https://medium.com/geekculture/introduction-to-neural-network-2f8b8221fbd3)

3. [Learning Rate to reduce final epoch loss.](https://towardsdatascience.com/understanding-learning-rates-and-how-it-improves-performance-in-deep-learning-d0d4059c1c10)

4. [When the model is overfitted or underfitted.](https://www.v7labs.com/blog/overfitting)

## Credits

1. Fashion-MNIST: a Novel Image Dataset for Benchmarking Machine Learning Algorithms. Han Xiao, Kashif Rasul, Roland Vollgraf. [arXiv:1708.07747](arxiv.org/abs/1708.07747)
