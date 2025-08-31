# Assignment 1 — Recognize a Digit using CNN (MNIST Dataset)

This project implements a **Convolutional Neural Network (CNN)** using **TensorFlow/Keras** to recognize handwritten digits from the **MNIST dataset**.
The notebook trains the model, evaluates accuracy, saves the trained model, and also exports predictions to a CSV file.

---

## 📂 Project Structure

```
├── Assignment1_MNIST_CNN.ipynb   # Main Jupyter/Colab notebook
├── mnist_cnn.h5                  # Saved trained model
├── predictions_sample100.csv     # Predictions for first 100 test images
└── README.md                     # Project description
```

---

## 📊 Dataset

* **MNIST Dataset** — 70,000 grayscale images of handwritten digits (0–9).

  * Training set: **60,000 images**
  * Test set: **10,000 images**
* Each image is **28 × 28 pixels** in grayscale.

---

## ⚙️ Steps Implemented

1. **Import Libraries** — NumPy, Matplotlib, TensorFlow/Keras, Pandas.
2. **Load Dataset** — Download and split MNIST into training and test sets.
3. **Preprocess Data**

   * Normalize pixel values to range \[0,1].
   * Reshape images to add channel dimension.
   * Convert labels to **one-hot encoding**.
4. **Visualize Samples** — Plot a few digit images.
5. **Build CNN Model**

   * Conv2D → MaxPooling → Conv2D → MaxPooling → Flatten → Dense → Dropout → Dense.
6. **Compile Model**

   * Optimizer: `Adam`
   * Loss: `categorical_crossentropy`
   * Metric: `accuracy`
7. **Train Model**

   * 8 epochs
   * Batch size: 128
   * Validation split: 10%
8. **Evaluate Model** — Achieved **\~99.2% accuracy** on test set.
9. **Make Predictions** — Test model on sample images.
10. **Save Model & Predictions**

    * Model saved as `mnist_cnn.h5`.
    * Predictions for first 100 test images exported as `predictions_sample100.csv`.

---

## 📈 Results

* **Training Accuracy:** \~98.9%
* **Validation Accuracy:** \~99.1%
* **Test Accuracy:** \~99.2%

The CNN model generalizes well with very low error rate.

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/<your-username>/Machine-Learning-Course.git
   ```
2. Open the notebook in Jupyter or Google Colab.
3. Run all cells to train and evaluate the model.
4. Check saved model (`mnist_cnn.h5`) and predictions CSV.

---

## 📌 Files Generated

* **`mnist_cnn.h5`** → Trained model file (can be reloaded for inference).
* **`predictions_sample100.csv`** → Contains predicted labels for first 100 test images.

---

## ✅ Conclusion

This project demonstrates how **Convolutional Neural Networks (CNNs)** can effectively classify handwritten digits with very high accuracy using the MNIST dataset.
The trained model achieves **>99% accuracy** and can be extended for digit recognition tasks in real-world applications.





# 📈 House Price Prediction — Linear Regression & Gradient Descent

This project demonstrates **linear regression** for predicting **house prices from house size** (in sq ft).
We compare the **Scikit-Learn Linear Regression model** with a **custom implementation of Gradient Descent**.

---

## 📂 Project Structure

```
├── HousePrice_Prediction.ipynb   # Main Jupyter/Colab notebook
├── README.md                     # Project description
```

---

## 🏡 Dataset

* Synthetic dataset generated for demonstration.
* **80 samples** of house sizes (500–3500 sq ft).
* True price relation:

  $$
  \text{Price (Lakhs)} \approx 0.1 \times \text{Size (sq ft)}
  $$
* Added Gaussian noise (±10 lakhs) to simulate real-world variation.

---

## ⚙️ Steps Implemented

1. **Setup & Imports** — NumPy, Matplotlib, Scikit-Learn.
2. **Dataset Creation** — Synthetic data of house sizes vs prices.
3. **Data Visualization** — Scatter plot of dataset.
4. **Baseline Model** — Scikit-Learn’s `LinearRegression`.
5. **Prepare for Gradient Descent** — Feature scaling, bias term.
6. **Define Loss & Gradient** — Mean Squared Error (MSE).
7. **Train with Gradient Descent** — Update weights iteratively.
8. **Plot Epoch vs Accuracy (R² %)** — Track performance.
9. **Plot Epoch vs Loss (MSE)** — Track convergence.
10. **Fit Comparison** — Compare Sklearn vs Gradient Descent.
11. **Prediction** — Predict house prices for new sizes.

---

## 📊 Results

* **Scikit-Learn Linear Regression**

  * Slope: `0.10150 lakhs/sq ft`
  * Intercept: `-2.94 lakhs`
  * R² Score: **0.9896**

* **Gradient Descent (Custom Implementation)**

  * Learned slope: `0.10135 lakhs/sq ft`
  * Learned intercept: `-2.595 lakhs`
  * Accuracy (R²): \~**99%**

Both methods give nearly identical results ✅.

---

## 📈 Plots

* **House Prices vs Size (with regression line)**
* **Epoch vs Accuracy (R² %)**
* **Epoch vs Loss (MSE)**
* **Fit Comparison (Sklearn vs Gradient Descent)**

---

## 🚀 Example Predictions

Using Gradient Descent model:

* 800 sq ft → **78.48 lakhs**
* 1200 sq ft → **119.02 lakhs**
* 2000 sq ft → **200.10 lakhs**
* 3000 sq ft → **301.44 lakhs**

---

## ✅ Conclusion

* Both **Scikit-Learn** and **custom Gradient Descent** perform very well on this dataset.
* Gradient Descent implementation helps understand **how regression actually learns weights**.
* Achieved **\~99% accuracy (R²)**, showing strong model fit.

---
