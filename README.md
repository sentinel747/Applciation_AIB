
# CRM Classifier Application

## Overview
The **CRM Classifier Application** is a Python-based tool designed to categorize companies based on their CRM data. It uses various NLP techniques, including cosine similarity and machine learning models, to compare company descriptions with predefined categories. The app supports multiple steps, from extracting domain and translating information to providing downloadable classifications.

## Files in This Repository
- `AIB_Applicatio.ipynb`: Main application file, which runs the CRM Classifier tool.
- `Models_comparison.ipynb`: Notebook containing a comparative analysis of 6 different models tested on the same classification task to evaluate their performance.
- `Context Input - Categories.xlsx`: Excel file containing predefined categories and notes to guide classification. This file should have:
  - `Player` column: Lists each category name.
  - `Notes` column: Descriptions or keywords to assist in classifying companies.
- `Data Input - CRM Extraction.xlsx`: Excel file containing CRM data to be classified. This file should have:
  - `Contact E-mail` column: Emails to identify domains.
  - Optional columns like `Contact Name` and `Contact Job Title`.

## Getting Started
1. **Clone this Repository**
   ```bash
   git clone <repository-link>
   cd <repository-folder>
   ```

2. **Install Dependencies**
   Use the `requirements.txt` file to install dependencies. Run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application**
   ```bash
   python AIB_Application.ipynb
   ```
   You can upload `Data Input` and `Context Input` files within the application.

## How to Use
1. **Upload Files**: Click on `Upload CRM Input File` to add your CRM data file and `Upload Context File` for the category file.
2. **Run Analysis**: Once files are uploaded, click `Run Analysis` to begin classification.
3. **Download Results**: After analysis, you can download the classified file in Excel format.

## Classification Model
- **Cosine Similarity**: The default classification method in the main application is based on cosine similarity, which matches company descriptions with predefined categories.
- **Model Comparison**: For a comprehensive evaluation, the file `Models_comparison.ipynb` contains a comparison of 6 different models tested on the same classification task. This notebook is designed to analyze the performance of each model to help identify the most effective one.

## Optional: Enhanced Deduction and Classification with Llama and Phi Models

1. **Business Activity Deduction with Llama Model**: For a more accurate deduction of the business activity before proceeding to classification, you may opt to download the **Llama-3.2-1B-Instruct-Q4_0** model by Bartowski. This model enhances the application's ability to infer the activity based on domain and description information.

2. **Company Classification with Phi Model**: To improve the classification of companies based on the predefined categories, you can download and use the **Phi-3.1-mini-4k-instruct-Q4_K_M** model locally. Set the model's `model_path` in the script to the local file location after downloading it to ensure enhanced classification performance.

## Requirements
- Python 3.7+
- Required libraries: `pandas`, `requests`, `transformers`, `scikit-learn`, `PyQt5`, `tqdm`, `openpyxl`

## Key Features
- **Domain Extraction**: Automatically retrieves the domain from email addresses.
- **Category Classification**: Uses cosine similarity to match company descriptions with predefined categories.
- **Downloadable Report**: Exports the classified data into a downloadable Excel file.
