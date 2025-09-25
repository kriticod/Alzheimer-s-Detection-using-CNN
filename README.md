# Alzheimer's Detection Using CNN with Explainability

## Project Overview
This project implements a Convolutional Neural Network (CNN) for the detection of Alzheimer's disease
using brain MRI scans. It includes explainability techniques to visualize what the model is learning and
how it makes predictions.

## Dataset
This project uses the OASIS (Open Access Series of Imaging Studies) dataset containing brain MRI
scans.
Dataset Source: OASIS Brain MRI Images on Kaggle

## Prerequisites
1. Python 3.8+
2. Google Colab (recommended) or Jupyter Notebook
3. Google Drive account (if using Colab)

##Setup Instructions
1. Download the Dataset
2. Download the dataset from Kaggle
3. You need a Kaggle account to download the dataset
4. Save the downloaded archive.zip file

## Environment Setup
Using Google Colab (Recommended):
1. Upload the project code files to Google Drive
2. Upload the archive.zip dataset to Google Drive
3. Mount Google Drive in Colab:
  
### python
from google.colab import drive
drive.mount('/content/drive')

### Using Local Environment:
1. Install required packages:
bash
pip install numpy pandas matplotlib seaborn tensorflow scikit-learn pillow
opencv-python gradcam
2. Place the archive.zip file in your project directory
3. Extract the Dataset

Run the following code to extract the dataset:

python
import zipfile
import os
#For Google Colab (adjust path as needed)
zip_path = '/content/drive/MyDrive/Research Project/archive.zip'
extract_path = '/content/Research_ProjectData'_
#For local environment (adjust path as needed
#zip_path = 'path/to/archive.zip'
#extract_path = 'Research_ProjectData'
#Create extraction directory if it doesn't exist
os.makedirs(extract_path, exist_ok=True)

#Extract the dataset
with zipfile.ZipFile(zip_path,zip_ref.extractall(extract_path)'r') as zip_ref:
#Verify extraction
print(os.listdir(extract_path))

## Running the Code

1. Open the main notebook (Alzheimers_CNN_Explainability.ipynb) in Google Colab or Jupyter Notebook
2. Make sure to update any file paths in the notebook to match where you extracted the dataset
3. Run the cells in sequential order

## Code Structure
Alzheimers_CNN_Explainability.ipynb: Main notebook containing data preprocessing, modeltraining, evaluation, and explainability techniques

## Explainability Methods Implemented
1. Grad-CAM visualizations for CNN interpretability
2. LIME
3. Expected Results
   
After running the code, you should see:
1. Model training and validation metrics for all the models (accuracy, loss)
2. Confusion matrix for model evaluation
3. Explainability visualizations highlighting regions of interest in brain MRIs
4. Troubleshooting

If you encounter memory issues in Colab, try reducing batch sizes or using Colab Pro
Ensure TensorFlow version is compatible with the code (TF 2.x recommended)
If paths are incorrect, update them according to your specific directory structure

## Additional Notes

The jupyter notebook file is in the .ipynb format for your convenience, however these are the
instructions to run the code again.
