
# Brain Bleed Detection

### Deep Learning-Based Intracranial Hemorrhage Classification Using ResNet-50

## Overview

Brain Bleed Detection is a deep learning project designed to analyze brain CT images and detect intracranial hemorrhage.

The system performs multi-label classification, predicting the presence of five hemorrhage subtypes along with an overall hemorrhage indicator.

The project uses the RSNA 2019 Intracranial Hemorrhage Detection dataset and combines two independently trained ResNet-50 models through ensemble learning.

## Project Objectives

- Detect intracranial hemorrhage from CT slices.
- Classify five different hemorrhage subtypes.
- Apply transfer learning using ResNet-50.
- Improve prediction performance through ensemble learning.
- Visualize model attention using Grad-CAM.
- Provide an interactive demonstration using Gradio.

## Hemorrhage Categories

The model predicts the following labels:

1. Epidural
2. Intraparenchymal
3. Intraventricular
4. Subarachnoid
5. Subdural
6. Any Hemorrhage

## Dataset

**RSNA 2019 Intracranial Hemorrhage Detection**

The project uses a selected subset of the original dataset.

- 14,145 selected CT slices.
- 7,932 patients.
- Patient-level training, validation, and test splitting.
- DICOM image preprocessing and HU conversion.

The dataset is not included in this repository.

## Methodology

1. DICOM image loading and preprocessing.
2. Data cleaning and label preparation.
3. Patient-level dataset splitting.
4. ResNet-50 transfer learning.
5. Training two independent models.
6. Ensemble prediction.
7. Model evaluation using ROC-AUC.
8. Grad-CAM visualization.

##  Model Architecture

- Backbone: ResNet-50
- Learning Approach: Transfer Learning
- Task: Multi-label Classification
- Models: Model A and Model B
- Final Prediction: Ensemble of both models

## Evaluation Results

**Ensemble Model — Test ROC-AUC**

| Category | ROC-AUC |
|---|---:|
| Any Hemorrhage | 0.9596 |
| Epidural | 0.9325 |
| Intraparenchymal | 0.9570 |
| Intraventricular | 0.9628 |
| Subarachnoid | 0.8864 |
| Subdural | 0.8861 |
| **Mean ROC-AUC** | **0.9307** |

These results were obtained using the project's selected held-out test subset.

## Explainability

Grad-CAM is integrated to generate visual heatmaps highlighting image regions that influence model predictions.

These visualizations provide exploratory insight into model attention and are not definitive lesion localization.

## Interactive Application

The project includes a Gradio-based interface designed to support:

- CT DICOM image upload.
- Hemorrhage prediction.
- Individual label probability scores.
- Model comparison.
- Grad-CAM visualization.
- Held-out test sample exploration.

## Technology Stack

- Python
- PyTorch
- ResNet-50
- Deep Learning
- Transfer Learning
- Ensemble Learning
- DICOM / pydicom
- Grad-CAM
- Gradio
- Jupyter Notebook

## Repository Structure

```text
Brain-Bleed-Detection/
│
├── brain-bleed-detection.ipynb
├── Brain_Bleed_CT_Documentation.docx
├── README.md
│
├── app/
├── screenshots/
└── requirements.txt
```

## Limitations & Disclaimer

This project is developed for educational and research purposes only.

It is not a clinically validated diagnostic system and must not be used to diagnose patients or guide medical decisions.

The selected dataset subset has a different label prevalence from the original dataset. Further external validation and clinical evaluation would be required before any clinical use.

## 👩‍💻 Author

**Bsella316**

GitHub: [@Bsella316](https://github.com/Bsella316)
