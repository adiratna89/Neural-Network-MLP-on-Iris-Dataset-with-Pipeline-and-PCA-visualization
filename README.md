
# 🌸 Neural Network (MLP) on Iris Dataset with Pipeline and PCA Visualization

<p align="center">
  <b>Multiclass classification of Iris flowers using a Multi-Layer Perceptron (MLP), ReLU activation, feature scaling through a Pipeline, and PCA-based 2D visualization.</b>
</p>

<p align="center">
  This mini project is part of my growing GitHub portfolio in Machine Learning and Neural Networks, where I focus on both implementation and clean project presentation.
</p>

---

## 🏷️ Project Badges

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Notebook">
  <img src="https://img.shields.io/badge/scikit--learn-FF9F1C?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/Neural%20Network-MLP-6A1B9A?style=for-the-badge" alt="MLP">
  <img src="https://img.shields.io/badge/PCA-Visualization-00897B?style=for-the-badge" alt="PCA">
  <img src="https://img.shields.io/badge/Project-Complete-success?style=for-the-badge" alt="Project Complete">
</p>

---

## ✨ Visual Story of the Project

<p align="center">
  <img src="Output_images/PCA visualization of Iris Dataset.png" alt="PCA Visualization of Iris Dataset" width="45%">
  <img src="Output_images/Confusion Matrix of MLP.png" alt="Confusion Matrix for MLP on Iris Dataset" width="45%">
</p>

<p align="center">
  <b>From 4-dimensional flower measurements ➜ neural network classification ➜ 2D PCA intuition.</b>
</p>

These visual outputs show both sides of the project:
- **PCA scatter plot** gives an intuitive view of class distribution in reduced dimensions.
- **Confusion matrix** shows how accurately the MLP model classified the three Iris species.

---

## 📌 What This Project Demonstrates

This project demonstrates how a **Multi-Layer Perceptron (MLP)** can be used for **multiclass classification** on the classic Iris dataset.

It combines:
- **Neural network modeling** using `MLPClassifier`
- **ReLU activation** for learning non-linear patterns
- **StandardScaler + Pipeline** for clean preprocessing
- **Confusion matrix and classification report** for evaluation
- **PCA visualization** for understanding class separation in 2D

This makes the notebook both a practical ML implementation and a visually interpretable mini-project.

---

## 📂 Project Snapshot

| Item | Details |
|---|---|
| **Problem Type** | Multiclass Classification |
| **Dataset** | Iris Flower Dataset |
| **Model Used** | Multi-Layer Perceptron (MLPClassifier) |
| **Activation Function** | ReLU |
| **Pipeline** | StandardScaler + MLPClassifier |
| **Dimensionality Reduction** | PCA (for visualization) |
| **Main Outputs** | Confusion Matrix, Classification Report, PCA Scatter Plot |
| **Environment** | Python, Jupyter Notebook, scikit-learn |

---

## 🌱 Dataset at a Glance

The **Iris dataset** is one of the most widely used datasets in machine learning for teaching and experimentation.

- **Total samples:** 150  
- **Features:** 4 numerical input features  
  - Sepal length  
  - Sepal width  
  - Petal length  
  - Petal width  
- **Target classes:** 3  
  - Setosa  
  - Versicolor  
  - Virginica  

Because the dataset is small, balanced, and well-structured, it is ideal for understanding classification algorithms and model visualization techniques.

---

## 🧠 Theory Corner

### 1) What is MLP?

A **Multi-Layer Perceptron (MLP)** is a feed-forward artificial neural network made up of:
- an **input layer**
- one or more **hidden layers**
- an **output layer**

Unlike simple linear models, MLP can learn **non-linear relationships** between features and target labels.  
That makes it useful for more flexible decision boundaries in classification tasks.

### 2) Why ReLU?

**ReLU (Rectified Linear Unit)** is one of the most commonly used activation functions in neural networks.

 **ReLU(x) = max(0, x)** 

It replaces negative values with zero and keeps positive values unchanged.  
This helps the network train efficiently and introduces the non-linearity needed to learn complex patterns.

### 3) Why PCA?

**PCA (Principal Component Analysis)** is a dimensionality reduction technique that transforms data into a smaller set of components while preserving as much variance as possible.

In this project, PCA is used **for visualization only**, not for model training.  
It helps reduce the 4-dimensional Iris data into 2 principal components so the class distribution can be plotted clearly in a scatter plot.

---

## 🧵 Notebook Workflow

The notebook follows a clean end-to-end ML workflow:

1. **Import required libraries**  
   - NumPy, Pandas, Matplotlib, Seaborn, scikit-learn

2. **Load the Iris dataset**  
   - Read the dataset from `sklearn.datasets`
   - Create a structured DataFrame for inspection

3. **Explore the data**  
   - Check features, classes, and target labels

4. **Split into training and testing sets**  
   - Prepare data for model evaluation

5. **Build a Pipeline**  
   - Apply `StandardScaler`
   - Train `MLPClassifier`

6. **Train the model**  
   - Fit the neural network on training data

7. **Evaluate the model**  
   - Accuracy score
   - Confusion matrix
   - Classification report

8. **Apply PCA for visualization**  
   - Reduce the feature space to 2 dimensions
   - Plot the class distribution

9. **Interpret outputs**  
   - Understand both model performance and data separability

---

## ⚙️ Model Configuration

The neural network is configured with the following main setup:

- **Hidden layer sizes:** `(10, 5)`
- **Activation:** `relu`
- **Solver:** `adam`
- **Maximum iterations:** `1000`
- **Random state:** `42`

Using a **Pipeline** ensures that feature scaling and model training happen in one clean workflow, which is especially useful for neural networks where scaling matters a lot.

---

## 📈 Results and Interpretation

### Confusion Matrix

The confusion matrix shows that the model performs very strongly on the test data.

<p align="center">
  <img src="Output_images/Confusion%20Matrix%20of%20MLP.png" alt="Confusion Matrix for MLP on Iris Dataset" width="420"/>
</p>

This indicates that the MLP classifier was able to correctly distinguish the three Iris species with excellent accuracy in this experiment.

### PCA Visualization

The PCA scatter plot projects the dataset into two principal components for visual understanding.

<p align="center">
  <img src="Output_images/PCA%20visualization%20of%20Iris%20Dataset.png" alt="PCA Visualization of Iris Dataset" width="420"/>
</p>


### Quick Interpretation

- **Setosa** appears clearly separated from the other two classes.
- **Versicolor** and **Virginica** show some overlap.
- This explains why some classes are naturally easier to classify than others.

---

## 🧩 What I Practiced in This Project

Working on this project helped me strengthen:

- Understanding of **MLP neural networks** for multiclass classification
- The role of **ReLU activation** in learning non-linear patterns
- The importance of **feature scaling** before neural network training
- Building a clean workflow using **scikit-learn Pipeline**
- Using **PCA** for visual explanation of structured data
- Presenting a machine learning mini-project in a more polished GitHub style

---

## 🚀 How to Run This Notebook

### 1️⃣ Clone the repository

```bash
git clone https://github.com/adiratna89/Neural-Network-MLP-on-Iris-Dataset-with-Pipeline-and-PCA-visualization.git
cd Neural-Network-MLP-on-Iris-Dataset-with-Pipeline-and-PCA-visualization
```

### 2️⃣ (Optional) Create and activate a virtual environment

```bash
python -m venv venv
```

**Windows**
```bash
venv\Scripts\activate
```

**macOS / Linux**
```bash
source venv/bin/activate
```

### 3️⃣ Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### 4️⃣ Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
Neural-Network-MLP-on-Iris-with-PCA-visualization-and-Pipeline.ipynb
```

---

## 📁 Repository Structure

```text
Neural-Network-MLP-on-Iris-Dataset-with-Pipeline-and-PCA-visualization/
│
├── Neural-Network-MLP-on-Iris-with-PCA-visualization-and-Pipeline.ipynb
├── README.md
├── LICENSE
└── Output_images/
    ├── Confusion-Matrix-MLP.jpg
    └── PCA-visualization-of-Iris-Dataset.jpg
```

This keeps the notebook, documentation, and output visuals clean and easy to navigate.

---

## 🔮 Future Improvements

Possible next upgrades for this project:

- Compare **MLP** with **Logistic Regression**, **SVM**, or **Random Forest**
- Perform **hyperparameter tuning** for hidden layers and learning settings
- Add **cross-validation** for more robust evaluation
- Visualize training loss or learning behavior
- Extend this project into a small **Neural Network mini-series** on GitHub

---

## 👤 Author

**Adiratna Kamble**  
Mumbai, Maharashtra, India

- GitHub: [github.com/adiratna89](https://github.com/adiratna89)
- LinkedIn: [www.linkedin.com/in/adiratna-kamble](https://www.linkedin.com/in/adiratna-kamble)

This project is part of my ongoing practice in **Python, Machine Learning, Deep Learning fundamentals, and GitHub project presentation**.

---

## 📄 License

This project is licensed under the **MIT License**.  
You are welcome to use or refer to this repository for learning purposes.

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a star!

Made with dedication and continuous learning by **Adiratna Kamble**

</div>
