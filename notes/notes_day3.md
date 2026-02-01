Observed Result:
The mode; achieved high accuracy on CIFAR-10 but dropped to 10% accuracy on CIFAR-10-C with Gaussian noise, which is close to random guessing.

Comparison with Prediction:
This 10% drop matches the prediction made by me in notes_day1.md that the model would fail under realistic corruptions such as noise.

Interpretation:
The result suggests that the model depends on fragile features that are not stable under distribution shift. CIFAR-10 evaluation failed to reveal this 
weakness, giving false sense of reliability.

Key Insight:
High in-distribution accuracy does not imply robustness or real-world reliability.

NOTE:-
After training for one epoch, the model reached 46.67% accuracy on the CIFAR-10 test set, showing that it had started to learn meaningful patterns from the data. However, when the same model was tested on CIFAR-10-C with Gaussian noise, its accuracy dropped to 10%, which is random guessing. This shows that even partially trained models that perform reasonably well on standard benchmarks can completely fail under realistic distribution shifts, and such failures are not revealed by clean test accuracy.

