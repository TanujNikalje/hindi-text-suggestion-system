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

### ✅ Trie-Based Dictionary & N-gram Search
- Efficient trie data structure for fast lookup
- Supports:
  - Unigram
  - Bigram
  - Trigram
  - Fourgram
  - Fivegram
- Suggestions ranked by frequency and context

---

### ✅ Fuzzy Matching
- Uses edit-distance algorithm
- Corrects spelling mistakes
- Activates when exact match is not found

---

### ✅ Contextual Suggestions
- Uses previous **up to 4 Hindi words**
- Provides context-aware predictions
- Improves accuracy using real language patterns

---

### ✅ Real-Time Frontend
- Interactive Hindi typing interface (`<textarea>`)
- Suggestion box appears near cursor
- Works across multiple lines without layout shift
- Dynamic updates via backend API

---

### ✅ Flask + Apache + WSGI Integration
- Flask handles API communication
- Apache + mod_wsgi for deployment
- Production-ready architecture
- FIFO-based communication between Python & C

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
