# NinjaCart Image Classification – Business Case

## Topic
Convolutional Neural Networks (CNN)

## Problem Statement

Ninjacart is India’s largest fresh produce supply chain company, leveraging technology to optimize sourcing and delivery of vegetables within 12 hours. A key component of their automation pipeline is a robust image classification system capable of distinguishing between different vegetable types and identifying irrelevant images as noise.

The objective of this project is to build a multi-class classifier that categorizes images into:

- Tomato  
- Potato  
- Onion  
- Noise (Indian market scenes)

The dataset provided contains structured train and test folders with four subfolders corresponding to each class.

Dataset Link:
https://drive.google.com/file/d/1clZX-lV_MLxKHSyeyTheX5OCQtNCUcqT/view?usp=sharing

---

## Dataset Context

The dataset consists of images scraped from Google and includes:

### Training Set (Total: 3135 images)
- Tomato: 789  
- Potato: 898  
- Onion: 849  
- Indian Market (Noise): 599  

### Test Set (Total: 351 images)
- Tomato: 106  
- Potato: 83  
- Onion: 81  
- Indian Market (Noise): 81  

Since no validation set is provided, an 80–20 split is performed on the training data for proper model tuning.

---

## Objective

Develop a CNN-based multi-class classifier that:

- Accurately identifies vegetable types  
- Correctly classifies non-vegetable images as noise  
- Generalizes well on unseen test data  
- Minimizes overfitting  

---

## Concepts Tested

- Dataset Preparation and Visualization  
- CNN Model Development  
- Transfer Learning  
- Overfitting Mitigation  
- Implementation of Training Callbacks  

---

## Project Workflow

### 1. Data Preparation and Exploration

- Imported and inspected dataset structure  
- Verified class distribution  
- Visualized sample images from each category  
- Checked image dimensions  
- Plotted histogram of class counts  

### 2. Dataset Splitting

- Performed 80–20 train-validation split  
- Ensured balanced representation across classes  

### 3. Preprocessing

- Resized images to uniform square dimensions  
- Normalized pixel values to range [0, 1]  
- Applied data augmentation to improve robustness  

### 4. Model Development

- Built a baseline CNN classifier  
- Improved architecture to reduce overfitting  
- Implemented Batch Normalization and Dropout  
- Applied transfer learning using pretrained architectures  
- Integrated callbacks such as EarlyStopping, ModelCheckpoint, and TensorBoard  

### 5. Evaluation

- Measured test accuracy  
- Generated confusion matrix for class-wise analysis  
- Plotted training and validation accuracy and loss curves  
- Performed random sample predictions  

---

## Evaluation Criteria (100 Points)

### Dataset Import and Exploration (10 Points)
- Verified structure and characteristics of the dataset  

### Exploratory Data Analysis (20 Points)
- Class distribution visualization  
- Image dimension analysis  
- Train-validation-test split  

### Model Architecture and Training (50 Points)
- Defined CNN from scratch  
- Improved baseline to reduce overfitting  
- Implemented training callbacks  
- Fine-tuned pretrained models  
- Plotted metrics and confusion matrix  

### Testing and Insights (20 Points)
- Evaluated on test dataset  
- Performed random image predictions  
- Provided summary and insights  

---

## Outcome

The final model demonstrates effective classification of vegetable categories while accurately identifying noise images, simulating a real-world automation solution for supply chain image processing.
