📌 **Overview:** <br>
Social media platforms have become central to modern communication but also serve as venues for hate speech and cyberbullying. Manual moderation is often insufficient to address the volume and complexity of such content. "Hate Speech Hunter" is an AI-driven system designed to detect hate speech in Tamil text, leveraging advanced natural language processing models to automate moderation and foster safer online environments.

🚀 **Approach & Technologies Used** <br><br>
🧠 **Machine Learning & Deep Learning Models**
**IndicBERT:** A transformer-based model pre-trained on 12 major Indian languages, including Tamil. IndicBERT is optimized for performance with fewer parameters compared to other multilingual models.

**LSTM (Long Short-Term Memory):** Utilized for sequence classification tasks to identify patterns indicative of hate speech.

**Random Forest & Logistic Regression:** Employed as baseline models to benchmark performance.

**TF-IDF Vectorization:** Applied for feature extraction to convert textual data into meaningful numerical representations.

🗂 **Dataset** <br>
**Data Collection**: The dataset comprises Tamil comments sourced from YouTube using the YouTube Comment Downloader tool.

**Preprocessing Steps:** Removal of stop words to reduce noise, Stemming to normalize words to their root forms, Handling of special characters and punctuation to clean the text data.

**📊 Model Training & Evaluation** <br>
Training Process: Models were trained on the preprocessed dataset, with hyperparameters tuned for optimal performance.

**Evaluation Metrics:** <br>

✅ Accuracy

✅ Precision

✅ Recall

✅ F1-score

These metrics provide a comprehensive assessment of the model's performance in detecting hate speech.

🔍 **Key Findings & Challenges**
Performance: IndicBERT outperformed traditional machine learning models, effectively capturing the nuances of Tamil-specific hate speech.

Challenges: Handling noisy text, dialect variations, and code-mixed Tamil-English content remains challenging and requires further research.

🔧 **Installation**
To set up the Hate Speech Hunter project locally:

# Clone the repository
git clone https://github.com/SSHarshitha/Hatespeech_detection_indicBert.git
cd Hatespeech_detection_indicBert

# Install dependencies
pip install -r requirements.txt
🚀 Usage
After installation, you can utilize the trained model to detect hate speech in Tamil text. Here's a basic example:

python
Copy
Edit
from model_build import predict_hate_speech

# Sample text
text = "உங்கள் உதவியால், நாங்கள் வெற்றியடைவோம்."

# Prediction
result = predict_hate_speech(text)
print(f"Prediction: {'Hate Speech' if result else 'Not Hate Speech'}")
