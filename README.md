# NLP for Disaster Detection
> This project classifies tweets as disaster-related or not disaster-related using a BiLSTM model. It provides a real-time web application and an API for classifying tweets during emergencies.

## Features
Real-time tweet classification
BiLSTM Model for sequential data processing
Web app using Streamlit
API hosted on Huggingface Spaces
Installation
Follow these steps to set up the project locally:

1. Clone the repository
   
```shell
git clone https://github.com/YourGitHubUsername/NLP-for-Disaster-Detection.git
```

```shell
cd NLP-for-Disaster-Detection
```

> 2. Install dependencies
Make sure you have Python 3.7+ installed. Run the following command to install the required dependencies:

```shell
pip install -r requirements.txt
```
## Try It Out
You can interact with the model here: Disaster Tweet Classifier on Huggingface

## How to Use
Enter your tweet into the input box.
Click "Classify".
The model will return whether the tweet is disaster-related or not disaster-related.

Example
## Input Tweet:

```shell
#flood #disaster Heavy rain causes flash flooding of streets in Manitou, Colorado Springs areas
```

output
## This tweet is about a real disaster. (Probability: 0.9930)

API Access
The model is also accessible via an API for real-time tweet classification. You can integrate it into your own applications by sending POST requests to the API endpoint.

Example API Usage

```shell
import requests

API_URL = "https://huggingface.co/spaces/tulasi/DisasterPrediction"
tweet = {"text": "Major flooding in the downtown area, people need help!"}

response = requests.post(API_URL, json=tweet)
print(response.json())
```

# File Structure

```shell
.
├── README.md             # Project documentation
├── requirements.txt      # List of dependencies
├── state_dict.pt         # PyTorch model weights
├── weights_matrix.npy    # GloVe embeddings matrix
└── word2idx.pkl          # Word-to-index mapping for embedding
```


Future Enhancements
Real-time monitoring: Integrate the model into real-time Twitter streams to classify tweets automatically as they are posted.
Multilingual Support: Expand the model to support classification in multiple languages.
