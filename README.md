# Change Detection in Bi-Temporal Satellite Images

## Overview

This repository focuses on bi-temporal satellite image change detection using deep learning techniques.

The primary objective of this project is to design and develop a novel architecture capable of outperforming existing state-of-the-art (SOTA) models on standard change detection benchmarks. To ensure meaningful comparison, several leading architectures have been carefully implemented and evaluated under consistent experimental settings.

The proposed model developed in this work is currently under review at the IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing (IEEE JSTARS). Full architectural details and implementation will be released after the review process is completed.

The implementations included here serve as strong baselines for comparison.


## Implemented Models

The following state-of-the-art architectures have been implemented and benchmarked:

- UNet++
- AGCDetNet
- UCDNet
- ECFNet
- SEIFNet
- ERSCDNet
- EGCDNet
- MSNet

Each model follows the structure and training methodology described in its original publication. The goal is faithful reproduction and fair evaluation.


## Datasets

### EGY-BCD Dataset

- Total image pairs: 6091
- Original resolution: 256 × 256
- Regions:
  - New Mansoura
  - El Falala City
  - New Cairo
  - New Thebes

Each sample consists of a bi-temporal image pair and a corresponding binary ground-truth change mask.

For experimentation:

- 2000 image pairs randomly selected
- Resized to 512 × 512
- Split into Train / Validation / Test with a 7:1:2 ratio


### LEVIR-CD Dataset

- 637 high-resolution image pairs
- Spatial resolution: 0.5 meters per pixel
- Original patch size: 1024 × 1024
- Focus: building and structural change detection

For training consistency:

- Patched into 512 × 512
- Final split:
  - 1776 training samples
  - 256 validation samples
  - 512 test samples
- Split ratio: 7:1:2

This dataset is highly imbalanced, with only a small fraction of pixels representing changed regions.


## Evaluation Metrics

All models are evaluated using:

- Precision
- Recall
- F1 Score
- Intersection over Union (IoU)
- Cohen’s Kappa
- Overall Accuracy
- Number of Parameters (Millions)
- Average Prediction Time per Image (seconds)

These metrics provide both accuracy and efficiency comparisons.


# Experimental Results

## EGY-BCD Dataset

| Model      | Precision | Recall | F1     | Kappa  | IoU    | Accuracy | Params (M) | Avg Time (s) |
|------------|------------|--------|--------|--------|--------|----------|------------|--------------|
| UNet++     | 0.4210     | 0.7465 | 0.5310 | 0.4116 | 0.3615 | 0.7924   | 4.9        | 0.6889       |
| AGCDetNet  | 0.8084     | 0.7656 | 0.7864 | 0.7749 | 0.6480 | 0.9782   | 48.1       | 0.8272       |
| UCDNet     | 0.4234     | 0.7278 | 0.5353 | 0.3979 | 0.3655 | 0.7719   | 1.3        | 0.6699       |
| ECFNet     | 0.6757     | 0.8083 | 0.7361 | 0.6735 | 0.5824 | 0.8573   | 24.6       | 0.6236       |
| SEIFNet    | 0.7782     | 0.7615 | 0.7698 | 0.7197 | 0.6257 | 0.9178   | 19.8       | 0.7280       |
| ERSCDNet   | 0.6825     | 0.7975 | 0.7355 | 0.6815 | 0.5817 | 0.9097   | 1.1        | 0.6355       |
| EGCDNet    | 0.7768     | 0.7191 | 0.7468 | 0.6937 | 0.5959 | 0.9022   | 71.7       | 0.6997       |
| MSNet      | 0.6728     | 0.6179 | 0.6442 | 0.5698 | 0.4751 | 0.8722   | 10.1       | 0.6952       |


## LEVIR-CD Dataset (Three Bands)

| Model      | Precision | Recall | F1     | Kappa  | IoU    | Accuracy | Params (M) | Avg Time (s) |
|------------|------------|--------|--------|--------|--------|----------|------------|--------------|
| UNet++     | 0.9133     | 0.7028 | 0.7943 | 0.7845 | 0.6588 | 0.9809   | 4.9        | 0.6870       |
| AGCDetNet  | 0.8166     | 0.7852 | 0.8006 | 0.7898 | 0.6675 | 0.9795   | 48.1       | 0.6120       |
| UCDNet     | 0.8697     | 0.8472 | 0.8583 | 0.8508 | 0.7517 | 0.9803   | 1.3        | 0.6715       |
| ECFNet     | 0.8393     | 0.8236 | 0.8313 | 0.8189 | 0.7114 | 0.9811   | 24.6       | 0.7426       |
| SEIFNet    | 0.8568     | 0.7999 | 0.8274 | 0.8181 | 0.7056 | 0.9178   | 19.8       | 0.6791       |
| ERSCDNet   | 0.8624     | 0.9300 | 0.8949 | 0.8889 | 0.8090 | 0.9885   | 1.1        | 0.5869       |
| EGCDNet    | 0.8286     | 0.8298 | 0.8242 | 0.8143 | 0.7009 | 0.9868   | 71.7       | 0.6217       |
| MSNet      | 0.8443     | 0.8048 | 0.8241 | 0.8148 | 0.7008 | 0.9715   | 10.1       | 0.6639       |


## Qualitative Results

Add your comparison image here, for example:

![Qualitative Comparison](results/comparison_example.png)


## Requirements

- Python 3.x
- TensorFlow / Keras
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn


## References

Add full IEEE-formatted citations for:

- UNet++
- AGCDetNet
- UCDNet
- ECFNet
- SEIFNet
- ERSCDNet
- EGCDNet
- MSNet
- EGY-BCD Dataset
- LEVIR-CD Dataset
