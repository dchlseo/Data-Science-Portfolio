# Ethics Justice Data Project

## Project Overview

This project focuses on analyzing the 'Ethics Justice' ([data source](https://github.com/hendrycks/ethics)) dataset using advanced natural language processing techniques. The primary objective is to classify scenarios based on ethical considerations using a pre-trained DistilBERT model. The project involves data preparation, model training, validation, and evaluation phases, with an emphasis on understanding the nuances of ethical judgments in textual data.

## Code Structure

### Importing Packages and Data

- **PyTorch and Transformers**: Utilizes PyTorch for deep learning and Hugging Face's Transformers for pre-trained models.
- **Data Handling**: Employs Pandas and NumPy for data manipulation.
- **Data Loading**: Reads the training, testing, and hard testing datasets from CSV files.

Data Example

<img width="899" alt="image" src="https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/55809d86-67b1-4fd6-80e6-050cc21198d8">

Data Labels

<img width="594" alt="image" src="https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/c3ae6eb5-85c9-4510-9ac4-35b0945dc3f1">



### Preparing Data

- **Tokenizer Function**: Retrieves a tokenizer for a given model name.
- **Model Loader**: Loads a sequence classification model with a specified number of labels.
- **Data Preparation**: Tokenizes the data and creates attention masks, converting them into PyTorch tensors. Splits the data into training and validation sets if required.

### Model Training (and Saving)

- **Training Function**: Trains the model using the specified optimizer (AdamW, Adam, or SGD). The function includes a learning rate scheduler and an option to save the trained model.
- **Validation**: Evaluates the model on the validation dataset to monitor performance during training.

### Model Evaluation

- **Evaluation Function**: Assesses the model's performance on a given dataset, calculating the average accuracy.

### Data Processing and Model Execution

- **Initialization**: Sets up the model, tokenizer, and data loaders for training, validation, and testing datasets.
- **Model Training Execution**: Trains and validates the model, then saves the trained model.
- **Model Testing**: Evaluates the model on both the standard test set and the more challenging test-hard set.

## Usage Instructions

1. **Data Preparation**: Ensure that the training, testing, and hard testing data are available in the specified directories.
2. **Model Selection**: Choose an appropriate pre-trained model (e.g., 'distilbert-base-uncased').
3. **Training the Model**: Run the training process with the desired hyperparameters (e.g., learning rate, epochs).
4. **Evaluation**: Evaluate the model on both the test and test-hard datasets to understand its performance.

## Dependencies

- Python 3.x
- PyTorch
- Transformers library
- Pandas
- NumPy
- Scikit-learn

## Notes

- The model's performance may vary based on the chosen hyperparameters and the specific pre-trained model used.
- The training process can be computationally intensive and may require a GPU for efficient execution.
