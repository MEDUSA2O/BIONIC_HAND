# Bionic Hand

This repository contains the code, models, and resources for developing a real-time signal classification system for a bionic hand. The project focuses on classifying Electromyographic (EMG) signals from the forearm muscles of amputees into six distinct action classes. The classified actions are then used to control a prosthetic hand, enabling more natural and intuitive movement for the user.

## Data Collection

The dataset consists of EMG signals collected from the forearm muscles of participants. These signals were recorded using non-invasive surface electrodes placed at specific locations on the forearm. The data captures the electrical activity generated by muscle contractions when the user attempts different hand movements.

## Data Preprocessing

To ensure the accuracy and reliability of the model, the raw EMG signals underwent several preprocessing steps:

- **Noise Removal**: Unnecessary frequencies and noise were filtered out to enhance the quality of the signals.
- **Normalization and Standardization**: The EMG data was normalized and standardized to ensure consistent input to the machine learning models, improving the classification accuracy.

## Model Development

### Convolutional Neural Network (CNN)

A Convolutional Neural Network (CNN) was trained on the preprocessed EMG data to classify the signals into six action classes. The CNN architecture was chosen for its ability to capture spatial hierarchies and patterns within the signal data, leading to robust classification performance.

### Temporal Convolutional Network (TCN)

In addition to the CNN, a Temporal Convolutional Network (TCN) was also developed to explore the temporal dynamics of the EMG signals. TCNs are particularly effective in sequence modeling, making them well-suited for capturing the time-dependent nature of EMG signals.

## Model Comparison

The performance of the CNN and TCN models was compared to determine the most effective approach for real-time signal classification. Both models were evaluated based on accuracy, latency, and real-time performance when deployed on the bionic hand.

## Deployment on Raspberry Pi

The trained models were optimized and deployed on a Raspberry Pi, enabling real-time classification of EMG signals directly on the device. TensorFlow Lite and ONNX were used to convert and run the models on the Raspberry Pi, ensuring low-latency and efficient performance suitable for controlling the prosthetic hand.

## Real-Time Performance

The deployed system achieved a 78% accuracy in classifying real-time EMG signals, providing a reliable and responsive interface for the bionic hand. The system's low latency and high accuracy make it a practical solution for real-world prosthetic applications.
