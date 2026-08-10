# Wearable Stress Detection Using ECG Signals

This project explores automated stress detection using physiological signals from wearable sensors. The goal is to classify a person's physiological state as **baseline or stress** using ECG data and compare different machine learning and deep learning approaches.

## Dataset

The project uses the **WESAD (Wearable Stress and Affect Detection) dataset**, a publicly available dataset containing physiological and motion data collected using wearable devices.

For this analysis, ECG signals are used to distinguish between:

* Baseline
* Stress

The ECG data is segmented into fixed time windows and normalized before model training.

## Project Workflow

The project includes:

* ECG signal extraction and preprocessing
* Baseline and stress label preparation
* Signal segmentation into time windows
* Data normalization and downsampling
* Train, validation, and test splitting
* Class imbalance handling
* Machine learning model training
* Deep learning model development
* Model performance comparison

## Models Used

Several machine learning and deep learning models were evaluated, including:

* Support Vector Machine (SVM)
* Random Forest
* AdaBoost
* K-Nearest Neighbors (KNN)
* XGBoost
* Bagging
* Artificial Neural Network (ANN)
* LSTM
* Bi-LSTM
* 1D-CNN
* CDIL-CNN
* CNN-BiLSTM-Attention

## Best Performing Model

The **CDIL-CNN** achieved the strongest overall performance in the experiments.

Key results:

* Test Accuracy: **98.55%**
* F1 Score: **0.9799**
* ROC-AUC: **0.9968**
* Precision: **0.9799**
* Recall: **0.9799**
* Cohen's Kappa: **0.9685**

The model correctly classified the majority of ECG test windows while maintaining strong performance across both baseline and stress classes.

## Selected Model Comparison

| Model                | Test Accuracy |   F1 Score |    ROC-AUC |
| -------------------- | ------------: | ---------: | ---------: |
| CDIL-CNN             |    **98.55%** | **0.9799** | **0.9968** |
| Random Forest        |        96.37% |     0.9481 |     0.9925 |
| CNN-BiLSTM-Attention |        95.88% |     0.9424 |     0.9911 |
| Bagging              |        95.40% |     0.9343 |     0.9861 |
| XGBoost              |        94.92% |     0.9283 |     0.9829 |
| SVM                  |        93.95% |     0.9141 |     0.9748 |
| KNN                  |        93.22% |     0.9048 |     0.9820 |

## Key Takeaway

The results show that deep temporal convolution architectures can effectively identify patterns associated with stress in wearable ECG signals. CDIL-CNN achieved the strongest performance among the evaluated approaches and outperformed several traditional machine learning models.

## Technologies

* Python
* NumPy
* Pandas
* Scikit-learn
* TensorFlow / Keras
* PyTorch
* XGBoost
* Matplotlib
* Machine Learning
* Deep Learning
* Time-Series Analysis
* Signal Processing

## Kaggle Notebook

The original project notebook is also available on Kaggle:

**Emotion & Stress Detection via Wearable Sensors**

https://www.kaggle.com/code/barghavnaikeslavath/emotion-stress-detection-via-wearable-sensors
