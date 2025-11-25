# 🎥 YouTube Sentiment Insights

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.0%2B-black?style=for-the-badge&logo=flask&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-Model-green?style=for-the-badge)
![DVC](https://img.shields.io/badge/DVC-Data%20Version%20Control-9cf?style=for-the-badge&logo=dvc&logoColor=white)
![Chrome Extension](https://img.shields.io/badge/Chrome%20Extension-v3-yellow?style=for-the-badge&logo=google-chrome&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)

**YouTube Sentiment Insights** is a powerful end-to-end machine learning application designed to analyze the sentiment of YouTube comments in real-time. It combines a robust **LightGBM** classification model with a **Flask API** and a user-friendly **Chrome Extension** to provide instant feedback on viewer sentiment directly on the YouTube video page.

---

## 🚀 Features

*   **Real-time Sentiment Analysis**: Classifies comments as **Positive**, **Neutral**, or **Negative**.
*   **Interactive Visualizations**:
    *   📊 **Sentiment Distribution**: Pie charts showing the overall mood of the comment section.
    *   ☁️ **Word Clouds**: Visual representation of the most frequent words used in comments.
    *   📈 **Trend Analysis**: Line graphs tracking sentiment changes over time.
*   **Chrome Extension**: Seamlessly integrates with YouTube to analyze comments without leaving the page.
*   **Robust ML Pipeline**: Built with **DVC (Data Version Control)** for reproducible data processing and model training.
*   **Advanced NLP**: Utilizes **TF-IDF** vectorization and **Lemmatization** for accurate text processing.

---

## 🛠️ Tech Stack

*   **Language:** Python 3.x
*   **Machine Learning:** LightGBM, Scikit-learn, Pandas, NumPy, NLTK
*   **Backend API:** Flask, Matplotlib, WordCloud
*   **Data Version Control:** DVC
*   **Frontend:** HTML, CSS, JavaScript (Chrome Extension)
*   **Experiment Tracking:** MLflow (Integrated)

---

## 📂 Project Structure

```bash
YouTube-Sentiment-Insights/
├── .dvc/                   # DVC configuration files
├── data/                   # Data directory (raw, interim, processed)
├── flask_api/              # Backend API
│   └── main.py             # Flask application entry point
├── notebooks/              # Jupyter notebooks for EDA and experiments
├── src/                    # Source code for ML pipeline
│   ├── data/               # Data ingestion and preprocessing scripts
│   ├── model/              # Model building and evaluation scripts
│   └── ...
├── yt-chrome-plugin-frontend/ # Chrome Extension source code
│   ├── manifest.json
│   ├── popup.html
│   └── popup.js
├── dvc.yaml                # DVC pipeline definition
├── params.yaml             # Hyperparameters for the model
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## ⚡ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/bhawsarathrva/yt_comment_sentiment_analyasis.git
cd YouTube-Sentiment-Insights
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the DVC Pipeline
To reproduce the entire machine learning pipeline (ingestion, preprocessing, training):
```bash
dvc repro
```
This will generate the `lgbm_model.pkl` and `tfidf_vectorizer.pkl` files in the root directory.

### 4. Start the Flask API
The backend server handles predictions and image generation.
```bash
python flask_api/main.py
```
The API will start running at `http://localhost:5000`.

### 5. Load the Chrome Extension
1.  Open Chrome and navigate to `chrome://extensions/`.
2.  Enable **Developer mode** (top right corner).
3.  Click **Load unpacked**.
4.  Select the `yt-chrome-plugin-frontend` directory from this project.
5.  Go to any YouTube video and click the extension icon to analyze comments!

---

## 🧠 Model Pipeline Details

The project uses **DVC** to manage the ML lifecycle:

1.  **Data Ingestion**: Splits raw data into training and testing sets.
2.  **Data Preprocessing**: Cleans text (lowercase, removing stopwords/special characters) and applies lemmatization.
3.  **Model Building**:
    *   **Vectorization**: TF-IDF (Term Frequency-Inverse Document Frequency).
    *   **Algorithm**: LightGBM Classifier (Gradient Boosting).
4.  **Model Evaluation**: Calculates metrics like Accuracy, Precision, Recall, and F1-Score.

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:
1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/YourFeature`).
3.  Commit your changes (`git commit -m 'Add some feature'`).
4.  Push to the branch (`git push origin feature/YourFeature`).
5.  Open a Pull Request.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/bhawsarathrva">Athrva Bhawsar</a>
</p>