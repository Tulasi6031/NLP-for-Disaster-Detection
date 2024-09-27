NLP-for-Disaster-Detection
Project Overview
This project aims to build a classifier that automatically categorizes tweets as either disaster-related or not disaster-related. The project uses a BiLSTM (Bi-directional Long Short-Term Memory) network to capture the context and long-term dependencies in tweets. The classifier was developed to help emergency response teams, organizations, and individuals filter through large volumes of social media content and identify critical, real-time disaster information.

The final model is deployed using Streamlit and Huggingface Spaces, allowing users to interact with the model via a web interface or API.

Features
BiLSTM Model: A neural network trained on disaster-related tweets.
Text Preprocessing: Clean and preprocess tweet data for effective model training.
GloVe Embeddings: Pre-trained word embeddings for better semantic understanding.
Real-Time Classification: Classify whether a tweet is disaster-related in real-time.
Scalable API: Model deployed on Huggingface for API access.
Streamlit Interface: User-friendly web application for interacting with the classifier.
Tools & Technologies
pandas for data manipulation
re for text cleaning
PyTorch for defining and training the BiLSTM model
GloVe Embeddings for word representation
Streamlit for web application development
Huggingface Spaces for model deployment
ngrok for testing during development
Installation
Follow these steps to get the project running locally:

Clone the repository:

bash
Copy code
git clone https://github.com/YourGitHubUsername/NLP-for-Disaster-Detection.git
cd NLP-for-Disaster-Detection
Install dependencies: Ensure you have Python 3.7+ installed. Run the following command to install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Run the Streamlit app: Start the web application locally by running:

bash
Copy code
streamlit run app.py
Testing the API: To test the API (deployed on Huggingface), send a tweet for classification via a POST request.

Usage
Using the Streamlit Web App:
Open the web interface by running the Streamlit app.
Enter a tweet in the input box and click "Submit".
The app will display whether the tweet is disaster-related or not.
Using the API:
The model is deployed via an API on Huggingface Spaces. You can submit a tweet to the API, and it will return the classification.

python
Copy code
import requests

API_URL = "https://huggingface.co/your-endpoint-url"
tweet = {"text": "Earthquake just hit downtown!"}

response = requests.post(API_URL, json=tweet)
print(response.json())
File Structure
app.py: The main file that runs the Streamlit web app.
requirements.txt: Lists the dependencies required to run the project.
state_dict.pt: Saved PyTorch model state.
weights_matrix.npy: The pre-trained GloVe embeddings matrix used in the model.
word2idx.pkl: Pickle file storing the word-to-index mapping used for embedding the tweets.
README.md: This documentation file.
Model Details
Architecture: The BiLSTM model processes tweets both forward and backward, capturing the contextual meaning of words. It uses GloVe word embeddings to convert text into numerical representations that the model can process.
Evaluation Metrics: The model was evaluated using accuracy, precision, recall, and F1-score on a test dataset of tweets.
Future Enhancements
Real-Time Tweet Monitoring: Automatically monitor and classify tweets as they are posted during disasters.
Multilingual Support: Expand the model to classify tweets in multiple languages.
Improved Accuracy: Incorporate advanced techniques such as transformers for higher classification accuracy.
