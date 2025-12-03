## These Experiments evaluated the impact of hardware acceleration, hyperparameter tuning, and model architecture on image classification performance.
# Key Takeaways

ResNet18 Outperformed Legacy Architectures ResNet18 achieved the highest validation accuracy (65%), proving that residual connections were necessary for feature learning on this dataset. In contrast, AlexNet and VGG16 suffered from stagnation, failing to improve beyond the baseline accuracy of 59%.

Stability Trumps Speed While larger learning rates (0.001) and batch sizes (64) offered faster initial computation, they caused the model to get stuck in local minima. A conservative configuration (Learning Rate 0.0001, Batch Size 32) was required to ensure consistent convergence.

Hardware Acceleration is Critical The CPU-only implementation failed to converge entirely (stuck at 51% accuracy). This demonstrates that GPU acceleration is not just a speed optimization, but a functional requirement for training deep learning models effectively.

Complexity Requires Time Data augmentation reduced accuracy by ~9% compared to the non-augmented baseline. This counter-intuitive result highlights that increasing data complexity (via rotation/flips) harms performance in short training runs (10 epochs) if the model is not given sufficient time to adapt.
