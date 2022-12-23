# IntroML-Tensorflow

Notes:

Sequential: That defines a SEQUENCE of layers in the neural network

Flatten: Remember earlier where our images were a square, when you printed them out? Flatten just takes that square and turns it into a 1 dimensional set.

Dense: Adds a layer of neurons

Each layer of neurons need an activation function to tell them what to do. There's lots of options, but just use these for now.

Relu effectively means "If X>0 return X, else return 0" -- so what it does it it only passes values 0 or greater to the next layer in the network.

Softmax takes a set of values, and effectively picks the biggest one, so, for example, if the output of the last layer looks like [0.1, 0.1, 0.05, 0.1, 9.5, 0.1, 0.05, 0.05, 0.05], it saves you from fishing through it looking for the biggest value, and turns it into [0,0,0,0,1,0,0,0,0] -- The goal is to save a lot of coding

Epoch: A full pass over all of your training data.

Loss: A scalar value that we attempt to minimize during our training of the model. The lower the loss, the closer our predictions are to the true labels.
This is usually Mean Squared Error (MSE) as David Maust said above, or often in Keras, Categorical Cross Entropy

Removing the Flatten function will result in an error about the shape of the data. n layers of n neurons is not feasible, so it makes more sense to "flatten"
the n,n images to a n*n x 1 (ex: 28 x 28 will be flattened into a 784 x 1)

When looking at the second Dense function, the first number is the number of neurons in the last layer. This number needs to match up with the number of classes
that you are classifying for. (in first.ipynb, we have 10 neurons in the final layer)
