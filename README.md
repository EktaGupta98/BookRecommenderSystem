📚 Book Recommendation System

A Flask-based web application that recommends books using a collaborative filtering approach. The system suggests similar books based on user input by leveraging precomputed similarity scores and trained recommendation models.

🚀 Features
📖 Top Popular Books Display on homepage
🔍 Search-based Book Recommendation System
🤝 Similarity-based Suggestions using ML model
🧠 Precomputed similarity matrix for fast results
🖼️ Displays book cover, author, and ratings
⚡ Lightweight and fast Flask backend
🧩 Tech Stack
Python
Flask
NumPy
Pandas
Pickle
HTML / CSS (Jinja Templates)
📁 Project Structure
├── app.py                     # Main Flask application :contentReference[oaicite:0]{index=0}
├── requirements.txt           # Project dependencies :contentReference[oaicite:1]{index=1}
├── Procfile                   # Deployment configuration (e.g., Heroku)
├── templates/                 # HTML templates
│   ├── index.html
│   └── recommend.html
├── model/ (or root files)     # Serialized ML data
│   ├── books.pkl              # Books dataset
│   ├── popular.pkl            # Popular books dataframe
│   ├── pt.pkl                 # Pivot table
│   └── similarity_score.pkl   # Similarity matrix
├── .venv/                     # Virtual environment (ignored)
├── .idea/                     # IDE config (ignored)
⚙️ How It Works
The system uses a pivot table (pt.pkl) representing user-book interactions.
A similarity matrix (similarity_score.pkl) is precomputed using cosine similarity.
When a user searches for a book:
The app finds its index in the pivot table.
Retrieves similar books based on similarity scores.
Displays top 5 recommended books with metadata.
▶️ How to Run the App
1️⃣ Clone the Repository
git clone <your-repo-url>
cd <your-project-folder>
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Run the Application
python app.py
4️⃣ Open in Browser
http://127.0.0.1:5000/
📈 Recommendation Logic Overview
Uses Collaborative Filtering
Based on Cosine Similarity
Steps:
Convert dataset into pivot table (users vs books)
Compute similarity between books
Recommend nearest neighbors
📌 Notes
Ensure all .pkl files are present in the root directory.
Input book name must match dataset entries.
Templates must exist inside the templates/ folder for proper rendering.
Large requirements.txt can be trimmed for deployment if needed.
🚀 Deployment

The app includes a Procfile, making it ready for deployment on platforms like:

Heroku
Render
Railway

Example command inside Procfile:

web: gunicorn app:app
🤝 Contributing

Contributions are welcome!

Fork the repo
Create a new branch
Submit a pull request
📬 Feedback

If you have suggestions or improvements, feel free to open an issue or contribute to the project.
