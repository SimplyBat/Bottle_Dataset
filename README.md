It is stored in Google Drive and loaded directly through Colab.

---

### ✔ Model Architecture — AlexNet  

AlexNet is a classic CNN consisting of:

- 5 convolutional layers  
- ReLU activations  
- MaxPooling  
- Dropout  
- 3 fully connected classifier layers  

For transfer learning:

1. Load pretrained AlexNet  
2. Replace the classifier output layer with the number of dataset classes  
3. Fine-tune all layers  

AlexNet is chosen because:

- Fast to train  
- Lightweight  
- Good baseline architecture  
- Easy to compare with deeper models like VGG16 and ResNet18  

---

### ✔ Training Pipeline

Every experiment uses the same core training loop:

- Adam optimizer  
- Cross-entropy loss  
- DataLoader for batching  
- GPU acceleration (if available)  
- Automatic logging to W&B:  
  - training accuracy  
  - validation accuracy  
  - loss curves  
  - hyperparameters  
  - architecture type  

Each experiment is encapsulated inside a reusable function, making the notebook modular and clean.

---

## 📊 3. Experiments & Visualizations

Below are the four required experiments.

### ### **Experiment 1 — Batch Size Comparison**
Models trained with:
- **Batch size = 16**
- **Batch size = 64**

Visualization goals:
- Training accuracy curves
- Validation accuracy curves
- Training vs. validation loss

---

### ### **Experiment 2 — Learning Rate Comparison**
Models trained with:
- **LR = 0.001**
- **LR = 0.0001**

Visualization goals:
- Convergence rate differences  
- Overshooting / underfitting patterns  
- Stability of loss curves  

---

### ### **Experiment 3 — Data Augmentation**
Two training runs:
- No augmentation  
- With augmentation:
  - RandomRotation  
  - HorizontalFlip  
  - ColorJitter  

Visualization:
- Impact of augmentation on generalization  
- Reduction of overfitting  

---

### ### **Experiment 4 — Architecture Comparison**
Models evaluated:
- **AlexNet**  
- **VGG16**  
- **ResNet18**

Visualization:
- Compare accuracy across architectures  
- Compare compute time  
- Parameter count vs. accuracy  
- Deeper networks’ effect on performance  

---

## 📈 4. Results (Example Format)

You will insert your real W&B graphs here.

### Example Result Structure:

#### **Batch Size Results**
- Batch size 16 → higher accuracy, slower per-epoch  
- Batch size 64 → faster per-epoch, slightly lower accuracy  

#### **Learning Rate Results**
- LR 0.001 → quicker convergence  
- LR 0.0001 → more stable but slower  

#### **Data Augmentation Results**
- Augmentation improved test accuracy by X%  
- Reduced overfitting visible in loss curves  

#### **Architecture Comparison**
| Model     | Accuracy | Params | Notes |
|-----------|----------|--------|-------|
| AlexNet   | 84%      | 60M    | Good baseline |
| VGG16     | 90%      | 138M   | Very accurate but heavy |
| ResNet18  | 88%      | 11M    | Good trade-off |

(Replace with your actual results)

---

## 📝 5. Takeaways

- Hyperparameters significantly affect convergence speed and stability.  
- Data augmentation greatly improves generalization.  
- AlexNet is a strong baseline, but deeper architectures like ResNet and VGG perform better on complex datasets.  
- W&B experiment tracking makes comparisons simple and professional.  
- Running structured experiments helps replicate real ML pipeline workflows.  

---

## 📦 6. Project Structure (Recommended)
