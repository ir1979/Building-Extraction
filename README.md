# Building Extraction using DeepLabV3+ and Custom Loss Functions

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) <!-- Choose your license -->

This project explores semantic segmentation of buildings from aerial imagery using PyTorch and the DeepLabV3+ architecture (with a ResNet50 backbone). The primary focus is on improving boundary prediction accuracy through the use of custom composite loss functions, particularly incorporating edge-weighted components.

## Features

*   **Model:** DeepLabV3+ with ResNet50 backbone (using `torchvision`).
*   **Datasets:** Primarily uses the Massachusetts Buildings Dataset (support for others like Inria can be adapted). Data is handled externally via Google Drive (see `data/README.md`).
*   **Loss Functions:** Implements a composite loss combining Binary Cross-Entropy (BCE), Tversky loss, and an adapted Hinge loss.
*   **Edge Weighting:** Explores applying Sobel-filter-derived edge weights to loss components (specifically Hinge loss) to emphasize boundary learning.
*   **Refinement Layer:** Includes an option to add a final 3x3 convolutional layer for potential output refinement.
*   **Comparative Experiments:** Scripts designed to train two models in parallel with identical initial weights but different loss configurations for direct comparison.
*   **Visualization:** Generates detailed visualizations comparing model outputs (probability maps, error maps, loss component maps) over epochs.
*   **Animation:** Creates animated GIFs showing the evolution of predictions and metrics over training epochs.
*   **Metrics:** Comprehensive evaluation metrics (IoU, Dice, Precision, Recall, TP/FP/FN/TN) logged during training and validation.

## Repository Structure

