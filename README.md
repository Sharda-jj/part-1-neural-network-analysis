# part-1-neural-network-analysis
# Part 1: Neural Network Fundamentals and Training Behavior Analysis

## Project Overview

This project focuses on building and analyzing a feed-forward neural network using a customer churn dataset. The main objective of this project was to understand how neural networks learn through forward propagation, backpropagation, loss calculation, and parameter updates.

The project was implemented using Python, TensorFlow/Keras, Pandas, Scikit-learn, Matplotlib, and Seaborn.

---

## Dataset Information

Dataset Used: Customer Churn Dataset

The dataset contains customer-related information such as subscription details, payment methods, contract type, and customer behavior. The target variable used for prediction is:

- `churn`
    - 0 → Customer did not churn
    - 1 → Customer churned

Dataset Source Link:

https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJlV-wBvUYs?usp=sharing

---

## Task 1: Dataset Understanding

The dataset was explored using Pandas functions to understand:

- Number of rows and columns
- Data types of features
- Missing values
- Statistical summary
- Distribution of target variable

A churn distribution chart was created to analyze class imbalance in the dataset.

### Observation

The dataset was highly imbalanced because most customers belonged to the non-churn category. Very few customers were labeled as churn customers.

---

## Task 2: Data Preprocessing

The following preprocessing steps were performed:

- Checked and handled missing values
- Encoded categorical columns using Label Encoding
- Removed unnecessary columns like customer_id
- Standardized numerical features using StandardScaler
- Split dataset into training and testing sets using 80:20 ratio

---

## Task 3: Neural Network Model Building

A feed-forward neural network was created using TensorFlow/Keras Sequential API.

### Model Architecture

- Input Layer
- Hidden Layer 1 → 16 neurons, ReLU activation
- Hidden Layer 2 → 8 neurons, ReLU activation
- Output Layer → 1 neuron, Sigmoid activation

### Optimizer and Loss Function

- Optimizer: Adam
- Loss Function: Binary Crossentropy

---

## Task 4: Training and Evaluation

The model was trained using training data and evaluated on testing data.

### Evaluation Techniques Used

- Training Accuracy
- Validation Accuracy
- Testing Accuracy
- Confusion Matrix
- Classification Report

### Observation

The model achieved high testing accuracy, but due to class imbalance, it struggled to correctly predict churn customers. Precision, recall, and F1-score were important evaluation metrics in this project.

---

## Task 5: Hyperparameter Experimentation

Three different experiments were performed by changing:

- Number of hidden layers
- Number of neurons
- Activation functions
- Learning rate
- Batch size
- Number of epochs

### Best Performing Model

Experiment 2 performed best with:
- 2 hidden layers
- 32 and 16 neurons
- ReLU activation
- 30 epochs

---

## Task 6: Final Reflection

This project helped in understanding important neural network concepts such as:

- Role of weights and biases
- Importance of activation functions
- Effect of learning rate on model training
- Underfitting and overfitting behavior
- Impact of imbalanced datasets on prediction performance

The project also showed that accuracy alone is not always enough for evaluating classification models.

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras

---

## Repository Structure

```bash
part-1-neural-network-analysis/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
└── results/
    ├── model_comparison_table.csv
    └── evaluation_outputs.png
```

---

## Conclusion

This project provided practical understanding of neural network fundamentals and model training behavior. Different hyperparameter experiments helped analyze how model architecture and learning configurations affect prediction performance.
