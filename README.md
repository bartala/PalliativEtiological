# 🧬💊 Elucidating Drug Mechanisms: Etiological \& Palliative 💊🧬


## 📚 **Overview**
This repository contains code and links to the datasets necessary to run the DruGNNosis-MoA Classifier model. This model predicts novel drug mechanisms as etiological or palliative using node embeddings in heterogeneous graph.

### Motivation
Understanding the relationships between drugs, genes, and diseases is crucial for effectively developing and selecting treatments. Our model aims to differentiate between two types of drug mechanisms: etiological (targeting disease causes or contributing factors) and palliative (alleviating symptoms). Despite its significance in drug design and repurposing, this distinction has not been extensively explored.

### Results
We compiled a comprehensive dataset of 2,018 FDA-approved drugs, including their target genes, protein interactions, and disease associations, sourced from three biomedical databases. This dataset was enriched with manually annotated mechanisms of action (MOA). Utilizing this data, we created a heterogeneous network linking drugs, genes, and diseases, revealing notable patterns such as the prevalence of follow-on drugs (targeting the same genes). We evaluated three Machine Learning models - a fine-tuned SciBERT language model, a basic Graph Neural Network (GNN), and a DruGNNosis-MoA (hybrid GNN-SciBERT model)- for classifying drug MOAs. The hybrid model demonstrated superior performance, achieving an F1-score of  0.942 in identifying drug MOAs.


## 🔗 **Resources**
Access the necessary resources for this project:
- **Supplementary**: [Download Drug Annotations](https://github.com/bartala/PalliativEtiological/tree/main/Supplementary)

- **DrugBank DataSet** (In the project we used Approved Drugs Version 5.1.10): [Download DrugBank Dataset](https://go.drugbank.com/releases/latest#protein-identifiers)
- **OMIM DataSet** (In the project we used morbidmap.txt downloaded May 1, 2023): [Download OMIM Dataset](https://www.omim.org/downloads)
- **BioGrid DataSet** (In the project we used BIOGRID-ORGANISM-Homo_sapiens-4.4.217.tab3.txt): [Download BioGrid Dataset](https://downloads.thebiogrid.org/File/BioGRID/Release-Archive/BIOGRID-4.4.217/BIOGRID-ORGANISM-4.4.217.tab3.zip)

## 🚀 **Quick Start**
  Before executing the colab nodebook, follow these steps for a smooth experience:

## I. Initial Setup and Preparation
- ### Selecting the Hardware Accelerator
  - Navigate to "Runtime" -> "Change runtime type" in the Colab menu.
  - Choose "GPU" as your hardware accelerator for optimal performance.

- ### Python Version Check
  - Execute `!python --version` in a new cell to confirm your Python version.
  - This notebook is optimized for Python 3.10.

- ### Mounting Google Drive / Colab's local disk
  - Mount your Google Drive to access the files.
  - Alternatively, upload files to Colab's local disk.

- ### Run Code
  To run specific sections or the entire code efficiently, follow these guidelines:
  
  - **Initial Setup:** 
    - Begin with the setup instructions to establish the necessary environment. 
    - Make sure the paths for all required files are correctly set.

  - **Running Specific Sections (Sections 2-9 from Palliativ_Etiological_Source_Code.ipynb notebook):**
    - **File Dependencies:** 
      - Check each section's instructions for its file requirements.
      - Ensure these files are loaded and their paths are correctly set.
    - **Independence of Sections:** 
      - Sections can run independently, **except for section 7**, which needs the 10-fold CV SciBert. Confirm that all necessary files for each section are available.
    - **Note:**
      - Before running a specific section, it is essential to verify that all classes, methods, and files required by that section are correctly loaded and executed.

  - **Running the Entire Notebook:**
    - Go to "Runtime" in the Colab menu and select "Run all".

  - **Source of Files:** 
    - Store necessary files in your Google Drive or Colab's local disk.

### **II. Using Pre-generated Resources**
- #### Pre-generated Embeddings
  - Generating embeddings for the GNN model can be quite time-consuming.

### **III. Fine-Tuned SciBERT Model**
  - Please note: To initialize the tokenizer for the SciBERT model, the use of an access token is optional.
    While an access token can be used (obtainable from your Hugging Face account), it's not mandatory for accessing public models like SciBERT.
    If you have an access token, assign it to the variable `access_token`. Otherwise, set the variable to `None`.

### **IV. Comparing  Model and SciBERT**
- #### Fine-Tuning for Comparison
  - To effectively compare the performance between the DruGNNosis-MoA model and SciBERT, it's essential to fine-tune both using the same 10-fold cross-validation process.
  - Detailed instructions for fine-tuning SciBERT using 10-fold cross-validation are provided in the respective sections of 'PalliativeEtiolgical.pynb' notebook.

## 📌 **Miscellaneous**
For any inquiries about the code or the algorithm, please contact alon.bartal@biu.ac.il.

## 📖 **Citing**
If you find DruGNNosis-MoA useful in your research, please consider citing our work:
```
@article{brettler2024drugnosis,
  author    = {Brettler, L. and Berman, E. and Jagodnik, Kathleen M. and Bartal, A.},
  title     = {DruGNNosis-MoA: Elucidating Drug Mechanisms as Etiological or Palliative With Graph Neural Networks Employing a Large Language Model},
  journal   = {IEEE Journal of Biomedical and Health Informatics},
  year = {2025},
  publisher={IEEE}
}
```
