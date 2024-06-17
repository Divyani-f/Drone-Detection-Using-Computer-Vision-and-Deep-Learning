# Drone Detection Using Ensemble Learning

## Overview
This project implements a drone detection system using ensemble learning techniques to enhance accuracy and robustness. The system leverages the OpenCV library for data preprocessing and integrates two state-of-the-art TensorFlow models: Single Shot Multibox Detector (SSD) and EfficientDet. The project explores the effectiveness of ensemble learning by combining predictions from both models to achieve superior drone detection performance.

## Architecture

### Implementation
- **Preprocessing**: Utilized OpenCV to preprocess the data, modifying the code to obtain different outputs.
- **Testing**: Implemented a comprehensive, consistent, and repeatable testing methodology.

### Dataset
- **Source**: [Drone Dataset from Kaggle](https://www.kaggle.com/datasets/dasmehdixtr/drone-dataset-uav)
- **Content**: Contains 1359 labeled photos with both `.txt` and `.xml` annotation files suitable for TensorFlow-based models.

### Methodology
1. **Data Collection and Annotation**: Assembled a dataset featuring drone images with corresponding XML annotations for box coordinates.

   ![XML Screenshot](path/to/xml_screenshot.png)  <!-- Replace with actual path -->

2. **Dataset Partitioning**: Divided the annotated dataset into training and testing sets.
3. **Model Selection and Configuration**: Chose pre-trained SSD and EfficientDet models, adapting configurations such as step size, batch size, dropout, and normalization layers to fit the custom drone dataset.

### Ensemble Learning
- Integrated SSD and EfficientDet models to leverage their complementary strengths.
- Averaged predictions from both models to enhance detection accuracy and robustness.
- This ensemble approach mitigates individual model weaknesses, resulting in a more accurate final detection output.

### Data Preprocessing
- **Steps**: Resizing, normalization, and noise removal using OpenCV.
- **Image Size**: Adjusted to 256x256 for computational efficiency.

   ![Before Image](path/to/before_image.png)  <!-- Replace with actual path -->
   ![After Image](path/to/after_image.png)  <!-- Replace with actual path -->

### Model Training and Evaluation
- Fine-tuned SSD and EfficientDet models using the custom dataset.
- Enhanced prediction accuracy by averaging model predictions through ensemble learning.
- Improved system adaptability and generalization for effective drone detection across various scenarios.

## Getting Started

### Prerequisites
- Python 3.x
- OpenCV
- TensorFlow
- NumPy

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/drone-detection-ensemble.git
   cd drone-detection-ensemble
