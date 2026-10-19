# SMS Spam Detector

## Project Overview
SMS Spam Detector is a Machine Learning and Natural Language Processing (NLP) project that classifies text messages as Spam or Legitimate (Ham). It also highlights suspicious phrases and gives safety advice to the user.

## Features
- Classifies SMS messages as Spam or Legitimate.
- Cleans text (lowercase, URL and punctuation removal) before prediction.
- Uses TF-IDF to convert text into numerical features.
- Uses a Random Forest model (about 97.7% accuracy on the test set).
- Shows suspicious phrases found in the message (e.g. urgent, password, OTP).
- Gives an explanation and safety recommendations.
- Streamlit web interface for testing messages.

## Dataset
SMS Spam Collection dataset (UCI) - 5,572 labeled messages (ham/spam).

## Project Files
- `app.py` - Streamlit web application.
- `spam_detector_app.zip` - Complete application package (`app.py`, `spam_model.pkl`, `tfidf.pkl`, `requirements.txt`).
- `spam_model.pkl` - Trained Random Forest model.
- `tfidf.pkl` - Saved TF-IDF vectorizer.
- `requirements.txt` - Required Python libraries.
- `final_examination.ipynb` - Notebook with training, evaluation and results.
- `README.md` - Project documentation.

## Technologies Used
Python, Scikit-learn, Pandas, NLP, TF-IDF, Random Forest, Streamlit, Joblib

## How to Run
1. Download and extract `spam_detector_app.zip`.
2. Install the libraries:
   ```bash
   python -m pip install -r requirements.txt
   ```
3. Make sure `app.py`, `spam_model.pkl` and `tfidf.pkl` are in the same folder.
4. Start the app:
   ```bash
   streamlit run app.py
   ```

## How It Works
1. The user pastes an SMS message.
2. The text is cleaned and converted to numbers with TF-IDF.
3. The Random Forest model predicts Spam or Legitimate.
4. The app shows the result, risk level, suspicious phrases, explanation and safety tips.

## Results
| Metric | Value |
|---|---|
| Accuracy | 97.67% |
| Spam precision | 1.00 |
| Spam recall | 0.83 |

## Limitations
The model misses some spam messages (recall 0.83), so a "Legitimate" result does not guarantee a message is safe. Always verify the sender through an official source and never share passwords or OTPs.

## Author
Aqsa Soomro
