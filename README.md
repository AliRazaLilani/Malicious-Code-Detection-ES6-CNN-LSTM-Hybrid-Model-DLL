# **Malicious-Code-Detection-ES6-CNN-LSTM-Hybrid-Model-DLL**

A CNN-LSTM hybrid model for detecting malicious webpage content and advertisements. This repository provides a comprehensive implementation for classifying web content as safe or malicious, aimed at protecting against phishing attacks and malicious advertisements.

## **Table of Contents**
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## **Introduction**
Phishing and malicious web content pose significant threats to users and platforms. This repository implements a **CNN-LSTM hybrid model** to classify webpage content as benign or malicious, using a combination of structured and unstructured features.

### **Scenarios Covered**
1. **Detecting phishing webpages** that mimic legitimate websites to steal sensitive information.
2. **Detecting malicious advertisements** that embed harmful scripts in webpage content.

---

## **Features**
- Exploratory Data Analysis (EDA) for understanding webpage content.
- Preprocessing techniques like tokenization, padding, and feature extraction.
- Implementation of a CNN-LSTM hybrid model to classify webpages.
- Support for structured features like JavaScript length, URL length, and obfuscation metrics.
- Visualization of results, including training history, confusion matrices, and evaluation metrics.

---

## **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/PhishingDetection-CNN-LSTM-Hybrid.git
   cd PhishingDetection-CNN-LSTM-Hybrid
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate    # Linux/Mac
   venv\Scripts\activate       # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Ensure you have Jupyter Notebook or JupyterLab installed:
   ```bash
   pip install notebook
   ```

---

## **Usage**

### **1. Running the Model**
- Open the `Thesis2_CNN_LSTM.ipynb` notebook in Jupyter Notebook or JupyterLab.
- Follow the cells sequentially to:
  1. Perform data preprocessing.
  2. Train the CNN-LSTM hybrid model.
  3. Evaluate the model's performance.

### **2. Training Your Own Dataset**
- Replace the example datasets with your own CSV files containing `content` and `label` columns.
- Ensure that your dataset follows the same preprocessing pipeline.

### **3. Visualization**
- View training accuracy and loss plots.
- Analyze the confusion matrix and classification reports.

---

## **Dataset**
This repository uses a dataset of malicious and benign webpages. The data contains:
- **Unstructured Features:** Webpage content (e.g., HTML, JavaScript).
- **Structured Features (optional):** URL length, JavaScript obfuscation metrics.

### **Dataset Format**
| Content                | Label     |
|------------------------|-----------|
| `<HTML content>`       | good/bad  |

Replace the dataset path in the notebook to train the model on your data.

---

## **Model Architecture**
The CNN-LSTM hybrid model consists of the following layers:
1. **Embedding Layer:** Converts tokenized text into dense vectors.
2. **Conv1D Layer:** Extracts spatial patterns like n-grams from the text.
3. **MaxPooling1D Layer:** Reduces feature dimensionality.
4. **LSTM Layer:** Captures temporal dependencies in the text.
5. **GlobalMaxPooling1D:** Aggregates outputs into a fixed-size representation.
6. **Dense Layers:** Performs final classification.

---

## **Results**
The model achieves high accuracy in detecting phishing and malicious content:
- **Accuracy:** >90%
- **Precision, Recall, F1 Score:** Detailed metrics are available in the notebook.

### **Visual Outputs**
- Training accuracy and loss curves.
- Confusion matrix showing model predictions.

---

## **Contributing**
Contributions are welcome! If you have ideas to improve this repository:
1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Added new feature"
   ```
4. Push the branch and submit a pull request:
   ```bash
   git push origin feature-name
   ```

---

## **License**
This project is licensed under the [MIT License](LICENSE).

---

## **Acknowledgements**
- The dataset used for training is based on publicly available malicious and benign webpage datasets.
- Special thanks to the developers of TensorFlow and Keras for their incredible tools.

---

## **Author**
**Ali Raza**
- Senior Software Engineer and Consultant
- Expertise: Machine Learning, Backend Development, and Web Security
- [LinkedIn Profile](https://www.linkedin.com/in/ali-raza-lilani-2729b9aa/)  
- [GitHub Profile](https://github.com/AliRazaLilani)

---

### **Keywords**
- Phishing Detection
- CNN-LSTM Hybrid Model
- TensorFlow/Keras
- Malicious Webpages
- Ad Security
- Feature Extraction
- Web Security
