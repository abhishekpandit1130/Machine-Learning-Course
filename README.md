# Assignment 1 – Recognize a Digit using Machine Learning (TensorFlow/Keras)

This project implements a Convolutional Neural Network (CNN) to recognize handwritten digits from the **MNIST** dataset using **TensorFlow** and **Keras**.  
The notebook includes **line-by-line explanations** in separate markdown cells for clarity.

---

## 📂 Repository Contents
- **Assignment1_MNIST.ipynb** – Main Jupyter/Colab notebook with code and explanations.
- **mnist_cnn.h5** – Saved trained CNN model (Keras format).
- **predictions_sample100.csv** – Example predictions on 100 test images.
- **README.md** – Project description and instructions.

---

## 📊 Dataset
The [MNIST dataset](http://yann.lecun.com/exdb/mnist/) contains:
- **60,000 training images**
- **10,000 test images**
- Each image: 28×28 pixels, grayscale
- Classes: Digits 0–9

---

## ⚙️ Requirements
Ensure the following Python libraries are installed:
```bash
pip install tensorflow numpy matplotlib pandas

