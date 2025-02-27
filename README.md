# 🎬 Movie Recommender System Using Machine Learning

## 📝 Overview

Recommendation systems play a crucial role in today's digital world, helping users make informed choices efficiently. These systems analyze user behavior and preferences to provide personalized suggestions. Our Movie Recommender System is built using machine learning techniques to suggest movies based on user interests.

## 📌 Types of Recommendation Systems

### 🔹 1. Content-Based Filtering

📌 Content-based recommendation systems analyze item attributes and user preferences to suggest similar content. These systems generate a feature vector for items and compare them to the user’s past preferences.

- 🎥 Used in platforms like YouTube and Twitter.
- 🏷 Works based on embeddings of features such as genre, actors, and director.
- ⚠️ The primary limitation is the risk of excessive specialization, where the system fails to suggest content outside known preferences.

### 🔹 2. Collaborative Filtering

📌 Collaborative filtering relies on user-item interactions by identifying patterns among users with similar tastes.

- 👥 Forms clusters of users with similar ratings or preferences.
- 📚 Used in applications like book recommendation systems.
- 🧩 Works on the principle that users with similar preferences in the past may like similar items in the future.
- ⚠️ Challenges include:
  - 🚀 Computational expense due to large user-item matrices.
  - 🎭 Popular items dominate recommendations, while newer or niche items might be overlooked.

### 🔹 3. Hybrid Filtering

📌 Hybrid recommendation systems combine content-based and collaborative filtering techniques to mitigate the limitations of each approach.

- 💡 Utilizes advanced techniques such as word2vec and embeddings.
- ✅ Commonly used in modern recommendation engines to enhance accuracy and diversity.

## 🎯 About This Project

This project is a **Streamlit web application** that recommends similar movies based on user interests. The system utilizes **cosine similarity** to measure the closeness between movie feature vectors, providing personalized suggestions.

## 📂 Dataset

- 🗂 The dataset contains information about movies, including genres, descriptions, and ratings.
- 🔍 Movie similarity is determined using cosine similarity.

### 📊 Cosine Similarity Concept

1. 🧮 Cosine similarity measures the similarity between two vectors in a multi-dimensional space.
2. 📈 The vectors used here are NumPy arrays representing movie features.
3. 🏆 The similarity score ranges from 0 to 1:
   - ❌ **0**: Completely dissimilar.
   - ✅ **1**: Identical.
4. 🔗 For more details , check URL : https://www.learndatasci.com/glossary/cosine-similarity/

## 🚀 How to Run the Project

### 📌 Steps to Set Up and Run the Application

#### 🔹 1. Clone the Repository

```sh
https://github.com/entbappy/Movie-Recommender-System-Using-Machine-Learning.git
```

#### 🔹 2. Install Dependencies

```sh
pip install -r requirements.txt
```

#### 🔹 3. Run the Web Application

```sh
streamlit run app.py
```

### 🔹 4. Deployment Setup (Procfile & setup.sh)

For deployment, you can use **Procfile** and **setup.sh** instead of a Conda environment.

#### 📌 Create a `Procfile`

```sh
echo "web: streamlit run app.py" > Procfile
```

#### 📌 Create a `setup.sh`

```sh
echo "mkdir -p ~/.streamlit/" > setup.sh
echo "echo \"[server]\nheadless = true\nenableCORS=false\nport = \$PORT\n\" > ~/.streamlit/config.toml" >> setup.sh
```

#### 📌 Make `setup.sh` Executable

```sh
chmod +x setup.sh
```

#### 📌 Run the Setup Script

```sh
./setup.sh
```

## 🎨 Features

- 🎬 Movie recommendations based on user input.
- 🖥 Interactive Streamlit UI for easy usability.
- 🧠 Uses **cosine similarity** for movie comparison.
- 📈 Scalable approach for adding more features in the future.

## 🔮 Future Enhancements

- 🔄 Implementing hybrid filtering to improve recommendation diversity.
- 👥 Adding user-based collaborative filtering.
- 🌍 Enhancing the dataset with real-time movie ratings and reviews.
- ☁️ Deploying the model on cloud platforms for wider accessibility.

---

