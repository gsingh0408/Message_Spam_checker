# End-to-End Spam Message Classifier

This repository contains the code for an SMS Spam Message Classifier developed using Python and scikit-learn. The model is trained to distinguish between legitimate (ham) and spam text messages.

##  Project Overview

The core of the project is the Jupyter Notebook (`Spam_Message_checker.ipynb`), which performs the following steps:
1.  **Data Loading:** Loads the `SPAM_text.csv` dataset.
2.  **Data Preprocessing:** Cleans and preprocesses the SMS text data.
3.  **Feature Engineering:** Uses **TF-IDF Vectorization** to convert text into numerical features.
4.  **Model Training:** Trains multiple classification models (Logistic Regression, Random Forest, XGBoost) and selects the best performing one.
5.  **Model Persistence:** Saves the final model, TfidfVectorizer, and LabelEncoder using `joblib`.

## Setup and Installation

### Prerequisites

You need Python 3.x installed on your system.

### Steps

1.  **Clone the Repository:**
    ```bash
    git clone <YOUR-REPOSITORY-URL>
    cd <YOUR-REPOSITORY-NAME>
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Get the Dataset:**
    Download the `SPAM_text.csv` file (available on Kaggle) and place it in the project root directory.
    *(See the download link above)*
4.  **Run the Notebook:**
    Open the `Spam_Message_checker.ipynb` file in Jupyter or VS Code to train the model, or use the saved `.joblib` files for prediction.

##  Saved Model Artifacts

The notebook saves the following files to enable fast loading and prediction without re-training:

| File Name | Description |
| :--- | :--- |
| `spam_model_best.joblib` | The trained **best classification model** (e.g., Logistic Regression or XGBoost). |
| `tfidf_vectorizer.joblib` | The fitted **TfidfVectorizer** object needed to transform new messages. |
| `label_encoder.joblib` | The fitted **LabelEncoder** used to convert 'ham'/'spam' to numerical labels. |
| `leaderboard_metrics.csv` | A CSV file containing metrics for all trained models. |

**NOTE:** These files are **generated** when you run the `Spam_Message_checker.ipynb` notebook. If you want to include them in your initial GitHub upload, you must run the entire notebook first, then upload the generated `.joblib` and `.csv` files.