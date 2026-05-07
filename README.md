# Neural Network (MLP) on Iris Dataset – Pipeline + PCA 🌸

Multiclass classification of Iris flowers using a **Multi-Layer Perceptron (MLP)** with **ReLU activation**, wrapped in a clean **scikit‑learn Pipeline** and supported by **PCA visualization** for better intuition.

This mini project continues my series of well-documented ML notebooks, focusing on neural networks plus dimensionality reduction on a classic dataset.

---

## 🔍 Visual Story

A quick look at what this project does.

<p align="center">
  <img src="Output_images/PCA-visualization-of-Iris-Dataset.jpg" alt="PCA visualization of Iris dataset" width="48%">
  <img src="Output_images/Confusion-Matrix-MLP.jpg" alt="Confusion Matrix of MLP model" width="48%">
</p>

These visuals show:
- How the three Iris species separate in 2D PCA space.
- How well the MLP classifier performs on the test set via the confusion matrix.

---

## 📘 What this project demonstrates

- Building a **neural network classifier (MLPClassifier)** for a **3‑class problem**.
- Using **ReLU** in hidden layers for non‑linear decision boundaries.
- Plugging preprocessing + model into a **scikit‑learn Pipeline** with `StandardScaler`.
- Evaluating performance using **accuracy**, **confusion matrix**, and **classification report**.
- Applying **PCA** for 2D visualization of the 4‑dimensional Iris dataset.

---

## 📂 Project Overview

- Problem type: **Multiclass classification** (Setosa, Versicolor, Virginica).
- Algorithm: **Multi‑Layer Perceptron (MLP)** neural network.
- Input features: Four numeric features from the Iris dataset.
- Preprocessing: Train‑test split + feature scaling using `StandardScaler` in a Pipeline.
- Extras: PCA scatter plot to visually understand how classes are separated.

---

## 🌱 Dataset – Iris Flower Dataset

- Features: **Sepal length**, **sepal width**, **petal length**, **petal width**.
- Target classes: **Setosa**, **Versicolor**, **Virginica**.
- Samples: **150** total (50 per class).
- Source: Available directly from `sklearn.datasets.load_iris()`.

---

## 🧠 Intuition: MLP, ReLU and PCA (Short Theory)

### Multi-Layer Perceptron (MLP)

An **MLP** is a feed‑forward neural network made of layers of neurons:  
input layer → one or more **hidden layers** → output layer.  
Each neuron takes a weighted sum of inputs, adds a bias and passes it through an activation function.  
Because of the hidden layers, MLPs can learn **non‑linear relationships** that simple linear models cannot capture.

### Why ReLU?

**ReLU (Rectified Linear Unit)** is defined as:

\[
\text{ReLU}(x) = \max(0, x)
\]

It keeps positive values as they are and clips negative values to zero.  
ReLU is very popular because it is simple, helps gradients flow better during training compared to sigmoid/tanh, and often leads to **faster and more stable training** in deeper networks.

### Why PCA in this project?

**PCA (Principal Component Analysis)** is a dimensionality reduction technique that finds new axes (principal components) which capture the maximum variance in the data.  
Here, PCA is used **only for visualization**: the 4‑dimensional Iris features are projected into 2 principal components so that all samples can be plotted in a single 2D scatter plot.  
This makes it easy to see which classes are well separated and where there is overlap between species.

---

## 🧮 Notebook Workflow

Main notebook:

- `Neural-Network-MLP-on-Iris-with-PCA-visualization-and-Pipeline.ipynb`

Inside the notebook you will find:

1. **Introduction & Objective**  
   - Brief problem statement and project goal.

2. **Data Loading & Exploration**  
   - Load Iris dataset using scikit‑learn.  
   - Create a pandas DataFrame and inspect features and target distribution.

3. **Train–Test Split & Pipeline Setup**  
   - Split data into training and testing subsets.  
   - Build a Pipeline with `StandardScaler` + `MLPClassifier`.

4. **MLP Model Training**  
   - Configure hidden layers, activation, solver and max iterations.  
   - Fit the Pipeline on training data.

5. **Evaluation**  
   - Predict on test set.  
   - Calculate accuracy.  
   - Generate confusion matrix and classification report.

6. **PCA Visualization**  
   - Apply PCA to the original features (2 components).  
   - Plot samples in PC1–PC2 space colored by class.

7. **Insights & Summary**  
   - Short interpretation of performance and PCA plot.

---

## 📈 Model Setup & Performance

- Hidden layer sizes: `(10, 5)`  
- Activation: **ReLU**  
- Solver: **Adam**  
- Max iterations: **1000**  
- Random state: **42**  

The model achieves strong performance on the test set (see confusion matrix above), correctly classifying the Iris species for this small, well‑separated dataset.

---

## 🧩 What I practiced in this project

- Designing a **neural network classifier** for a small, clean dataset.  
- Using **scikit‑learn Pipelines** to keep preprocessing and modeling together.  
- Understanding how **feature scaling** affects neural networks.  
- Combining **ML models with visual explanations** using PCA and confusion matrices.  
- Writing a consistent, GitHub‑ready README to document ML mini projects.

---

## ⚙️ How to run this notebook

1. **Clone the repository**

```bash
git clone https://github.com/adiratna89/Neural-Network-MLP-on-Iris-Dataset-with-Pipeline-and-PCA-visualization.git
cd Neural-Network-MLP-on-Iris-Dataset-with-Pipeline-and-PCA-visualization
```

2. **(Optional) Create and activate a virtual environment**

3. **Install required libraries**

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

4. **Open the notebook**

```bash
jupyter notebook "Neural-Network-MLP-on-Iris-with-PCA-visualization-and-Pipeline.ipynb"
```

5. Run the cells step by step to reproduce the results and plots.

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

This structure keeps the notebook, documentation and output images organized and easy to explore.

---

## 👤 Author

**Adiratna Kamble**

- GitHub: [adiratna89](https://github.com/adiratna89)
- LinkedIn: [linkedin.com/in/adiratna-kamble](https://www.linkedin.com/in/adiratna-kamble)

This project is part of my ongoing practice in Machine Learning and Neural Networks, as well as improving how I present projects on GitHub.

---

## 📄 License

This project is licensed under the **MIT License**.  
You are welcome to use or refer to this repository for learning purposes.
