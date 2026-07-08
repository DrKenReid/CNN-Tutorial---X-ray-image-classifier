# CNN X-ray Image Classifier for Pneumonia Detection

A hands-on tutorial implementing a Convolutional Neural Network for classifying chest X-ray images as normal or pneumonia-positive. Designed as a learning resource for medical professionals and researchers exploring deep learning for diagnostic imaging.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrKenReid/CNN-Tutorial---X-ray-image-classifier/blob/main/CNN_Tutorial_X_ray_image_classifier.ipynb)

## Techniques Demonstrated

| Category | Details |
|---|---|
| **Data Pipeline** | Kaggle API integration, `tf.data`/`tf.image` preprocessing, resizing, normalisation |
| **Data Augmentation** | Random horizontal flips plus brightness/contrast jitter to improve generalisation |
| **Class Balancing** | Computed class weights to handle imbalanced medical imaging datasets |
| **CNN Architecture** | 3-block CNN (32→64→128 filters) with BatchNormalization, Dropout, Adam optimiser, binary crossentropy |
| **Training** | EarlyStopping, ReduceLROnPlateau callbacks; model and history saved to Google Drive |
| **Evaluation** | Accuracy, precision, recall, F1-score, confusion matrix heatmap, ROC curve/AUC with operating-threshold analysis |
| **Reproducibility** | TensorFlow and NumPy random seeds for consistent results |

## How to Use

1. Open the notebook in Google Colab using the badge above (free GPU recommended: **Runtime → Change runtime type → GPU**).
2. You will need a [Kaggle API token](https://www.kaggle.com/settings/account) — create one under "API Tokens" (recommended; legacy credentials also still work). The notebook walks you through setup and installs the required `kaggle` CLI (≥ 1.8.0).
3. Run the cells in order. The notebook automatically downloads the chest X-ray dataset, trains the model, and evaluates performance.
4. The trained model and training history are saved to your Google Drive automatically.

## Configuration

Key parameters you can adjust in the notebook:

- `batch_size` — images per training iteration (default: 32)
- `img_height` / `img_width` — input dimensions (default: 150×150; increase to 256 or 512 for higher fidelity)
- CNN depth, filter counts, Dropout rates, and dense layer sizes
- EarlyStopping patience and learning rate reduction factor

## A Note on Medical AI

A model like this can post high validation accuracy yet score noticeably lower on the held-out test set — this benchmark is known for distribution shift and image-level (rather than patient-level) splits, and the notebook includes a section explaining why that gap appears and what it teaches. Medical imaging in practice demands far more rigour: patient-level data splits, diverse training populations, radiologist-validated labels, regulatory approval, and prospective clinical trials. The notebook is a pedagogical tool — it demonstrates the mechanics of building a diagnostic CNN, not a deployable clinical system. That gap between "works on a benchmark" and "works in a hospital" is where most of the real engineering lives.

## License

This project is open-source and available under the [MIT License](LICENSE).

## Related

- [Generalized Analysis of Text Data](https://github.com/DrKenReid/Generalized-Analysis-of-Text-Data) — NLP reference notebook with 13 techniques
- [VAE for Molecule Discovery](https://github.com/DrKenReid/VAE-for-Molecule-Discovery) — generative modelling for drug discovery
- [kenreid.co.uk/data_science](https://www.kenreid.co.uk/data_science.html) — all projects, publications, and CV

## Author

**Ken Reid** — Data Scientist, photographer, and avid reader.

- [kenreid.co.uk](https://www.kenreid.co.uk) — Portfolio & blog
- [@kenreid.co.uk](https://bsky.app/profile/kenreid.co.uk) — Bluesky
- [@DrKenReid](https://github.com/DrKenReid) — GitHub
