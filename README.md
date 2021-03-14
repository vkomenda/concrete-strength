## Neural Network Modelling of Concrete Compressive Strength

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vkomenda/concrete-strength/blob/main/concrete.ipynb)

This is an attempt to recreate the neural network predicting concrete strength development [1] based on the experimental dataset [2].

Unlike in [1], I didn't divide the whole dataset into 4 subsets based on local correlation. Instead, I pick a random 3/4 of the experiments from the dataset and use those for validation of the trained network. All other experiments are used for training the network. It turns out that this simple randomised approach works with an additional hidden layer of a few neurons that model an experiment classifier whose purpose is to learn a few clusters within the training dataset. The error rate converges to a fixed limit. The predicted values are fairly correlated with the experimental results. The coefficients of determination R^2 are about 0.85 on the training set and about 0.8 on the validation set, which matches the accuracy of the NN in [1].

I use Python mostly for presentation reasons and because anybody can train this NN straight from GitHub with no local setup.

[1] I-Cheng Yeh, [Modeling of strength of high performance concrete using artificial neural networks](https://www.researchgate.net/publication/222447231_Modeling_of_Strength_of_High-Performance_Concrete_Using_Artificial_Neural_Networks_Cement_and_Concrete_research_2812_1797-1808), _Cement and Concrete Research_, Vol. 28, No. 12, pp. 1797-1808 (1998).

[2] https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength
