# 🧬💊 Elucidating Drug Mechanisms: Etiological \& Palliative 💊🧬


## 📚 **Overview**
This repository contains code and links to the datasets necessary to run the HeteroSciGNN Classifier model. This model predicts novel drug mechanisms as etiological or palliative using node embeddings in heterogeneous graph.

### Motivation
Understanding the relationships between drugs, genes, and diseases is crucial for effectively developing and selecting treatments. Our model aims to differentiate between two types of drug mechanisms: etiological (targeting disease causes or contributing factors) and palliative (alleviating symptoms). Despite its significance in drug design and repurposing, this distinction has not been extensively explored.

### Results
We compiled a comprehensive dataset of 2,018 FDA-approved drugs, including their target genes, protein interactions, and disease associations, sourced from three biomedical databases. This dataset was enriched with manually annotated mechanisms of action (MOA). Utilizing this data, we created a heterogeneous network linking drugs, genes, and diseases, revealing notable patterns such as the prevalence of follow-on drugs (targeting the same genes). We evaluated three Machine Learning models - a fine-tuned SciBERT language model, a basic Graph Neural Network (GNN), and a HeteroSciGNN (hybrid GNN-SciBERT model)- for classifying drug MOAs. The hybrid model demonstrated superior performance, achieving an F1-score of 0.934 in identifying drug MOAs.


## 🔗 **Resources**
Access the necessary resources for this project:

- **Datasets**: [Download Datasets](link-to-datasets)
- **Pre-generated Embeddings**: [Download Embeddings](link-to-embeddings)
- **Pre-finetuned SciBERT Model**: [Download Model](link-to-model)

## 🚀 **Quick Start**
  Before executing the colab nodebook, follow these steps for a smooth experience:

## I. Initial Setup and Preparation
- ### Selecting the Hardware Accelerator
  - Navigate to "Runtime" -> "Change runtime type" in the Colab menu.
  - Choose "GPU" as your hardware accelerator for optimal performance.

- ### Python Version Check
  - Execute `!python --version` in a new cell to confirm your Python version.
  - This notebook is optimized for Python 3.10.

- ### Accessing Necessary Files
  - All required files, including datasets and embeddings, are in our GitHub repository.
  - Download these files and upload them to your Google Drive in a structured directory, like "/content/drive/MyDrive/project/PalliativEtiological/".

- ### Mounting Google Drive / Colab's local disk
  - Mount your Google Drive to access the files.
  - Alternatively, upload files to Colab's local disk.

- ### Run Code
  To run specific sections or the entire code efficiently, follow these guidelines:
  
  - **Initial Setup:** 
    - Begin with the setup instructions to establish the necessary environment. 
    - Make sure the paths for all required files are correctly set.

  - **Running Specific Sections (Sections 2-9):**
    - **File Dependencies:** 
      - Check each section's instructions for its file requirements.
      - Ensure these files are loaded and their paths are correctly set.
    - **Independence of Sections:** 
      - Sections can run independently, **except for section 7**, which needs the 10-fold CV SciBert. Confirm that all necessary files for each section are available.


  - **Running the Entire Notebook:**
    - Go to "Runtime" in the Colab menu and select "Run all".
    - **Key File Check:** Ensure `comprehensive_dataset.csv.gz` is available and loaded, as it's critical for the entire notebook.

  - **Source of Files:** 
    - Download necessary files from our GitHub repository.
    - Store them correctly in your Google Drive or Colab's local disk.

### **II. Using Pre-generated Resources**
- #### Pre-generated Embeddings
  - Generating embeddings for the GNN model can be quite time-consuming.
  - To expedite the process, you may choose to use pre-generated embeddings from our GitHub repository.
  - Instructions for using these embeddings are provided in the relevant sections of this notebook.

### **III. Fine-Tuned SciBERT Model**
  - Please note: To initialize the tokenizer for the SciBERT model, the use of an access token is optional.
    While an access token can be used (obtainable from your Hugging Face account), it's not mandatory for accessing public models like SciBERT.
    If you have an access token, assign it to the variable `access_token`. Otherwise, set the variable to `None`.

### **IV. Comparing HeteroSciGNN Model and SciBERT**
- #### Fine-Tuning for Comparison
  - To effectively compare the performance between the HeteroSciGNN model and SciBERT, it's essential to fine-tune both using the 10-fold cross-validation process.
  - Detailed instructions for fine-tuning SciBERT using 10-fold cross-validation are provided in the respective sections of 'PalliativeEtiolgical.pynb' notebook.

## 📌 **Miscellaneous**
For any inquiries about the code or the algorithm, please contact alon.bartal@biu.ac.il.

## 📖 **Citing**
If you find HeteroSciGNN useful in your research, please consider citing our work:

@article{??????
}
