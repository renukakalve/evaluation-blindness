NOTE:-
After training for one epoch, the model reached 46.67% accuracy on the CIFAR-10 test set, showing that it had started 
to learn meaningful patterns from the data. However, when the same model was tested on CIFAR-10-C with Gaussian noise, its 
accuracy dropped to 10%, which is random guessing. This shows that even partially trained models that perform reasonably well 
on standard benchmarks can completely fail under realistic distribution shifts, and such failures are not revealed by clean test
accuracy.
