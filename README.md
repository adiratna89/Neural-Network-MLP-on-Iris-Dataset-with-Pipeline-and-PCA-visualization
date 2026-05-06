# Neural Network (MLP) on Iris Dataset with Pipeline and PCA Visualization

This project demonstrates multiclass classification on the famous Iris dataset using a **Multi-Layer Perceptron (MLP)** model with **ReLU activation**, combined with a **scikit-learn Pipeline** for preprocessing and **Principal Component Analysis (PCA)** for 2D visualization.

It combines neural network modeling, preprocessing, evaluation, and visualization in a clean end-to-end machine learning workflow.

---

## Project Highlights

- Multiclass classification using **MLP Classifier**
- Feature scaling with **StandardScaler** inside a **Pipeline**
- Dimensionality reduction using **PCA** for 2D visualization
- Performance evaluation using confusion matrix and classification report

## Table of Contents

- [Project Overview](#project-overview)
- [Objective](#objective)
- [About the Dataset](#about-the-dataset)
- [Theory Background](#theory-background)
  - [What is MLP?](#what-is-mlp)
  - [Why ReLU Activation?](#why-relu-activation)
  - [Why PCA?](#why-pca)
- [Tools and Libraries Used](#tools-and-libraries-used)
- [Project Workflow](#project-workflow)
- [Model Details](#model-details)
- [Results](#results)
- [Output Visualizations](#output-visualizations)
- [How to Run the Project](#how-to-run-the-project)
- [Key Learnings](#key-learnings)
- [Conclusion](#conclusion)

---

## Project Overview

The Iris dataset is one of the most well-known datasets in machine learning and is commonly used to demonstrate classification techniques. In this project, an MLP neural network is trained to classify iris flowers into three species based on four numerical input features.

To make the workflow more robust and professional, feature scaling is handled through a **Pipeline** using `StandardScaler`, while **PCA** is used to reduce the dataset into two principal components for visualization.

---

## Objective

The main objective of this project is to classify Iris flower species using a neural network model and to understand the dataset visually through dimensionality reduction.

This project focuses on:

- Building a multiclass classification model using **MLPClassifier**
- Applying **ReLU activation** in the hidden layers
- Using a **Pipeline** for clean preprocessing and model training
- Evaluating model performance using accuracy, confusion matrix, and classification report
- Visualizing the dataset in 2D using **PCA**

---

## About the Dataset

The Iris dataset is a classic multiclass classification dataset available in `sklearn.datasets`.

### Dataset Information

- Total samples: **150**
- Total features: **4 numerical features**
- Total target classes: **3**
  - Setosa
  - Versicolor
  - Virginica

### Input Features

- Sepal length
- Sepal width
- Petal length
- Petal width

The dataset is balanced and relatively simple, which makes it ideal for understanding machine learning workflows and model behavior.

---

## Theory Background

### What is MLP?

**MLP (Multi-Layer Perceptron)** is a type of artificial neural network made up of multiple layers of interconnected neurons. It typically includes an input layer, one or more hidden layers, and an output layer.

An MLP learns complex patterns in data by applying weights, biases, and activation functions through these layers. Unlike simple linear models, MLP can capture nonlinear relationships, which makes it useful for many classification problems.

### Why ReLU Activation?

**ReLU (Rectified Linear Unit)** is one of the most commonly used activation functions in neural networks. It returns the input directly if it is positive; otherwise, it returns zero.

ReLU helps neural networks learn nonlinear patterns more efficiently and is computationally simple. It also reduces some of the training difficulties seen in older activation functions like sigmoid and tanh.

### Why PCA?

**PCA (Principal Component Analysis)** is a dimensionality reduction technique used to transform high-dimensional data into a smaller number of components while preserving as much variance as possible.

In this project, PCA is not used for training the model. Instead, it is used for **visualization**, so the four-dimensional Iris data can be represented in a two-dimensional plot. This helps in understanding class separation and data distribution.

---

## Tools and Libraries Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**

### Scikit-learn Components Used

- `load_iris`
- `train_test_split`
- `StandardScaler`
- `Pipeline`
- `MLPClassifier`
- `accuracy_score`
- `confusion_matrix`
- `classification_report`
- `PCA`

---

## Project Workflow

The project follows a step-by-step machine learning workflow:

1. Import required libraries
2. Load the Iris dataset
3. Define features and target
4. Create a DataFrame for inspection
5. Perform basic exploratory data analysis
6. Split the dataset into training and testing sets
7. Build an MLP pipeline using `StandardScaler` and `MLPClassifier`
8. Train the model
9. Evaluate predictions using classification metrics
10. Apply PCA to reduce data into 2 dimensions
11. Visualize class distribution in PCA space

This structured workflow makes the notebook easy to understand and suitable for learning as well as portfolio presentation.

---

## Model Details

The classification model is built using **MLPClassifier** inside a scikit-learn Pipeline.

### Model Configuration

- Hidden layer sizes: **(10, 5)**
- Activation function: **ReLU**
- Solver: **Adam**
- Maximum iterations: **1000**
- Random state: **42**

### Why use Pipeline?

A Pipeline helps combine preprocessing and modeling into a single clean workflow. In this project, `StandardScaler` standardizes the features before they are passed to the neural network.

This is especially important for neural networks because feature scaling helps training become more stable and effective.

---

## Results

The trained MLP model achieved strong classification performance on the test set.  
The confusion matrix shows correct predictions across all three Iris classes in this run, indicating that the model learned the class patterns effectively.

### Evaluation Methods Used

- Accuracy score
- Confusion matrix
- Classification report

The model correctly classified the Iris flower species with high performance, and the confusion matrix shows that predictions were very accurate for all three classes.

---

## Output Visualizations

### Confusion Matrix

The confusion matrix provides a class-wise view of prediction performance. It helps show whether the model is confusing one class with another.

![Confusion Matrix](Output_images/Confusion Matrix (MLP).png)

### PCA Visualization

The PCA scatter plot projects the four-dimensional dataset into two principal components. This allows us to visually observe how the three classes are distributed.

![PCA Visualization](Output_images/PCA visualization of Iris Dataset.png)

### Interpretation of PCA Plot

- **Setosa** appears clearly separated from the other two classes
- **Versicolor** and **Virginica** show some overlap
- This visual pattern helps explain why classification between some classes can be more challenging than others in general

---

## Repository Structure

- `Neural Network - MLP on Iris with PCA visualization and Pipeline.ipynb` — main notebook
- `Output_images/` — saved output plots used in the README
- `README.md` — project documentation

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/adiratna89/Neural-Network-MLP-on-Iris-Dataset-with-Pipeline-and-PCA-visualization.git
```

### 2. Open the project folder

```bash
cd Neural-Network-MLP-on-Iris-Dataset-with-Pipeline-and-PCA-visualization
```

### 3. Install required libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn notebook
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open and run the notebook

Open the notebook file and run all cells step by step.

---

## Key Learnings

This project helped strengthen understanding of:

- Neural network-based classification using **MLPClassifier**
- The role of **ReLU activation** in learning nonlinear patterns
- The importance of **feature scaling** in machine learning pipelines
- Clean preprocessing and modeling using **Pipeline**
- Model evaluation using confusion matrix and classification report
- Visual interpretation of high-dimensional data using **PCA**

---

## Future Improvements

- Compare MLP with Logistic Regression or SVM
- Tune hidden layers and hyperparameters
- Apply the same workflow to a more complex dataset

---

## Conclusion

This project presents a complete and beginner-friendly machine learning workflow using the Iris dataset. By combining **MLP**, **ReLU**, **Pipeline**, and **PCA**, it demonstrates not only model training and evaluation but also how visualization can improve understanding of the dataset.

Overall, this mini-project is a strong example of applying neural networks to a multiclass classification problem in a structured and interpretable way.
