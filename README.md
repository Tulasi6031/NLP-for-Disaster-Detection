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

3. Install dependencies
Make sure you have Python 3.7+ installed. Run the following command to install the required dependencies:

bash
Copy code
pip install -r requirements.txt
3. Run the Streamlit app
Start the web application on your local machine by running:

bash
Copy code
streamlit run app.py
You can now access the app in your browser to classify tweets in real time.

Usage
Web Application
Enter a tweet into the input box.
Click the "Submit" button to classify the tweet.
The app will return whether the tweet is disaster-related or not.
API
You can interact with the model via an API deployed on Huggingface Spaces. Send a POST request with a tweet, and the API will return the classification.

python
Copy code
import requests

API_URL = "https://huggingface.co/your-endpoint-url"
tweet = {"text": "Earthquake just hit downtown!"}

response = requests.post(API_URL, json=tweet)
print(response.json())
File Structure
bash
Copy code
.
├── app.py                # Streamlit app
├── README.md             # Project documentation
├── requirements.txt      # List of dependencies
├── state_dict.pt         # PyTorch model weights
├── weights_matrix.npy    # GloVe embeddings matrix
└── word2idx.pkl          # Word-to-index mapping for embedding
Future Improvements
Real-time tweet stream classification
Multi-language tweet classification
Performance optimization using Transformer models
