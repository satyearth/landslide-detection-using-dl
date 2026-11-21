# Landslide Detection Using Deep Learning

A deep learning-based semantic segmentation project that detects landslide-affected regions from multispectral satellite imagery using a U-Net architecture.

## Overview

Landslides can cause significant damage to infrastructure, ecosystems, and human settlements. This project explores the use of deep learning and satellite imagery to identify landslide-affected areas through pixel-level image segmentation.

The model takes multispectral satellite images as input and predicts a binary segmentation mask highlighting landslide regions.

## Project Highlights

- Uses multispectral satellite imagery with 14 input channels.
- Processes images at a resolution of 128 × 128 pixels.
- Implements a U-Net architecture for semantic segmentation.
- Uses Binary Cross-Entropy (BCE) and Dice Loss.
- Trained using the Adam optimizer.
- Training configured for 30 epochs.

## Dataset

| Dataset | Number of Samples |
|---|---:|
| Training images and masks | 3,799 |
| Validation images | 245 |
| Test images | 800 |

**Input shape:** `128 × 128 × 14`

The training dataset contains corresponding segmentation masks. The test dataset does not contain ground-truth labels, so test predictions are not independently verified.

## Model Architecture

**U-Net**

U-Net is a convolutional neural network commonly used for biomedical and satellite image segmentation. Its encoder-decoder structure and skip connections help capture both contextual and spatial information.

The model performs binary pixel-wise segmentation:

- Landslide-affected region
- Non-landslide region

## Technologies Used

- Python
- PyTorch
- NumPy
- Pandas
- Matplotlib
- h5py
- Scikit-learn

## Evaluation Results

The following results were obtained on the validation dataset:

| Metric | Score |
|---|---:|
| Dice Score | 76.59% |
| IoU | 62.06% |
| Precision | 75.12% |
| Recall | 78.11% |

These metrics represent validation performance, not verified test-set performance.

## Project Workflow

1. Load multispectral satellite imagery.
2. Preprocess images and segmentation masks.
3. Build the U-Net segmentation model.
4. Train using BCE + Dice Loss.
5. Evaluate predictions using Dice Score, IoU, Precision, and Recall.
6. Generate landslide segmentation predictions.

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Install the required libraries:

```bash
pip install torch numpy pandas matplotlib h5py scikit-learn
```

## How to Run

1. Open the Jupyter Notebook included in this repository.
2. Configure the dataset paths according to your local environment.
3. Run the notebook cells in sequence.
4. Train the model and evaluate its validation performance.

## Applications

- Landslide-affected area identification
- Satellite image analysis
- Disaster management research
- Remote sensing and environmental monitoring

## Future Improvements

- Improve segmentation accuracy with additional training data.
- Experiment with advanced segmentation architectures.
- Evaluate performance on independently labeled test imagery.
- Explore deployment for large-scale satellite image analysis.

## Disclaimer

This project is developed for educational and research purposes. Predictions should not be treated as a substitute for professional geological assessment or official disaster-management decisions.

## Author

**Satya**
