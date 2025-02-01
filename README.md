# Image Augmentation & MNIST Classification with TensorFlow  

## 📌 Project Overview  
This project demonstrates the impact of **image augmentation techniques** on model performance by training a neural network on the MNIST dataset. Key comparisons include model accuracy and generalization with/without augmentation.  

**Dataset**: MNIST.  
**Goal**: Evaluate how augmentation improves robustness and reduces overfitting in general Image classification tasks.

---

## 🚀 Key Features  
1. **Image Augmentation Pipeline**:  
   - Adjustments: Horizontal flipping, grayscale conversion, saturation, brightness, rotation, and cropping.  
   - Real-time augmentation using TensorFlow’s `tf.image` module.  
2. **Optimized Dataset Preparation**:  
   - Normalization (`[0, 255]` → `[0, 1]`), caching, shuffling, and prefetching for GPU efficiency.  
3. **Deep Learning Model**:  
   - Architecture: 2 hidden layers (4096 neurons each, ReLU activation), output layer (10 neurons, softmax).  
   - Trained separately on augmented vs. raw data for performance comparison.  

---

## 🔍 Findings  
- **Augmented Model**:  
  - **Accuracy**: 94.2% (train) vs. 95.8% (test)  
  - **Runtime**: 3s/epoch | **Memory**: 4GB (NVIDIA GPU).  
- **Baseline (No Augmentation)**:  
  - **Accuracy**: 99.1% (train) vs. 94.4% (test) 
  - **Runtime**: 3s/epoch | **Memory**: 3.8GB (NVIDIA GPU). 
- **Conclusion**:  
  - Augmentation improved test generalization by 1.4% while adding minimal computational overhead.  

---

## 🛠 System Requirements  
### Dependencies  
- Python 3.8+  
- Libraries: `tensorflow`, `tensorflow-datasets`, `matplotlib`, `Pillow`  
- Hardware: GPU with cuDNN support (recommended)

---

## 📄 License  
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
