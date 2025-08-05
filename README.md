# COVID-19 Chest X-Ray Classifier

This project is a Convolutional Neural Network (CNN)-based classifier that detects COVID-19 from chest X-ray images. The dataset used contains X-ray images of COVID-positive and COVID-negative patients.

## 📂 Dataset

- The dataset was loaded using TensorFlow's `image_dataset_from_directory` method.
- It was structured into separate folders for training, validation, and testing:
  - `/train`
  - `/val`
  - `/test`
- There are 40 images in the test set.

## 🧠 Model Architecture

- A simple CNN architecture was implemented using `Conv2D`, `MaxPooling2D`, `Flatten`, and `Dense` layers.
- The input shape used was `(180, 180, 3)`.
- Model was compiled with:
  - `optimizer='adam'`
  - `loss='binary_crossentropy'`
  - `metrics=['accuracy']`

## 📈 Performance

- The model achieved **~100% accuracy** on both training and test datasets.
- ⚠️ Note: The high accuracy is due to the simplicity and small size of the dataset, with only 40 images in the test set. This makes the model's task easier and less representative of real-world complexity.

Please do not consider this model reliable for real-world medical diagnosis without further testing and validation.

## ⚙️ Tools Used

- Python
- TensorFlow / Keras
- Google Colab

## 🚀 How to Run

1. Upload the dataset with proper folder structure: `train`, `val`, and `test` inside the base directory.
2. Load data using:

    ```python
    tf.keras.utils.image_dataset_from_directory()
    ```

3. Train and evaluate the model using the provided notebook.

## 📌 Future Improvements

- Add data augmentation to generalize better.
- Introduce dropout or L2 regularization to prevent overfitting.
- Increase dataset size for more robustness.

## 📁 File

- `COVID_19_Xray.ipynb` – Jupyter Notebook containing the full training pipeline.
