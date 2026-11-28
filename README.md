# Landslide Detection Using Deep Learning

A deep learning-based semantic segmentation project that detects landslide-affected regions from multispectral satellite imagery using a U-Net architecture.

## 🔗 Project Notebook

**Kaggle Notebook:** [Landslide Detection Using Deep Learning](https://www.kaggle.com/code/satyearth/landslide-detection-using-dl)

The complete implementation, model training, and evaluation are available in the Kaggle Notebook.

## 📌 Overview

Landslides can cause significant damage to infrastructure, ecosystems, and human settlements. This project explores the use of deep learning and satellite imagery to identify landslide-affected areas through pixel-level image segmentation.

The model takes multispectral satellite images as input and predicts a binary segmentation mask highlighting landslide-affected regions.

## ✨ Project Highlights

- Uses multispectral satellite imagery with 14 input channels.
- Processes images at a resolution of 128 × 128 pixels.
- Implements a U-Net architecture for semantic segmentation.
- Uses Binary Cross-Entropy (BCE) and Dice Loss.
- Trained using the Adam optimizer.
- Training configured for 30 epochs.

## 📂 Dataset

| Dataset | Number of Samples |
|---|---:|
| Training images and masks | 3,799 |
| Validation images | 245 |
| Test images | 800 |

**Input Shape:** `128 × 128 × 14`

The training dataset contains corresponding segmentation masks. The test dataset does not contain ground-truth labels, so test predictions are not independently verified.

## 🧠 Model Architecture

### U-Net

U-Net is a convolutional neural network commonly used for biomedical and satellite image segmentation.

Its encoder-decoder structure and skip connections help capture both contextual and spatial information.

The model performs binary pixel-wise segmentation:

- Landslide-affected region
- Non-landslide region

## ⚙️ Techniques Used

- Semantic Segmentation
- U-Net Architecture
- Multispectral Image Processing
- Binary Cross-Entropy Loss
- Dice Loss
- Adam Optimization
- Pixel-wise Binary Classification

## 🛠️ Technologies Used

- Python
- PyTorch
- NumPy
- Pandas
- Matplotlib
- h5py
- Scikit-learn
- Kaggle Notebooks

## 📊 Evaluation Results

The following results were obtained on the validation dataset:

| Metric | Score |
|---|---:|
| Dice Score | 76.59% |
| IoU | 62.06% |
| Precision | 75.12% |
| Recall | 78.11% |

These metrics represent validation performance, not verified test-set performance.

## 🔄 Project Workflow

1. Load multispectral satellite imagery.
2. Preprocess images and segmentation masks.
3. Build the U-Net segmentation model.
4. Train using BCE + Dice Loss.
5. Evaluate predictions using Dice Score, IoU, Precision, and Recall.
6. Generate landslide segmentation predictions.

## 🚀 How to Run

This project is implemented using Kaggle Notebooks, so no local installation is required.

1. Open the [Kaggle Project Notebook](https://www.kaggle.com/code/satyearth/landslide-detection-using-dl).
2. Sign in to your Kaggle account.
3. Click **Copy & Edit** to create your own editable version.
4. Ensure the required dataset is attached to the notebook.
5. Run the notebook cells sequentially.
6. Train the U-Net model and evaluate its validation performance.

## 🌍 Applications

- Landslide-affected area identification
- Satellite image analysis
- Disaster management research
- Remote sensing
- Environmental monitoring

## 🔮 Future Improvements

- Improve segmentation accuracy with additional training data.
- Experiment with advanced segmentation architectures.
- Evaluate performance on independently labeled test imagery.
- Explore deployment for large-scale satellite image analysis.

## ⚠️ Disclaimer

This project is developed for educational and research purposes. Predictions should not be treated as a substitute for professional geological assessment or official disaster-management decisions.

## 👨‍💻 Author

**Satya**

[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-blue?logo=kaggle)](https://www.kaggle.com/code/satyearth/landslide-detection-using-dl)
