# Alzheimer’s Diagnostic with OASIS

## Overview
This repository contains the code and documentation for a project aimed at detecting Alzheimer’s disease at an early stage using the Open Access Series of Imaging Studies (OASIS) brain dataset. The project utilizes machine learning techniques, particularly Convolutional Neural Networks (CNN) and the VGG16 model, to classify brain MRI images and identify patterns associated with Alzheimer's disease.

## Contributors
- Devender
- Jagpreet Singh
- Karman Singh Bains
- Manpreet Singh Gill

## Abstract
Alzheimer’s is a nervous system disease that affects human memory and thinking abilities. Detecting it early can slow its progression. This project utilizes MRI scans from the OASIS dataset to detect structural changes in the brain associated with Alzheimer’s disease.

## Dataset
The OASIS dataset consists of MRI scans of 150 individuals aged 60 to 96 years, scanned in a similar environment. The dataset contains brain images and demographic data of the scanned individuals.

## Dataset Preprocessing
- **Selection of Dimension**: The first dimension representing the side view of the brain was chosen for analysis.
- **Image Slicing**: NIfTI medical images were sliced between frames 60 to 70 to maximize information extraction.
- **Categorization Adjustment**: Data augmentation techniques were employed to balance the number of images across different dementia severity categories.

## Materials and Methods
- **Convolutional Neural Network (CNN)**: Implemented a CNN architecture for image classification.
- **VGG16 Model**: Employed the VGG16 pre-trained model as a feature extractor.

## Results
- **CNN**: Achieved a test accuracy of 89.02%.
- **VGG16**: Achieved a test accuracy of 93.59%, outperforming the CNN model.

## Evaluation
- Both models perform well in detecting Alzheimer’s disease, with a focus on minimizing false negatives for Mild Demented cases.
- Emphasis on minimizing misclassification of Mild Demented cases as Non Demented or Moderately Demented.

## Experimentation
- Explored the possibility of incorporating Principal Component Analysis (PCA) for dimensionality reduction.
- Experimented with different model architectures and regularization techniques to improve generalization performance.

## How to Run
1. Clone the repository: `git clone <Alzheimer>`
2. Install dependencies: `pip install -r requirements.txt`
3. Working with Notebook: `alzheimer-cnn-vgg16-93%.ipynb`

## Our Links
- [Final Kaggle Notebook](https://www.kaggle.com/code/karmansinghbains/original-oasis2-alzheimer-with-data-transformation)
- [Published Notebook](https://www.kaggle.com/code/singhjagpreet096/oasis-brain-analysis-with-transfer-learning-vgg16)

## References
- [OASIS Dataset](https://www.oasis-brains.org/)
- [Marcus et al., Open Access Series of Imaging Studies (OASIS), 2010](https://www.ncbi.nlm.nih.gov/pubmed/20950613)