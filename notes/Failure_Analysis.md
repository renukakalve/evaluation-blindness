1) What failed ? 
The model failed to generalize under realistic input corruptions. Although it
performed reasonably well on clean CIFAR-10 images, its performance collapsed
to random guessing when Gaussian noise was added.

2) Why it failed ? 
The model learned shortcut features that are effective only under clean conditions,
such as texture patterns, same background, image quality etc. Gaussian noise expose
these  fragile featurs, leaving the model without stable representations to rely on.

3) Why the benchmark didn’t warn us ?
CIFAR-10 tests models on clean images that are very similar to the trainig data.
Beacause the test data comes from the same conditions, the benchmark never checks
how the model behaves when the input chnages. As a result, it cannot tell whether
the model has learned strong, reliable features or weak features that only work in
clean distribution. This is why high accuracy on CIFAR-10 can give a false sense of
how well the model will perform in real world conditions.
