1) How fast did accuracy increase?
The training accuracy increased quickly, even within a single epoch. This shows
that the model can easily learn patterns from the clean CIFAR-10 images.

2) Did test accuracy track training accuracy?
Yes, the test accuracy increased along with the training accuracy. This means the
model generalized well on the test set when both training and test data came from
the same clean distribution.

3) Does this accuracy feel “trustworthy” given Block 1?
Not completely. Even though the accuracy is high on CIFAR-10, Block 1 showed that
this benchmark does not test real-world conditions like noise or blur. So the
accuracy alone does not guarantee that the model will perform reliably in real
world situations.
