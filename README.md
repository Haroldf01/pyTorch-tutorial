To begin, we'll, at the very least, want to start calculating accuracy, and loss, at the epoch (or even more granular) level.

Not only this, but we'll want to calculate two accuracies:

1. In-sample accuracy: This is the accuracy on the data we're actually feeding through the model for training. This is the data that we're "fitting" against.
2. Out-of-sample accuracy: This is the accuracy on data that we've set aside that the model will never see/fit against.

In general, we expect in-sample accuracy to be higher than out-of-sample accuracy. You may also hear "out of sample" accuracy referred to as "validation accuracy." While we expect validation/out-of-sample accuracy to be a bit worse than the in-sample accuracy, we want to track that delta. Something like 5-10% accuracy difference is pretty common, but as this delta grows, it usually signals to us that our model is beginning to "overfit" (the neural network is just memorizing the data and changing weights to work only for the training data, rather than generally understanding the data).

You can also track in and out of sample loss. You will often be able to spot both losses decline to a point, and then out of sample loss begins to arc and curve back upwards. This is usually a sign that you've gotten the most out of your model's training.