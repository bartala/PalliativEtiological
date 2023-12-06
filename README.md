# 🌟Identifying Palliative and Etiological Drugs🌟

### 📚 **Documentation**
_For a detailed explanation of the project, please refer to our **paper**(should be linked?)

# 🚀 **Quick Start**
  Before executing the colab nodebook, follow these steps for a smooth experience:

## **I. Initial Setup and Preparation**
- ### Selecting the Hardware Accelerator
  - In the Colab menu, navigate to "Runtime" -> "Change runtime type".
  - Choose "GPU" as your Hardware accelerator to ensure optimal performance.

- ### Python Version Check
  - Confirm your Python version by executing `!python --version` in a new cell.
  - This notebook is ideally run on Python 3.10.

- ### Accessing Necessary Files
  - All necessary files, including datasets and embeddings, are available in our GitHub repository.
  - Download these and upload them to your Google Drive in a structured directory (e.g., "/content/drive/MyDrive/project/GNN/").

- ### Mounting Google Drive
  - Mount your Google Drive to this notebook to access the files. Instructions are provided in the following cell.
  - As an alternative, you can upload files to Colab's local disk, but note that these will be lost if the Colab session restarts.

## **II. Using Pre-generated Resources**
- ### Pre-generated Embeddings
  - Generating embeddings for the GNN model can be quite time-consuming.
  - To expedite the process, you may choose to use pre-generated embeddings from our GitHub repository.
  - Instructions for using these embeddings are provided in the relevant sections of this notebook.

- ### Pre-finetuned SciBERT Model
  - Finetuning the SciBERT model is also a resource-intensive task, requiring significant time.
  - As a convenient alternative, we offer a pre-finetuned SciBERT model available in our GitHub repository.
  - You can directly use this model, skipping the finetuning step. Details on how to do this are included in the notebook.
  - Please note: The pre-finetuned SciBERT model is specifically designed for generating embeddings for the GNN model. It is not intended for comparison with the GNN.

## **III. Comparing GNN Model and SciBERT**
- ### Fine-Tuning for Comparison
  - To effectively compare the performance between the GNN model and SciBERT, it's essential to fine-tune both using the 10-fold cross-validation process.
  - Detailed instructions for fine-tuning SciBERT using 10-fold cross-validation are provided in the respective sections of this notebook.

## **IV. Important Note on Model Fine-Tuning**
- ### Requirement for Self Fine-Tuning
  - Due to our use of 10-fold cross-validation (10CV) for model comparison, it's necessary for you to fine-tune the SciBERT model yourself, rather than using a single pre-finetuned model we provided in GitHub.
  - The 10CV process involves training and evaluating the model on different subsets of the data across 10 iterations, which cannot be replicated with a pre-finetuned model designed for a single dataset split.
  - This step ensures that each model is optimized and evaluated under similar conditions, allowing for a fair and meaningful comparison.
  - We provide detailed steps in the notebook for fine-tuning the SciBERT model using 10-fold cross-validation to facilitate this process.

- ### Why Not Use a Pre-Finetuned Model?
  - Using a single pre-finetuned model does not align with the 10CV methodology, as it would only reflect the model's performance on one specific training-validation split.
  - To maintain the integrity of the comparative analysis between the GNN model and SciBERT, each model must undergo the same 10-fold cross-validation process.
