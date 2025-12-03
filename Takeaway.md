# Key Takeaways 🎯
## These Experiments evaluated the impact of hardware acceleration, hyperparameter tuning, and model architecture on image classification performance.

📊
ResNet18 Outperformed Legacy Architectures ResNet18 achieved the highest validation accuracy (65%), proving that residual connections were necessary for feature learning on this dataset. In contrast, AlexNet and VGG16 suffered from stagnation, failing to improve beyond the baseline accuracy of 59%.

🏆
Stability Trumps Speed While larger learning rates (0.001) and batch sizes (64) offered faster initial computation, they caused the model to get stuck in local minima. A conservative configuration (Learning Rate 0.0001, Batch Size 32) was required to ensure consistent convergence.

⚡
Complexity Requires Time Data augmentation reduced accuracy by ~9% compared to the non-augmented baseline. This counter-intuitive result highlights that increasing data complexity (via rotation/flips) harms performance in short training runs (10 epochs) if the model is not given sufficient time to adapt.
