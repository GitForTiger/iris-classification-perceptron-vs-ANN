# Iris Classification: Perceptron vs. Artificial Neural Network

This repository presents a comparative study between a traditional Machine Learning model (**Single-Layer Perceptron**) and a Deep Learning model (**Artificial Neural Network**) for solving the multi-class classification problem using the famous Iris dataset.

The objective is to evaluate how a linear classifier compares against a multi-layer neural network when classifying flower species based on sepal and petal measurements.

---

## 🚀 Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Visualized feature distributions and relationships using Seaborn pairplots.
- Examined class separability among the three Iris species:
  - Setosa
  - Versicolor
  - Virginica

### 2. Data Preprocessing
- Label encoded target classes into numerical values.
- Standardized all input features using StandardScaler.
- Performed an 80:20 train-test split while maintaining class balance.

### 3. Model Development

#### Model 1: Perceptron
- Implemented using Scikit-Learn's `Perceptron` classifier.
- Trained for 1000 iterations.
- Acts as a linear decision boundary classifier.

#### Model 2: Artificial Neural Network (ANN)
- Built using TensorFlow/Keras Sequential API.
- Dense hidden layers with ReLU activation.
- Softmax output layer for multi-class classification.
- Optimized using Adam optimizer and categorical cross-entropy loss.

---

## 📊 Results

### Perceptron Classifier

The Perceptron achieved an overall accuracy of **90%** on the test dataset. It perfectly classified Setosa flowers but showed some confusion between Versicolor and Virginica due to their overlapping feature distributions.

**Classification Report**

```text
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        10
           1       1.00      0.70      0.82        10
           2       0.77      1.00      0.87        10

    accuracy                           0.90        30
   macro avg       0.92      0.90      0.90        30
weighted avg       0.92      0.90      0.90        30
```

### Artificial Neural Network (ANN)

The ANN successfully captured the non-linear relationships within the dataset and achieved a superior test accuracy of **96.67%**.

Key observations:
- Better generalization compared to the Perceptron.
- Improved classification of overlapping classes.
- Higher overall precision, recall, and F1-score.

---

## 📈 Performance Comparison

| Metric | Perceptron | ANN |
|----------|------------|------|
| Accuracy | 90.00% | 96.67% |
| Learning Type | Linear | Non-Linear |
| Complexity | Low | Moderate |
| Performance on Overlapping Classes | Moderate | Excellent |

---

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
- TensorFlow
- Keras

---

## 📂 Dataset

The project uses the Iris Flower Dataset containing:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

Target Classes:
- Setosa
- Versicolor
- Virginica

Dataset Source:
`sklearn.datasets.load_iris()`

---

## 🎯 Conclusion

The comparison demonstrates that while the Perceptron performs reasonably well on a relatively simple dataset, the Artificial Neural Network achieves higher accuracy by effectively learning non-linear decision boundaries. This highlights the advantage of deep learning models when dealing with complex classification tasks.

---
