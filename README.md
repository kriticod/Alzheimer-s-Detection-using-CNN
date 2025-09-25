# Alzheimer-s-Detection-using-CNN
This project implements a Convolutional Neural Network (CNN) for the detection of Alzheimer's disease using brain MRI scans. It includes explainability techniques to visualize what the model is learning and how it makes predictions.

Alzheimer's Detection Using CNN with Explainability
Project Overview
This project implements a Convolutional Neural Network (CNN) for the detection of Alzheimer's disease
using brain MRI scans. It includes explainability techniques to visualize what the model is learning and
how it makes predictions.
Dataset
This project uses the OASIS (Open Access Series of Imaging Studies) dataset containing brain MRI
scans.
Dataset Source: OASIS Brain MRI Images on Kaggle
Prerequisites
●
●
●
Python 3.8+
Google Colab (recommended) or Jupyter Notebook
Google Drive account (if using Colab)
Setup Instructions
1. Download the Dataset
1. 2. 3. Download the dataset from Kaggle
You need a Kaggle account to download the dataset
Save the downloaded archive.zip file
2. Environment Setup
●
Using Google Colab (Recommended):
1. 2. Upload the project code files to Google Drive
Upload the archive.zip dataset to Google Drive
Mount Google Drive in Colab:
python
from google.colab import drive
3. drive.mount('/content/drive')
●
Using Local Environment:
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
# For Google Colab (adjust path as needed)
zip_path = '/content/drive/MyDrive/Research Project/archive.zip'
extract
_path = '/content/Research
_
Project
Data'
_
# For local environment (adjust path as needed)
# zip_path = 'path/to/archive.zip'
# extract
_path = 'Research
_
Project
Data'
_
# Create extraction directory if it doesn't exist
os.makedirs(extract
_path, exist
_
ok=True)
# Extract the dataset
with zipfile.ZipFile(zip_path,
zip_
ref.extractall(extract
_path)
'r') as zip_
ref:
# Verify extraction
print(os.listdir(extract
_path))
Running the Code
1. 2. 3. Open the main notebook (Alzheimers
CNN
_
_
Explainability.ipynb) in Google Colab or Jupyter
Notebook
Make sure to update any file paths in the notebook to match where you extracted the dataset
Run the cells in sequential order
Code Structure
●
Alzheimers
CNN
_
_
Explainability.ipynb: Main notebook containing data preprocessing, model
training, evaluation, and explainability techniques
Explainability Methods Implemented
●
●
Grad-CAM visualizations for CNN interpretability
LIME
Expected Results
After running the code, you should see:
●
●
●
Model training and validation metrics for all the models (accuracy, loss)
Confusion matrix for model evaluation
Explainability visualizations highlighting regions of interest in brain MRIs
Troubleshooting
●
●
●
If you encounter memory issues in Colab, try reducing batch sizes or using Colab Pro
Ensure TensorFlow version is compatible with the code (TF 2.x recommended)
If paths are incorrect, update them according to your specific directory structure
Additional Notes
●
The jupyter notebook file is in the .ipynb format for your convenience, however these are the
instructions to run the code again.
