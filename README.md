# 📚 Book Recommendation System

A Flask-based web application that recommends books using a collaborative filtering approach. The system suggests similar books based on user input by leveraging precomputed similarity scores and trained recommendation models.

---

## 🚀 Features

- 📖 Top Popular Books Display on homepage  
- 🔍 Search-based Book Recommendation System  
- 🤝 Similarity-based Suggestions using ML model  
- 🧠 Precomputed similarity matrix for fast results  
- 🖼️ Displays book cover, author, and ratings  
- ⚡ Lightweight and fast Flask backend  

---

## 🧩 Tech Stack

- Python  
- Flask  
- NumPy  
- Pandas  
- Pickle  
- HTML / CSS (Jinja Templates)  

---

## 📁 Project Structure

```
├── app.py
├── requirements.txt
├── Procfile
├── templates/
│   ├── index.html
│   └── recommend.html
├── books.pkl
├── popular.pkl
├── pt.pkl
├── similarity_score.pkl
```

---

## ⚙️ How It Works

- Uses a pivot table (`pt.pkl`) for user-book relationships  
- Uses a similarity matrix (`similarity_score.pkl`)  
- When user searches:
  - Finds the book index  
  - Computes similar books  
  - Returns top 5 recommendations  

---

## ▶️ How to Run the App

### 1. Clone Repository
```bash
git clone <your-repo-url>
cd <your-project-folder>
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run App
```bash
python app.py
```

### 4. Open Browser
```
http://127.0.0.1:5000/
```

---

## 📈 Recommendation Logic

- Collaborative Filtering  
- Cosine Similarity  
- Nearest Neighbors approach  

---

## 📌 Notes

- Ensure all `.pkl` files are present  
- Book names must match dataset  
- Templates must be inside `templates/` folder  

---

## 🚀 Deployment

Ready for deployment using:

- Heroku  
- Render  
- Railway  

Example Procfile:
```
web: gunicorn app:app
```

---

## 🤝 Contributing

Feel free to fork, improve, and submit pull requests!

---

## 📬 Feedback

Suggestions and improvements are always welcome 🚀
