# 🚨 Spam Mail Detector

A lightweight Python-based spam detection system that runs entirely in one file using scikit-learn and a hardcoded dataset.

**Now with a beautiful web frontend! 🌐**

## ✨ Features

- 🧠 **Machine Learning**: Uses Multinomial Naive Bayes classifier
- 📊 **TF-IDF Vectorization**: Advanced text feature extraction
- 🧹 **Text Preprocessing**: Removes stopwords and punctuation
- 💾 **Model Persistence**: Saves trained model for faster subsequent runs
- 🎯 **Accurate**: Shows accuracy metrics after training
- 🎨 **Multiple Interfaces**: Beautiful web UI + simple CLI

## 📦 Requirements

Install the required packages:

```bash
pip install scikit-learn nltk numpy
```

Or use:

```bash
pip install -r requirements.txt
```

## 🚀 Usage

### Web Interface (Recommended)

Start the web application:

```bash
python app.py
```

Then open your browser and go to: **http://localhost:5000**

You'll see a beautiful web interface where you can:
- Type or paste messages
- Click "Detect Spam" to analyze
- Try example messages with one click
- See instant results with confidence scores

### CLI Interface

Run the command-line version:

```bash
python spam_detector.py
```

Then enter messages when prompted:

```
📧 Enter a message (or 'quit' to exit): Win a free iPhone today!
🚫 RESULT: SPAM detected!
📊 Confidence: 95.2%
```

## 📊 Dataset

The detector uses a hardcoded dataset of 15 examples:
- **8 spam messages** (prizes, free offers, urgent claims)
- **7 ham messages** (meetings, work updates, normal emails)

## 🧠 How It Works

1. **Preprocessing**: Converts text to lowercase, removes punctuation and stopwords
2. **Feature Extraction**: Uses TF-IDF to create numerical features
3. **Training**: Trains a Multinomial Naive Bayes classifier
4. **Prediction**: Predicts if a message is spam or not with confidence score

## 📈 Performance

The model achieves high accuracy on the hardcoded dataset (typically 95%+).

## 🎯 Example Output

```
🚨 SPAM MAIL DETECTOR 🚨
============================================================

✅ Loaded saved model from disk

────────────────────────────────────────────────────────────
✨ Ready to detect spam! Enter 'quit' to exit.
────────────────────────────────────────────────────────────

📧 Enter a message (or 'quit' to exit): Win free money now!
────────────────────────────────────────────────────────────
🚫 RESULT: SPAM detected!
📊 Confidence: 92.5%
────────────────────────────────────────────────────────────
```

## 📝 Files

- `app.py` - Flask web application 🆕
- `templates/index.html` - Beautiful web frontend 🆕
- `spam_detector.py` - Core ML module (can be used standalone as CLI)
- `spam_model.pkl` - Saved trained model (created after first run)
- `spam_vectorizer.pkl` - Saved vectorizer (created after first run)
- `test_detector.py` - Test script
- `requirements.txt` - Dependencies
- `README.md` - This file

## 🎓 Learning Resources

- [scikit-learn Documentation](https://scikit-learn.org/)
- [NLTK Documentation](https://www.nltk.org/)
- [Naive Bayes Classification](https://scikit-learn.org/stable/modules/naive_bayes.html)

## ⚠️ Note

This is a demonstration project with a small hardcoded dataset. For production use, consider training on larger, real-world datasets.

