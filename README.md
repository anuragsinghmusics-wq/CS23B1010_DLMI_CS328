# Brain MRI Tumor Segmentation using Otsu & Sauvola

## Project Overview
This project performs brain tumor segmentation on MRI images using two classical thresholding techniques:

- Otsu Thresholding  
- Sauvola Thresholding  

The main objective is to check whether simple image processing methods can accurately detect tumor regions.

---

## Dataset
Dataset used: Brain Tumor Segmentation – Nikhil Tomar (Kaggle)

The dataset contains:
- MRI images  
- Ground truth masks  

---

## Methodology

### 1. Preprocessing
- CLAHE (Contrast Limited Adaptive Histogram Equalization)
- Gaussian Blur for noise removal

### 2. Segmentation Techniques
- Otsu Thresholding
- Sauvola Thresholding

### 3. Evaluation Metrics
- Dice Score
- Jaccard Score (IoU)

These metrics measure the overlap between the predicted tumor region and the ground truth mask.

---

## Results

### Quantitative Results

| Method   | Dice Score | Jaccard Score |
|----------|------------|---------------|
| Otsu     | 0.0645     | 0.0341        |
| Sauvola  | 0.0428     | 0.0223        |

Both Otsu and Sauvola produced very low overlap scores.

- Otsu performed slightly better than Sauvola
- Overall segmentation quality is poor

This shows that simple thresholding methods are not suitable for accurate brain tumor segmentation, and advanced methods are required.

---

## Output Visualization

The output displays:

- Original MRI Image  
- Ground Truth Mask  
- Otsu Segmentation Result  
- Sauvola Segmentation Result  

---

## Requirements

Install the required libraries:

```bash
pip install opencv-python scikit-image tqdm matplotlib pandas
