# Trained Models

This directory contains trained model weights resulting from experiments run using the scripts in this repository.

## Available Models

*   **`refined_hinge_weight/`**: Contains weights from the experiment comparing the composite loss (BCE+Tversky+Hinge) with and without edge-weighting on the Hinge component, using the refined model architecture (includes extra 3x3 conv).
    *   `model1_epoch_050.pth`: Model trained with *unweighted* Hinge component.
    *   `model2_epoch_050.pth`: Model trained with *edge-weighted* Hinge component.

*   *(Add other experiments/models here as needed)*

## Usage

These weights can be loaded into the model architecture defined in `src/building_segmentation/models.py` for evaluation or further fine-tuning. See the evaluation scripts or notebooks for examples.

## Download / Git LFS

*(Choose ONE option)*

**Option A (External Download):**
These model weights are hosted externally due to their size. You can download them from:
*   [Link to Google Drive / Dropbox / etc. where weights are stored]

Place the downloaded `.pth` files into the corresponding subdirectories within this `models/` folder.

**Option B (Git LFS):**
These model weights are tracked using Git Large File Storage (LFS). Ensure you have Git LFS installed (`git lfs install`). Cloning the repository should automatically download the weights. If not, run `git lfs pull` after cloning.
