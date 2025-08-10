# Image Classification Project (8 Natural Images)

This project implements a multi-class image classification system using traditional machine learning algorithms to classify images into 8 different categories: airplane, car, cat, dog, flower, fruit, motorbike, and person.

## 📋 Project Overview

The project compares three different machine learning algorithms for image classification:
- **Support Vector Machine (SVM)** - Linear kernel
- **Logistic Regression** - Multi-class classification
- **K-Nearest Neighbors (KNN)** - k=5 neighbors

## 🎯 Dataset

The dataset contains 8 classes of natural images:
- **Airplane**: 581 training, 146 validation images
- **Car**: 774 training, 194 validation images  
- **Cat**: 708 training, 177 validation images
- **Dog**: 561 training, 141 validation images
- **Flower**: 674 training, 169 validation images
- **Fruit**: 800 training, 200 validation images
- **Motorbike**: 630 training, 158 validation images
- **Person**: 788 training, 198 validation images

**Total**: 5,516 training images, 1,383 validation images

## 🏗️ Project Structure

```
Image Classification(8 natural images)/
├── Image_Classification.ipynb.ipynb  # Main Jupyter notebook
├── README.md                         # This file
├── requirements.txt                  # Python dependencies
├── quick_upload.py                   # Google Drive to Git upload script
└── upload_dataset.py                 # Alternative upload script
```

## 🚀 Features

- **Image Preprocessing**: Resizes images to 128x128 pixels and normalizes pixel values
- **Feature Engineering**: Flattens images and applies standardization
- **Multiple Models**: Compares SVM, Logistic Regression, and KNN
- **Comprehensive Evaluation**: 
  - Classification reports with precision, recall, and F1-score
  - Confusion matrices with visual heatmaps
  - Accuracy comparison across models
- **Visualization**: Sample predictions with true vs predicted labels

## 📊 Results

| Model | Accuracy | Best Performing Classes | Challenges |
|-------|----------|------------------------|------------|
| **SVM** | 77% | Fruit (100%), Person (96%), Motorbike (90%) | Cat (53%), Dog (40%) |
| **Logistic Regression** | 75% | Fruit (98%), Person (94%), Motorbike (85%) | Dog (38%), Cat (51%) |
| **KNN** | 63% | Fruit (98%), Person (86%), Airplane (65%) | Dog (17%), Flower (37%) |

## 🛠️ Installation & Setup

1. **Clone or download the project files**

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Dataset Setup Options**:

   ### Option A: Manual Dataset Setup
   - Organize images in the following structure:
   ```
   dataset/
   ├── train/
   │   ├── airplane/
   │   ├── car/
   │   ├── cat/
   │   ├── dog/
   │   ├── flower/
   │   ├── fruit/
   │   ├── motorbike/
   │   └── person/
   └── validation/
       ├── airplane/
       ├── car/
       ├── cat/
       ├── dog/
       ├── flower/
       ├── fruit/
       ├── motorbike/
       └── person/
   ```

   ### Option B: Automatic Google Drive to Git Upload
   
   **Prerequisites:**
   - Install Git LFS: https://git-lfs.github.com/
   - Have your dataset uploaded to Google Drive as a ZIP file
   - Get the Google Drive file ID from the sharing link

   **Steps:**
   1. Get your Google Drive file ID:
      - Upload your dataset to Google Drive as a ZIP file
      - Right-click → Share → Copy link
      - Extract the file ID from the URL (long string between /d/ and /view)
   
   2. Run the upload script:
      ```bash
      python quick_upload.py
      ```
   
   3. Enter your Google Drive file ID when prompted
   
   4. The script will automatically:
      - Download your dataset from Google Drive
      - Extract it to the correct folder structure
      - Setup Git LFS for large files
      - Add, commit, and push to your repository

4. **Update dataset paths** in the notebook (if using manual setup):
   ```python
   train_path = 'path/to/your/dataset/train'
   validation_path = 'path/to/your/dataset/validation'
   ```

## 🎮 Usage

1. **Open the Jupyter notebook**:
   ```bash
   jupyter notebook Image_Classification.ipynb.ipynb
   ```

2. **Run all cells** to execute the complete pipeline:
   - Data loading and preprocessing
   - Model training
   - Evaluation and visualization

## 📈 Key Findings

- **SVM performed best** overall with 77% accuracy
- **Fruit and Person classes** were easiest to classify (98-100% accuracy)
- **Cat and Dog classes** were most challenging (40-53% accuracy)
- **Feature engineering** (standardization) improved model performance
- **Image size** of 128x128 provided good balance between performance and computational cost

## 🔧 Technical Details

- **Image Processing**: PIL for image loading and resizing
- **Feature Extraction**: Flattened RGB pixel values (49,152 features per image)
- **Data Preprocessing**: StandardScaler for feature normalization
- **Model Training**: Scikit-learn implementations
- **Evaluation Metrics**: Accuracy, precision, recall, F1-score, confusion matrices

## 🎨 Visualization

The project includes:
- Confusion matrix heatmaps for each model
- Accuracy comparison bar chart
- Sample prediction visualizations with true vs predicted labels

#### Dataset 
Manual download link: https://drive.google.com/drive/folders/1cCBs3yyzBpZoIz8Sv2cEfp-c1eAXJJGP?usp=sharing





 
