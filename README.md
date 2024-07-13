# Instant Spam Identification via Logistic Regression

This repository not only contains Python code for identifying spam emails using Logistic Regression but also includes functionality for live email collection. Upon receiving an email from a specified address, the system promptly captures the body of the message. This enables dynamic and up-to-date model training. The model is trained on a comprehensive dataset of email messages meticulously labeled as either spam or ham (non-spam). By continuously gathering new email data in real-time, the system ensures that the model remains robust and proficient at distinguishing between legitimate and unsolicited messages, thereby enhancing its effectiveness in combating spam.

## Dependencies

- numpy
- pandas
- scikit-learn

## Installation

You can install the required dependencies using pip:

pip install numpy pandas scikit-learn

## Usage

1. Clone the repository:

git clone https://github.com/ApexLegend9/RT-Spam-Detection.git

2. Ensure you have a CSV file containing email data. By default, the code assumes the file is named `spam.csv` and contains columns named `Message` and `Category` (spam or ham).

3. Run the Jupyter Notebook script:

The script will perform the following steps:

### Data Collection & Pre-Processing

- Load the data from the CSV file into a pandas DataFrame.
- Replace null values with an empty string.
- Label encode the categories: spam as 0, ham as 1.

### Splitting the Data

- Split the data into training and test sets.

### Feature Extraction

- Convert text data into feature vectors using TF-IDF vectorization.

### Training the Model

- Train a Logistic Regression model using the training data.

### Evaluating the Model

- Assess the model's accuracy on both training and test data.

### Building a Predictive System

- Connect to a Gmail account using IMAP.
- Fetch emails from the inbox.
- Predict whether each email is spam or not using the trained model.

## Configuration

- Update the file path in the code to point to your CSV file if it's not named `spam.csv`.
- Adjust the IMAP settings (user, password, imap_url) according to your email provider.
