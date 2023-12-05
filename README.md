# Disfluency-ICON

Contains scripts and Models for the Shared Task in ICON 2023 - Disfluency Identification for 6 Indian Languages 2023


Repository Contains 

* Scripts
* Scripts
* Data

## Scripts
Scripts contain 2 Jupyter Notebooks and 1 python script
	* Split-50.py 
		This introduces a line break after every 50 tokens
This will enable us to load data that does not have any clear end of sentence markers.
	Change the following label to the required file

	* Train File
		Fine Tunes a selected model on the train data and evaluate it on the dev data. Change the following label at the top of the script accorndingly.
		
File paths
dev_file = '/content/drive/MyDrive/Disfluency Task/Training_Data_Split_50/tamil/tamil_train_50.tsv'
train_file = '/content/drive/MyDrive/Disfluency Task/Training_Data_Split_50/tamil/tamil_train_50.tsv'


model_checkpoint = "bert-base-multilingual-cased"
batch_size = 16
max_sequence_length = 256
task = "disfluency"
epochs = 5

model_save_location="/content/drive/MyDrive/Disfluency Task/Model/Tamil-Bert"

	* Test File

Load the model at 'model_save_location' from the previous step and run testing on the test data (split.py run on the test file as well)
	
Modify the location of the model and of the test files 

## Model
All the Models created by the train script - One for each language

## Data
Contains all the train dev & test data for all 6 languages
