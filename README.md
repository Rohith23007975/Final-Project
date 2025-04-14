# KitchenWise 🍳  

KitchenWise is a smart recipe recommendation system API that helps you cook delicious meals using the ingredients available in your fridge or kitchen. Just input what you have, and KitchenWise will suggest the most suitable recipes using NLP and similarity-based matching.

---

## ✨ Features

- **Recipe Data Scraping**  
  Automatically scrape recipes from trusted food websites and save the data in a structured CSV format.

- **Ingredient Processing (NLP)**  
  Process ingredients and recipe steps using NLP techniques to extract and lemmatize core ingredients for accurate vectorization.

- **Recipe Recommendation System**  
  Convert your available ingredients into vectors and use **cosine similarity** to find and recommend the closest matching recipes.

- **Modular Design**  
  Well-structured and modular codebase, making it easy to update datasets, algorithms, or integrate into web/mobile apps.

- **Flask API Support**  
  Easily integrate the system with external applications using a RESTful API built with Flask.

---

## 🧠 Technology Stack

- **Programming Language**: Python  
- **Web Framework**: Flask  
- **Notebook Environment**: Jupyter Notebook  
- **NLP**: Custom pre-processing, tokenization, lemmatization  
- **Similarity Algorithm**: Cosine Similarity (via `sklearn`)  
- **Data Storage**: CSV-based storage (recipes, ingredients, vectors)

---

## 🚀 How to Run the Flask API

### 1. Install Requirements
```bash
pip install flask pandas numpy scikit-learn
```

### 2. Start the API Server
Make sure `main.py`, `recommendation_engine.py`, `recipes_processed.csv`, and `recipe_recommendation_model.pkl` are in the same directory. Then run,

```bash
python main.py
```

Server will start on: `http://127.0.0.1:5000`

---

## 🛠️ Using cURL to Test the API

### 🧾 Template Command
```bash
curl -X POST "http://127.0.0.1:5000/recommend" -H "Content-Type: application/json" -d "{\"ingredients\": \"<comma-separated-ingredients>\"}"
```

### ✅ Example Command
```bash
curl -X POST "http://127.0.0.1:5000/recommend" -H "Content-Type: application/json" -d "{\"ingredients\": \"onion, garlic, tomato, ginger\"}"
```

### ✅ Example Output (JSON)
```json
{
  "recommended_recipes": [
    {
      "name": "Spicy Tomato Curry",
      "Difficulty": "Medium",
      "url": "https://somefoodsite.com/spicy-tomato-curry",
      "time": "30 mins"
    },
    {
      "name": "Garlic Tomato Pasta",
      "Difficulty": "Easy",
      "url": "https://somefoodsite.com/garlic-tomato-pasta",
      "time": "25 mins"
    }
  ]
}
```

---


## 📝 Future Enhancements

- Add user login and personalized recommendations  
- Recipe rating and feedback loop  
- Mobile app integration  
- Advanced ingredient substitutions and dietary filters  

---

Happy Cooking with **KitchenWise**! 🍲
