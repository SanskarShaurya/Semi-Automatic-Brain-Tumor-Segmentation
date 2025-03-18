# Semi-Automatic-Brain-Tumor-Segmentation

## Overview
This repository contains a Jupyter Notebook that implements Otsu-segmentation along with smoothening techniques. The methodology follows the approach described in the research paper "A semi-automatic brain tumor segmentation algorithm".

## Features
- Loads and processes an image
- Converts it to grayscale
- Pads the image to ensure a square shape
- Otsu based N-level thresholding algorithm is used to segment the original MRI image (and smoothened image) into (N+1) classes.
- The two segmentation maps are fused with the rule of K Nearest Neighbors (KNN).
- A seed point needs to be manually placed on each tumor region by the user. The final segmented tumor regions are extracted using a bi-directional region growing algorithm

## Requirements
Ensure you have the following Python libraries installed:
```bash
pip install numpy matplotlib pillow scikit-image scipy
```

## Usage
1. Clone this repository:
```bash
git clone <repo-url>
cd <repo-directory>
```
2. Run the Jupyter Notebook:
```bash
jupyter notebook code.ipynb
```

## File Structure
- `code.ipynb` - Jupyter Notebook containing the image processing pipeline

## Example Output
The script processes an image and applies multi-scale smoothing techniques, giving us an image with tumor detected in it.

## References
X. Zhang, X. Li, H. Li and Y. Feng, "A semi-automatic brain tumor segmentation algorithm," 2016 IEEE International Conference on Multimedia and Expo (ICME), Seattle, WA, USA, 2016, pp. 1-6, doi: 10.1109/ICME.2016.7553003.

