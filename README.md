# 🎵 Emotion-Based Music Recommendation System

An AI-powered music recommendation system that recognizes a user's facial emotion and recommends songs that match their current mood. The project combines **Computer Vision**, **Deep Learning**, and **Spotify music metadata** to deliver personalized music recommendations.

---

## 📌 Project Overview

Music has a strong influence on human emotions, and people often choose songs that reflect or change their mood. This project automates that process by detecting facial expressions and recommending songs that best suit the detected emotional state.

The system first identifies the user's emotion from an input image using deep learning models trained on the FER2013 facial expression dataset. Based on the predicted emotion, it retrieves a list of popular songs from a Spotify mood dataset.

---

## ✨ Features

- Facial emotion recognition from images
- Custom CNN model
- Transfer Learning using ResNet50V2
- Real-time face detection using OpenCV
- Emotion classification into seven categories
- Emotion-to-music mapping
- Spotify-based song recommendations
- Performance evaluation using confusion matrices and accuracy curves

---

## 😊 Supported Emotions

The system recognizes seven facial emotions:

- Angry 😠
- Disgust 🤢
- Fear 😨
- Happy 😀
- Neutral 😐
- Sad 😢
- Surprise 😲

---

## 🎵 Music Recommendation Logic

After detecting the user's emotion, the system recommends the **Top-5 most popular songs** from the Spotify mood dataset.

| Detected Emotion | Recommended Mood |
|------------------|------------------|
| Happy | Happy |
| Sad | Happy |
| Angry | Calm |
| Fear | Calm |
| Neutral | Energetic |
| Surprise | Energetic |
| Disgust | Sad |

This mapping is designed to either reinforce positive emotions or improve negative emotional states.

---

## 🧠 Deep Learning Models

### Custom CNN

A convolutional neural network was built from scratch using:

- Convolution layers
- Batch Normalization
- Max Pooling
- Dropout
- Fully Connected Layers
- Softmax Classification

**Test Accuracy:** **67.4%**

---

### ResNet50V2

A transfer learning model based on **ResNet50V2** pretrained on ImageNet.

The last layers were fine-tuned for facial emotion recognition.

**Test Accuracy:** **69.0%**

ResNet50V2 achieved better overall performance than the custom CNN.

---

## 📂 Datasets

### FER2013

Used to train and evaluate the facial emotion recognition models.

Contains facial images belonging to seven emotion classes.

---

### Spotify Mood Dataset

Contains songs labeled according to mood with information such as:

- Song Name
- Artist
- Mood
- Popularity

The recommendation engine retrieves the highest-rated songs for each mood category.

---

## ⚙️ Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## 🚀 Project Workflow

```

Input Image
│
▼
Face Detection (OpenCV)
│
▼
Image Preprocessing
│
▼
Emotion Recognition
│
├── CNN
└── ResNet50V2
│
▼
Emotion Prediction
│
▼
Mood Mapping
│
▼
Spotify Dataset
│
▼
Top-5 Song Recommendations

```

---

## 📊 Model Evaluation

The project evaluates both models using:

- Training & Validation Accuracy
- Loss Curves
- Confusion Matrix
- Random Prediction Visualization

The comparison demonstrates the effectiveness of transfer learning over the custom CNN architecture.

---

## 📁 Project Structure

```

Emotion-Based-Music-Recommender/
│
├── data/
│   ├── FER2013/
│   └── Spotify Mood Dataset/
│
├── models/
│   ├── CNN_Model.h5
│   └── ResNet50V2_Model.h5
│
├── notebooks/
│   └── Emotion\_Based\_Music\_Recommender.ipynb
│
├── images/
│
├── README.md
│
└── requirements.txt

```

---

## 🔮 Future Improvements

- Real-time webcam emotion detection
- Spotify API integration for live music streaming
- Personalized playlists
- Hybrid recommendation system
- Mobile application deployment
- Support for multiple languages and cultures

---

## 📸 Demo

*(Add screenshots or GIFs demonstrating emotion detection and music recommendations.)*

---

## 📚 References

- FER2013 Facial Expression Dataset
- Spotify Mood Dataset
- TensorFlow
- OpenCV
- ResNet50V2
