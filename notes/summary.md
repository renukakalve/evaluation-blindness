1. Problem:
Modern vision models report high accuracy on standard benchmarks like CIFAR-10.
However, these benchmarks evaluate models only under clean and controlled
conditions. In real-world conditions like different backgrounds, noise, blur image
can drop the accuracy of the model. This raises the question of whether benchmark
accuracy truly reflects real-world reliability.

2. Setup:
To study this, I trained a RestNet-18 model on the CIFAR-10 dataset and evaluated
its performance on both the clean CIFAR-10 test set and the corrupted CIFAR-10-C
introduces realistic corruptions such as Gaussian noise while keeping the task and
labels unchanged. This setup allows us to test how models behave under distribution
shift without retraining.

3. Observation:
The model achieved high accuracy on CIFAR-10(46.67%) but dropped to 10% accuracy on
CIFAR-10-C with Gaussian noise, which is close to random guessing.

4. Insight:
This result shows that good performance on clean benchmarks does not guarantee
robustness under realistic conditions. The model appears to depend on fragile
surface level features that break when noise is introduced. Because CIFAR-10
evaluation does not test such conditions, it fails to reveal this weakness and
gives a false sense of reliability
