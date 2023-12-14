# 🧬💊 Elucidating Drug Mechanisms: Etiological \& Palliative 💊🧬


## 📚 **Overview**
This repository contains code and links to the datasets necessary to run the HeteroSciGNN Classifier model. This model predicts novel drug mechanisms as etiological or palliative using node embeddings in heterogeneous graphs.

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

- ### Mounting Google Drive
  - Mount your Google Drive to access the files, following the instructions in the next cell.
  - Alternatively, upload files to Colab's local disk, but they will be lost if the session restarts.

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

- #### Pre-finetuned SciBERT Model
  - Finetuning the SciBERT model is also a resource-intensive task, requiring significant time.
  - As a convenient alternative, we offer a pre-finetuned SciBERT model available in our GitHub repository.
  - You can directly use this model, skipping the finetuning step. Details on how to do this are included in the notebook.
  - Please note: The pre-finetuned SciBERT model is specifically designed for generating embeddings for the HeteroSciGNN model. It is not intended for comparison with the HeteroSciGNN model.

### **III. Comparing HeteroSciGNN Model and SciBERT**
- #### Fine-Tuning for Comparison
  - To effectively compare the performance between the HeteroSciGNN model and SciBERT, it's essential to fine-tune both using the 10-fold cross-validation process.
  - Detailed instructions for fine-tuning SciBERT using 10-fold cross-validation are provided in the respective sections of this notebook.

### **IV. Important Note on Model Fine-Tuning**
- #### Requirement for Self Fine-Tuning
  - Due to our use of 10-fold cross-validation (10CV) for model comparison, it's necessary for you to fine-tune the SciBERT model yourself, rather than using a single pre-finetuned model we provided in GitHub.
  - The 10CV process involves training and evaluating the model on different subsets of the data across 10 iterations, which cannot be replicated with a pre-finetuned model designed for a single dataset split.
  - This step ensures that each model is optimized and evaluated under similar conditions, allowing for a fair and meaningful comparison.
  - We provide detailed steps in the notebook for fine-tuning the SciBERT model using 10-fold cross-validation to facilitate this process.

- #### Why Not Use a Pre-Finetuned Model?
  - Using a single pre-finetuned model does not align with the 10CV methodology, as it would only reflect the model's performance on one specific training-validation split.
  - To maintain the integrity of the comparative analysis between the HeteroSciGNN Classifier and SciBERT, each model must undergo the same 10-fold cross-validation process.
 
## 📌 **Miscellaneous**
For any inquiries about the code or the algorithm, please contact alon.bartal@biu.ac.il.

## 📖 **Citing**
If you find HeteroSciGNN useful in your research, please consider citing our work:

@article{??????
}
