# BT5153 Group 06 — Diabetic Retinopathy Prediction

This project focuses on detecting diabetic retinopathy using deep learning and traditional machine learning approaches.  
It combines data preprocessing, feature extraction, model training, and a web-based demo built using Flask.

---

## 📂 Folder Overview

### PythonNotebook/

This folder contains all the Jupyter Notebooks used during the development phase:

| Notebook | Description |
|:---------|:------------|
| **DatasetSplit.ipynb** | Prepares the dataset by splitting it into training (70%) , test (15%) , and validation (15%) sets based on image labels. This ensures proper evaluation during model training. |
| **DenseNet_121.ipynb** | Extracts deep features from retinal images using DenseNet121 architectures, train, validate model to classify images into diabetic severity. Evaluation metrics for validation and test set are shown, together with Grad-CAM images for interpretability. |
| **EfficientNetB3+DenseNet_Feature_Extraction_and_Traditional_ML_Classifier.ipynb** | Extracts deep features from retinal images using EfficientNetB3 and DenseNet architectures, then applies traditional machine learning classifiers (such as SVM and Random Forest) to classify diabetic retinopathy severity. |
| **Gaussian_Filter.ipynb** | Applies Gaussian filtering to retinal images to enhance image clarity, reduce noise, and potentially improve feature extraction quality. |
| **Vision_Transformers.ipynb** | Runs a pretrained Vision Transformer model with out preprocessed data, and shows evaluation metrics on the test set after training. Then, generates an attention heatmap and integration with LLM for better interpretability.|

> These notebooks were primarily used for preprocessing, feature engineering, and model training.

---

### FlaskWebsite/

This folder contains the complete source code for the web application built using Flask.  
The web app allows users to upload retinal images and get predictions on diabetic retinopathy severity.

**How to run the Flask website:**

1. Install the required packages (if you haven't already):
   ```bash
   pip install -r requirements.txt
   ```

2. Navigate to the `FlaskWebsite/` directory:
   ```bash
   cd FlaskWebsite
   ```

3. Launch the Flask application:
   ```bash
   python app.py
   ```

4. Open your browser and go to:  
   [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

The website will provide a simple interface where users can upload an image and receive a model prediction.

---

### Other Files and Folders

- **SampleImages/**  
  Contains example retinal images that can be used for testing the Flask application.

- **dataset.txt**  
  Has the google drive link to access the datasets

- **label.csv**  
  A CSV file containing image filenames and their associated diabetic retinopathy labels.

---

## 📝 Notes

- The **PythonNotebook/** and **FlaskWebsite/** are independent. You do not need to run the notebooks to use the web application.
- The pretrained models and feature extraction processes are already integrated into the web app for prediction purposes.
- `dataset.zip` and `label.csv` are mainly for retraining or model experiments, not needed for basic website use.
- The original code contained our **OpenAI API key**. However, to prevent misuse of our key on a public Repo, we have removed this and replaced it with a comment to insert an API key.
---
