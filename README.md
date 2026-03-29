# 🧠 Handwritten Digit Classification using CNN-SVM Hybrid Model

## 📌 Overview
This project implements a hybrid machine learning model combining Convolutional Neural Networks (CNN) and Support Vector Machine (SVM) for handwritten digit classification using the MNIST dataset.

The CNN is used as a feature extractor, while the SVM acts as a classifier on top of the learned deep features, improving generalization performance.

---

## ❓ Problem Statement
Handwritten digit recognition is a fundamental problem in computer vision with applications in banking, postal systems, and document digitization.

The objective is to classify grayscale images (28×28 pixels) into one of 10 digit classes (0–9).

---

## 📂 Dataset
- Dataset: MNIST  
- Training samples: 60,000  
- Testing samples: 10,000  
- Image size: 28 × 28 (grayscale)  
- Classes: 10 (digits 0–9)

---

## 🧹 Data Preprocessing
- Normalized pixel values to range [0, 1]  
- Reshaped input to include channel dimension (28×28×1)  
- Converted labels into categorical format for CNN training  

---

## 🧠 Model Architecture

### 🔹 CNN (Feature Extractor)
- Conv2D (32 filters) + ReLU  
- MaxPooling  
- Conv2D (64 filters) + ReLU  
- MaxPooling  
- Flatten layer  
- Dense layer (128 neurons)  
- Dropout (0.5) for regularization  

The CNN learns hierarchical spatial features from images.

---

### 🔹 Feature Extraction
- Extracted **128-dimensional feature vectors** from the CNN (before final classification layer)  
- These features represent high-level image patterns  

---

### 🔹 SVM Classifier
- Linear kernel SVM trained on extracted features  
- Handles classification with better margin optimization  

---

## 🔀 Workflow
1. Load and preprocess MNIST dataset  
2. Train CNN model on image data  
3. Extract deep features from CNN  
4. Train SVM classifier on extracted features  
5. Evaluate model performance  

---

## 📊 Results
- Hybrid CNN-SVM model achieves high classification accuracy on test data  
- CNN captures complex image features  
- SVM improves classification boundaries and generalization  

---

## 📈 Key Insights
- Hybrid models combine strengths of deep learning and traditional ML  
- CNN alone performs well, but SVM enhances decision boundaries  
- Feature extraction reduces dimensional complexity for SVM  

---

## 🛠️ Technologies Used
- Python  
- NumPy  
- TensorFlow / Keras  
- Scikit-learn  
- Joblib  

---

## 📁 Project Outputs
- Trained CNN feature extractor model (`featureextractor.h5`)  
- Trained SVM model (`svm_model.pkl`)  

---

## 🚀 Conclusion
This project demonstrates an effective hybrid approach by combining CNN for feature extraction and SVM for classification. It highlights how deep learning and classical machine learning can work together to achieve robust performance in image classification tasks.

---

## 🔮 Future Improvements
- Use non-linear SVM kernels (RBF)  
- Hyperparameter tuning for both CNN and SVM  
- Try advanced architectures (ResNet, VGG)  
- Deploy as a web application  
- Apply to real-world handwritten datasets  

---

## 👨‍💻 Author
Shashank
