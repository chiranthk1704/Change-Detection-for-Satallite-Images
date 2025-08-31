# Change Detection in Satellite Images  

## Technologies and Tools Used  
- Python (TensorFlow / Keras)  
- Jupyter Notebooks (`.ipynb`)  
- Deep Learning models for Change Detection  
- Git & GitHub for version control  

---

## Features of the Work  

- Implemented **six state-of-the-art models** for **bi-temporal satellite image change detection**.  
- Each model is implemented as a **separate Jupyter Notebook**, focusing on architectural details from the original research papers.  
- Evaluations include **Accuracy, Precision, Recall, F1-score, IoU, and Cohen’s Kappa**.  
- Tested primarily on the **LEVIR-CD dataset** for building and land-use change detection.  
- Organized results for easy understanding and comparison between different models.  

---

## Implemented Models  

1. **Improved UNet++** – End-to-End Change Detection for High Resolution Satellite Images  
   - Nested skip connections for finer feature extraction.  

2. **AGCDetNet** – Attention-Guided Network for Building Change Detection  
   - Incorporates **channel and spatial attention** to refine feature maps.  

3. **UCDNet** – Deep Learning Model for Urban Change Detection  
   - Multi-scale feature extraction for robust **urban area monitoring**.  

4. **ECFNet** – Siamese Network with Fewer False Positives/Negatives  
   - Reduces misclassifications with a **Siamese CNN framework**.  

5. **SEIFNet** – Spatiotemporal Enhancement and Interlevel Fusion Network  
   - Enhances **spatial + temporal features** and fuses shallow & deep features.  

6. **Robust CNN Framework** – Change Detection from Bi-temporal Images  
   - Strong baseline CNN model robust to **illumination and seasonal variations**.  

---