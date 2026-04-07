# 📝 Hindi Text Suggestion System

The **Hindi Text Suggestion System** is a high-performance hybrid application that provides real-time Hindi word and phrase suggestions based on user input.

It combines:
- ⚡ C backend (Trie + N-gram engine)
- 🌐 Flask middleware (API layer)
- 🎨 HTML/CSS/JS frontend
- 🚀 Apache + WSGI deployment

This system is optimized for **speed, accuracy, and scalability**, making it ideal for intelligent editors, search boxes, and language learning tools.

---

## 🌟 Features

✅ **Trie-Based Dictionary & N-gram Search**  
Uses compact trie structures for fast dictionary and n-gram lookup. Supports unigram, bigram, trigram, fourgram, and fivegram models. Words are prioritized based on frequency and grammatical context.  

✅ **Fuzzy Matching**  
Implements edit-distance-based search to correct spelling mistakes. Used when exact dictionary match fails.  

✅ **Contextual Suggestions**  
N-gram tries provide context-aware suggestions based on up to the last 4 Hindi words typed. Prioritizes more probable next words based on real Hindi language usage.  

✅ **Real-Time Frontend**  
Interactive Hindi typing interface using a `<textarea>`. The suggestion box appears directly below the last typed word, even across lines, without shifting layout. Suggestions update dynamically via backend API.  

✅ **Flask + Apache + WSGI Integration**  
Lightweight Flask server receives frontend input and communicates with C backend via FIFO. Deployed using Apache2 + mod_wsgi, ensuring production-readiness and stability.  


---

## 🔧 Technologies Used

| Layer        | Technology                     |
|-------------|------------------------------|
| Frontend     | HTML, CSS, JavaScript        |
| Backend      | C (Trie & N-gram logic)      |
| Middleware   | Python Flask                 |
| Server       | Apache2 + mod_wsgi           |
| Communication| FIFO (Python ↔ C)            |
| OS           | Linux (Ubuntu/Debian)        |

---

## 🚀 How It Works

1. User types Hindi text in the frontend.
2. Input is sent to `/suggest` API (Flask).
3. Flask backend:
   - Sends request to C server via FIFO
4. C server:
   - Performs dictionary + N-gram lookup
   - Finds best matches
5. Suggestions returned to frontend
6. Displayed in real-time near cursor

---

## 📦 Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/hindi-text-suggestion-system.git
cd hindi-text-suggestion-system
