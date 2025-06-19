# 😴 KNN from Scratch

## 📌 Project Overview

This project implements the K-Nearest Neighbors (KNN) algorithm **from scratch** in Python, without using ready-made machine learning libraries (like scikit-learn) for the core algorithm. The code was developed in a Jupyter Notebook and tested on several classic datasets.

## 🧠 What is KNN?

K-Nearest Neighbors (KNN) is a simple yet powerful supervised machine learning algorithm used for classification and regression. It operates on the principle that similar objects are close to each other in the feature space.

**Basic principle**: To classify a new data point, the algorithm finds the K closest points in the training set and performs a "majority vote" among these neighbors to determine the class of the new point.

## 🛠️ Implemented Features

1. **Euclidean distance calculation**: Implemented to measure similarity between data points.
2. **Data standardization**: Normalization of features to zero mean and unit variance.
3. **KNN classification**: Complete implementation of the classification algorithm.
4. **Performance evaluation**: Testing the model with different K values and evaluation metrics.
5. **Visualization**: Comparative plots of accuracy, precision, recall, and F1-score for different K values.

## 📊 Datasets Used

The code tests the KNN algorithm on four datasets:

1. **Iris Dataset**: Small dataset with 3 classes of flowers (150 samples).
2. **Wine Dataset**: Wine data with 13 features and 3 classes.
3. **Digits Dataset**: Handwritten digit images (8x8 pixels, 10 classes).
4. **Fashion MNIST**: Clothing images (28x28 pixels, 10 classes) - using only 10% of the data for performance reasons.

## ⚙️ How the Code Works

1. **Preprocessing**:
   - Data standardization (important for distance-based algorithms).
   - Splitting data into training (70%) and test (30%) sets.

2. **Training and Prediction**:
   - For each K value in the specified range (3 to 15 by default):
     - The model stores the training data (KNN is a "lazy" algorithm - no traditional training occurs).
     - Makes predictions by calculating distances to all training points.
     - Selects the K nearest neighbors and performs majority voting.

3. **Evaluation**:
   - Calculates performance metrics (accuracy, precision, recall, F1-score) for each K.
   - Generates plots comparing performance on training and test sets.

## 🚀 Possible Extensions  

If you want to improve this project:  

* Add more distance metrics (Manhattan, Chebyshev, etc.)  
* Support weighted voting (closer neighbors count more)  
* Automatically find the best *K* using cross-validation  
* Adapt the algorithm for regression (predicting numbers)  
* Build a simple web demo with Streamlit  

These extensions would make the implementation more robust and versatile while maintaining the educational value of the from-scratch approach.

## ⏱️ Performance

The KNN algorithm implemented from scratch is computationally intensive, especially for large datasets, as it requires calculating distances between all points. Fashion MNIST (even with 10% of the data) may take several minutes to run, depending on hardware.

## 📜 License

This project is licensed under the MIT License.

---

Made by [pdrzxzz](https://github.com/pdrzxzz) | Computer Science Student 🎓
