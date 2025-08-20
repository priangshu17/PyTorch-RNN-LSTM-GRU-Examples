# PyTorch-RNN-LSTM-GRU-Examples

This repository contains two educational Jupyter Notebooks that implement and compare three fundamental recurrent neural network (RNN) architectures: the simple RNN, Gated Recurrent Unit (GRU), and Long Short-Term Memory (LSTM). The models are applied to two different domains to showcase their versatility: image classification and text classification.

## 🚀 Projects Overview

The repository is divided into two distinct projects, each in its own notebook.

---

### 1. MNIST Image Classification with RNNs

* **Notebook:** `rnn_lstm_gru_mnist.ipynb`
* **Concept:** This project demonstrates an interesting application of RNNs to computer vision. The MNIST dataset, which consists of 28x28 pixel images of handwritten digits, is treated as a sequence. Each image is viewed as a sequence of 28 time steps, where each step is a row of 28 pixels.
* **Models Compared:** A flexible `RecurrentNet` class is used to build and compare the performance of a simple **RNN**, **GRU**, and **LSTM**.

#### Results on MNIST

After 5 epochs of training, the models achieved the following accuracy on the 10,000 test images:

| Model       | Test Accuracy |
| :---------- | :------------ |
| **GRU** | **98.62 %** |
| **LSTM** | 98.23 %       |
| **Simple RNN**| 96.31 %       |

---


### 2. IMDb Sentiment Analysis with Bidirectional RNNs

* **Notebook:** `rnn_lstm_gru_text.ipynb`
* **Concept:** This project tackles a classic Natural Language Processing (NLP) task: sentiment analysis on the IMDb movie review dataset. It utilizes the `transformers` and `datasets` libraries from Hugging Face for efficient data handling and tokenization.
* **Models Compared:** A `TextClassifier` class is used to build and compare **bidirectional** versions of the **RNN**, **GRU**, and **LSTM**. Bidirectionality allows the network to learn from both past and future context in the text sequence.

#### Results on IMDb

After 5 epochs of training, the models achieved the following accuracy on the validation set. Training history plots are also generated within the notebook.

| Model                 | Validation Accuracy |
| :-------------------- | :------------------ |
| **Bidirectional GRU** | **~88.24 %** |
| **Bidirectional LSTM**| ~51.12 %            |
| **Bidirectional RNN** | ~50.00 %            |

*(Note: The RNN and LSTM models struggled to learn effectively with the given hyperparameters, highlighting the GRU's strong performance on this task.)*

---

Navigate to and open either of the two notebooks:

rnn_lstm_gru_mnist.ipynb for the image classification task.

rnn_lstm_gru_text.ipynb for the text classification task.

Run the cells sequentially to see the data preparation, model training, and evaluation process for each architecture.


