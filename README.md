# Handwritten Character Recognition

## 📌 Project Overview

This project implements a Convolutional Neural Network (CNN) to recognize handwritten digits from 0 to 9.

The model is trained on the MNIST handwritten digit dataset and learns to classify images of handwritten digits automatically.

The objective of this project is to build, train, evaluate, and save a deep learning model capable of recognizing handwritten digits with high accuracy.

---

## 🎯 Objective

The main objectives of this project are:

- Load and preprocess the MNIST dataset.
- Visualize handwritten digit images.
- Build a Convolutional Neural Network (CNN).
- Train the model on handwritten digit images.
- Evaluate the model using test data.
- Analyze model performance using classification metrics and a confusion matrix.
- Make predictions on unseen handwritten digits.
- Save the trained model for future use.

---

## 📊 Dataset

The project uses the **MNIST Handwritten Digit Dataset**.

The dataset contains:

- 60,000 training images
- 10,000 testing images
- Image size: 28 × 28 pixels
- 10 classes: digits 0–9
- Grayscale images

The MNIST dataset is loaded directly using TensorFlow/Keras.

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 🔄 Data Preprocessing

The pixel values originally range from 0 to 255.

They were normalized to a range of 0 to 1 using:

```python
x_train = x_train.astype("float32") / 255.0
x_test = x_test.astype("float32") / 255.0
A channel dimension was then added so that the images could be provided to the CNN:

(28, 28) → (28, 28, 1)
🧠 CNN Architecture

The model consists of the following layers:
Input layer – 28 × 28 × 1
Convolutional layer – 32 filters
Max Pooling layer
Convolutional layer – 64 filters
Max Pooling layer
Flatten layer
Fully connected Dense layer – 128 neurons
Output layer – 10 neurons with Softmax activation

The convolutional layers learn visual features such as edges, curves, and digit shapes.

The final Softmax layer produces probabilities for the 10 possible digits.

⚙️ Model Configuration

The model was compiled using:

Optimizer: Adam
Loss function: Sparse Categorical Crossentropy
Evaluation metric: Accuracy
Epochs: 5
Batch size: 64
Validation split: 10%
📈 Results

The model achieved the following performance:

Metric	Result
Training Accuracy	99.35%
Validation Accuracy	99.13%
Test Accuracy	99.02%
Test Loss	0.0330

The model successfully generalized to the unseen MNIST test dataset.

🔍 Model Evaluation
Classification Report

The model achieved approximately 99% precision, recall, and F1-score across all digit classes from 0 to 9.

This indicates that the model performs consistently across the different handwritten digit classes.

Confusion Matrix

A confusion matrix was used to analyze the predictions for each digit.

The diagonal cells represent correctly classified images, while the off-diagonal cells represent misclassifications.

The large values along the diagonal demonstrate the strong classification performance of the CNN.

🖼️ Sample Predictions

The trained model was tested on unseen handwritten digit images.

For example:

Actual Digit: 7
Predicted Digit: 7

The model also correctly classified a set of 10 randomly selected test examples used during evaluation.

💾 Saved Model

The trained model has been saved as:

handwritten_digit_model.keras

This allows the trained CNN to be loaded later without retraining it from scratch.

📁 Project Structure
Handwritten_Character_Recognition/
│
├── handwritten_character_recognition.ipynb
├── handwritten_digit_model.keras
├── requirements.txt
└── README.md
🚀 How to Run the Project
1. Clone the repository
git clone <your-github-repository-url>
2. Open the project folder
cd Handwritten_Character_Recognition
3. Install the required packages
pip install -r requirements.txt
4. Open the Jupyter Notebook

Open:

handwritten_character_recognition.ipynb
5. Run the notebook

Run the cells sequentially to:

Load the dataset
Preprocess the images
Build the CNN
Train the model
Evaluate the model
Generate predictions
Visualize the results
📌 Conclusion

A Convolutional Neural Network was successfully developed for handwritten digit recognition using the MNIST dataset.

The model achieved 99.02% accuracy on the test dataset, demonstrating that CNNs can effectively learn visual patterns from handwritten digit images and classify them accurately.