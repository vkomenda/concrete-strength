This is an attempt to recreate the neural network predicting concrete strength development [1] based on the experimental dataset [2].

Unlike in [1], I didn't divide the whole dataset into 4 subsets based on local correlation. Instead, I pick a hundred experiments from the dataset at random and use those for validation of the trained network. All other experiments are used for training the network. It turns out that this simple randomised approach needs refinement because while the error rate does converge to a fixed limit, the predicted results still differ from the experimental results sometimes quite a bit. So it appears that preprocessing the dataset and finding local correlations should help improving the accuracy. This is currently a todo. Specifically, the coefficients of determination R^2 must be at least above 0.8 in order to match the accuracy of the NN in [1].

I use Python mostly for presentation reasons and because anybody can train this NN straight from GitHub with no local setup.

[1] I-Cheng Yeh, Modeling of strength of high performance concrete using artificial neural networks, Cement and Concrete Research, Vol. 28, No. 12, pp. 1797-1808 (1998).

[2] https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength
