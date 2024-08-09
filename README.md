This project aims to compare the performance of two machine learning models, a generative model and a discriminative model, for toxicity classification 
in text comments. The generative model generates text comments, while the discriminative model classifies comments as toxic or non-toxic. 

This README provides a brief introduction to the project and instructions for running the program.

How to Run the Program

Environment Setup
Open Google Colab: Go to Google Colab and sign in with your Google account.
Create a New Notebook: Click on "File" -> "New Python 3 Notebook" to create a new Colab notebook.
Import the Dataset: If your dataset is stored locally, you will need to upload it to Colab. You can do this by clicking on the folder icon on the left sidebar, then clicking on the "Upload" button.
Mount Google Drive (Optional): If your dataset is stored on Google Drive, you can mount your Google Drive in Colab using the following code:



from google.colab import drive
drive.mount('/content/drive')

Running the Program
Install Dependencies: Run the following code to install the necessary Python packages:

!pip install transformers
Training the Models: Prepare your dataset and train both the generative and discriminative models using the provided scripts. Replace path_to_train_data.csv and path_to_validation_data.csv with the paths to your training and validation datasets.
For the generative model:

!python train_generative_model.py --train_data_path path_to_train_data.csv --validation_data_path path_to_validation_data.csv

!python train_discriminative_model.py --train_data_path path_to_train_data.csv --validation_data_path path_to_validation_data.csv

!python evaluate_generative_model.py --test_data_path path_to_test_data.csv
