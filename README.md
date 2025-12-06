## Problem & Motivation 🚀

Machine learning and deep learning have become powerful tools for image classification. However, real-world applications often require balancing **model accuracy**, **training speed**, and **generalization** — especially when working with limited data or computational resources.

For my project, I am working with a custom image dataset stored on my Google Drive (path: `/content/drive/MyDrive/dataset`).

- Which model architecture yields the best performance  
- How training parameters (like batch size and learning rate) affect convergence  
- Whether data augmentation helps improve generalization  
- The trade-offs between using a pretrained model vs. training from scratch  

This project aims to systematically explore these trade-offs across multiple axes:

- **Model architecture**: comparing classical convolutional models (AlexNet, VGG16, ResNet18)  
- **Pretraining vs. training from scratch**: evaluating if pretrained weights give a meaningful advantage on a small dataset  
- **Hyper-parameters**: testing different batch sizes and learning rates for stability and speed  
- **Data augmentation**: assessing if random transformations help against overfitting  

By doing this, the goal is to find a configuration that is **both accurate and practical** — producing high test accuracy while still training quickly and generalizing well.  
This is particularly useful for projects where compute is limited (e.g., personal laptops, minimal GPU), or for rapid prototyping and deployment.

In short: I want to understand *what works best — and why* — for my dataset, so that I can apply this knowledge to future classification tasks with confidence.
