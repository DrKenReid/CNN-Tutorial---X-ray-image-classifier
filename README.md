# 🫁 CNN X-ray Image Classifier for Pneumonia Detection

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrKenReid/CNN-Tutorial---X-ray-image-classifier/blob/main/CNN_Tutorial_X_ray_image_classifier.ipynb)

## 🔍 Overview
This Google Colab notebook implements a Convolutional Neural Network (CNN) for classifying chest X-ray images as either normal or indicating pneumonia. It serves as a hands-on tutorial for medical professionals and researchers in radiology and pulmonary diseases who want to explore automated diagnosis assistance tools using deep learning.

## ✨ Features
- **📊 Data Preparation**: Automatically downloads and prepares the pneumonia X-ray dataset from Kaggle.
- **🖼️ Image Preprocessing**: Implements image resizing, normalization, and data augmentation using the modern `tf.data` / `tf.image` pipeline.
- **🧠 CNN Model Architecture**: A 5-block CNN with BatchNormalization and Dropout for regularization, compiled with Adam optimizer and binary crossentropy loss.
- **⚖️ Class Balancing**: Computes and applies class weights to handle imbalanced datasets (common in medical imaging).
- **🏋️‍♀️ Model Training**: Uses TensorFlow/Keras with EarlyStopping and ReduceLROnPlateau callbacks for efficient, automated training.
- **📈 Performance Evaluation**: Assesses model performance using accuracy, precision, recall, F1-score, and confusion matrix.
- **📊 Visualization**: Provides visualizations of sample X-rays, training progress curves, confusion matrix heatmaps, and color-coded prediction results.
- **🔬 Reproducibility**: Sets random seeds for TensorFlow and NumPy to promote consistent results across runs.
- **☁️ Google Drive Integration**: Automatically saves the trained model and training history to Google Drive for persistence.

## 🛠️ Requirements
- Google Colab environment (free GPU recommended: Runtime → Change runtime type → GPU)
- Google account for Google Drive integration
- Kaggle account and API credentials for dataset access ([create token here](https://www.kaggle.com/settings/account))
- Required libraries (pre-installed or auto-installed in Colab):
  - TensorFlow (includes Keras)
  - NumPy
  - Pandas
  - Matplotlib
  - Seaborn
  - Scikit-learn

## 🚀 Usage
1. Click the **Open in Colab** badge above (or open the notebook manually in Google Colab).
2. Ensure you have a Kaggle account and API token (instructions provided in the notebook).
3. Run the cells in order, following the markdown explanations in each section.
4. The notebook will guide you through:
   - Setting up the Kaggle API and downloading the dataset
   - Preparing and preprocessing the X-ray images
   - Building and training the CNN model
   - Evaluating the model's performance
   - Visualizing results and predictions

## ⚙️ Configuration
You can modify the following parameters in the notebook:
- `batch_size`: Number of images processed in each training iteration (default: 32)
- `img_height` and `img_width`: Dimensions of input images (default: 150×150; increase to 256×256 or 512×512 for higher fidelity at the cost of longer training)
- CNN architecture: Number of convolutional blocks, filters, Dropout rates, and dense layer sizes
- Training parameters: Number of epochs, EarlyStopping patience, learning rate reduction factor

## 📤 Output
The notebook generates several outputs:
1. Trained CNN model saved to Google Drive (`.keras` format)
2. Training history saved as JSON (loss and accuracy per epoch)
3. Visualizations of sample X-rays with class labels
4. Training accuracy/loss curves
5. Confusion matrix heatmap and full classification report

## ⚠️ Limitations
- Designed to run in Google Colab; modifications may be needed for local execution
- Performance depends on the quality and diversity of the training dataset
- Intended for research and educational purposes; not for clinical use without proper validation
- GPU non-determinism means results may vary slightly between runs despite random seeds

## 🤝 Contributing
Contributions, issues, and feature requests are welcome. Feel free to check the [issues page](https://github.com/DrKenReid/CNN-Tutorial---X-ray-image-classifier/issues) if you want to contribute.

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).

## ⚖️ Disclaimer
This tool is for research and educational purposes only. It should not be used for clinical diagnosis without proper medical validation and regulatory approval.
