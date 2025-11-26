## Technical Approach with AlexNet ⚙️

To evaluate the performance of classical convolutional networks on my dataset (`/content/drive/MyDrive/dataset`), I implemented and trained **AlexNet**, one of the earliest high-impact deep learning architectures for image classification. Although AlexNet is not state-of-the-art today, it provides a strong baseline and is ideal for comparing training behaviors under different conditions.

### 🧱 Model Architecture (AlexNet Overview)

AlexNet consists of:
- **5 convolutional layers** with ReLU activations  
- **Local Response Normalization (LRN)** after early layers  
- **Max-pooling layers**  
- **3 fully connected layers**, ending with a classification layer  
- **Dropout** in the fully connected layers to reduce overfitting  

The model is much lighter than modern networks like ResNet or EfficientNet, which makes it easier to train on Google Colab while still being expressive enough to capture complex visual patterns.

### 🔧 Implementation Strategy

1. **Importing Pretrained AlexNet**  
   I used `torchvision.models.alexnet(pretrained=True)` to start from ImageNet weights when testing transfer learning.  
   I also trained AlexNet **from scratch** for comparison.

2. **Customizing the Classifier**  
   Since my dataset has a different number of classes than ImageNet, I replaced the final layer:  
   ```python
   model.classifier[6] = nn.Linear(4096, num_classes)
