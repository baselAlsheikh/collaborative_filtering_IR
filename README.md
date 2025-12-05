# Collaborative Filtering Recommendation System  
### **README**

## 📌 Overview
This project implements a **user–user collaborative filtering** recommendation system using Python.  
It follows the structure required in the assignment, including generating synthetic movie ratings,  
normalizing the data, computing user similarities, and producing movie recommendations for new users.

The notebook contains 3 main stages:
1. **Data Generation** – Creating a movie list and randomized user–movie rating matrix  
2. **Normalization + Similarity Calculation** – Mean-centering and cosine similarity  
3. **Recommendations** – Predicting ratings and recommending top movies to new users  

---

## 📂 Project Structure
The notebook is divided into clear, easy-to-run cells:

### **Cell 1 – Dataset Creation**
- Defines 20 movies from different genres  
- Creates 15 users  
- Randomly assigns ratings:
  - 5 users rate 8–10 movies  
  - 5 users rate 4–6 movies  
  - 5 new users rate only 2–3 movies  
- Stores data in a Pandas DataFrame

### **Cell 2 – Data Normalization & User Similarity**
- Computes each user’s average rating  
- Applies **mean-centering**  
- Replaces missing values with 0  
- Calculates **cosine similarity** between the first 10 users  
- Extracts the **top 3 most similar user pairs**

### **Cell 3 – Recommendations for New Users**
- For each new user (U11–U15):
  - Computes similarity to the first 10 users  
  - Selects the **3 most similar neighbors**  
  - Predicts ratings for unrated movies  
  - Recommends the **top 2–3 movies** based on predicted score  

---

## 🧠 How It Works
The core idea behind collaborative filtering is that **users with similar preferences can help recommend movies to each other**.

Key concepts used:
- **Mean-centering:** adjusts for different user rating scales  
- **Cosine similarity:** measures similarity between user rating vectors  
- **Weighted prediction:** uses neighbor similarity to estimate missing ratings  


## 📝 Requirements
Make sure the following libraries are installed:

```bash
pip install numpy pandas
