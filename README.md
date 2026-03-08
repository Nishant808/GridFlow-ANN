# GridFlow ANN: Predicting Combined Cycle Power Plant Output

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

## 📌 Project Overview
Efficiency is critical in power generation. This project implements a **Deep Learning regression model** using **PyTorch** to predict the net hourly electrical energy output (PE) of a Combined Cycle Power Plant. By analyzing environmental variables, the model provides highly accurate energy forecasts, aiding in grid stability and resource management.

## 📊 Dataset Description
The model is trained on **9,568 data points** collected from a Combined Cycle Power Plant over six years. The features represent hourly average environmental variables:
* **AT (Ambient Temperature):** In the range 1.81°C to 37.11°C.
* **V (Exhaust Vacuum):** In the range 25.36 to 81.56 cm Hg.
* **AP (Ambient Pressure):** In the range 992.89 to 1033.30 millibar.
* **RH (Relative Humidity):** In the range 25.56% to 100.16%.
* **PE (Energy Output):** The target variable (420.26 to 495.76 MW).

## 🛠️ Technical Architecture
I engineered a custom **Artificial Neural Network (ANN)** with the following specifications:
* **Framework:** PyTorch
* **Layers:** Multi-layer Perceptron (MLP) featuring:
    * Input layer (4 features)
    * Two hidden layers with **ReLU** activation functions
    * Single output neuron for regression
* **Optimizer:** Adam Optimizer for efficient gradient descent
* **Loss Function:** Mean Squared Error (MSE)
* **Preprocessing:** Robust feature scaling using `StandardScaler` to ensure optimal convergence.

## 🚀 Key Features & Results
* **Deep Learning Pipeline:** End-to-end implementation from raw CSV data to a trained PyTorch model.
* **Validation Strategy:** Utilized an 80/20 train-test split with a dedicated validation phase during training to monitor for overfitting.
* **Model Checkpointing:** Implemented a "Best Model" saving logic based on validation loss to ensure the most performant weights are preserved.
* **Performance Monitoring:** Visualized training vs. validation loss curves to verify model stability.

## 📁 Repository Structure
```text
├── Power_Plant_ANN.ipynb    # Main Jupyter Notebook with implementation
├── powerplant_data.csv      # Dataset (ensure this is present or linked)
├── best_model.pth           # Saved weights of the best performing model
└── README.md                # Project documentation
