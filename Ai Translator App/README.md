# AI Translator Chat Bot

![AI Translator Chat Bot Banner](assets/banner.png)

## 🚀 Overview

**AI Translator Chat Bot** is a full-featured, modern, WhatsApp-style web app for real-time language translation, voice synthesis, OCR-powered image translation, and phrase management. Designed for ease of use and extensibility, it leverages Python (Flask), Bootstrap, gTTS, LibreTranslate, and several powerful language and image processing libraries.

---

## ✨ Features

- **Chat-style Translation:**  
  Enjoy a WhatsApp-like chat interface for seamless multilingual conversations.

- **Auto Language Detection:**  
  Automatically detects the language of your input and updates the UI accordingly.

- **Voice Synthesis (TTS):**  
  Listen to translations with selectable male/female voice (where supported).

- **Speech-to-Text:**  
  Speak your message directly via browser speech recognition.

- **OCR Image Translation:**  
  Upload images and extract text via Tesseract OCR for instant translation.

- **Favorites & Phrasebook:**  
  Save, manage, and quickly access your favorite phrases.

- **Session-based History:**  
  Review your translation history, rate quality, and provide feedback.

- **Responsive UI:**  
  Works well on all screen sizes, including mobile.

- **Full-Screen Mode:**  
  Expand the chat and controls for immersive use.

- **Pronunciation Practice:**  
  Simple feedback on how closely you pronounce the translated text.

- **User Accounts:**  
  Register, sign in, and maintain private translation histories and favorites.

---

## 📦 Tech Stack

- **Backend:** Flask, Flask-Login, SQLAlchemy, gTTS, pytesseract
- **Frontend:** Bootstrap 5, Vanilla JS, WhatsApp-style CSS
- **Translation:** LibreTranslate (self-hosted or public API)
- **OCR:** Tesseract OCR (via Pillow & pytesseract)
- **TTS:** Google Text-to-Speech (gTTS)

---

## 🖥️ Screenshots

![Chat Demo](assets/demo-chat.png)
![OCR Demo](assets/demo-ocr.png)
![Favorites & History](assets/demo-favorites-history.png)

---

## 🛠️ Installation & Running

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/ai-translator-chatbot.git
cd ai-translator-chatbot
```

### 2. Set up Python environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Install Tesseract OCR

- **Linux (Debian/Ubuntu):**  
  `sudo apt-get install tesseract-ocr`
- **macOS (with Homebrew):**  
  `brew install tesseract`
- **Windows:**  
  Download from [UB Mannheim builds](https://github.com/tesseract-ocr/tesseract/wiki) and update the path in `app.py` if needed.

### 4. Set up LibreTranslate

- **Option 1:** Self-hosted (recommended):  
  Follow instructions at [LibreTranslate Deploy](https://github.com/LibreTranslate/LibreTranslate)
- **Option 2:** Use the public endpoint (for testing):  
  Update `LIBRETRANSLATE_URL` in `app.py` to `https://libretranslate.de/translate`  
  (Note: Rate limits and privacy apply)

### 5. Run the app

```bash
flask run
# or if running directly
python app.py
```

- Open [http://localhost:5000](http://localhost:5000) in your browser.
- Register a new user and start translating!

---

## 📄 Usage Tips

- **Auto Detect Language:**  
  Select "Auto Detect" as source; detected language updates automatically after translation.
- **Favorites:**  
  Click "Add to Favorites" in chat history to save useful translations.
- **Speech Input:**  
  Click the 🎤 icon to dictate your message.
- **Full Screen:**  
  Use the ⛶ button for distraction-free translation.
- **OCR:**  
  Upload an image (e.g., sign, page, or screenshot) to extract and translate printed text.

---

## 🔐 Security & Privacy

- User sessions and data are stored locally (SQLite by default).
- For production:  
  - Change `SECRET_KEY` and consider a more robust DB (e.g., PostgreSQL).
  - Use HTTPS and secure deployment practices.
- Uploaded images are deleted after OCR.

---

## 🤝 Contribution

Pull requests are welcome! Please fork the repository and submit your PR.  
For major changes, open an issue first to discuss what you would like to change.

### TODO / Ideas

- Advanced TTS engine support (with real male/female voice selection)
- Support for more translation providers
- Export/import favorites/history
- Group chat or shareable links
- Language proficiency analytics

---

## 🧩 Project Structure

```
ai-translator-chatbot/
│
├── app.py
├── models.py
├── requirements.txt
├── static/
│   ├── style.css
│   ├── main.js
│   ├── smart-buttons.css
│   └── whatsapp-chat.css
├── templates/
│   ├── base.html
│   └── index.html
├── assets/
│   └── (screenshots, banner)
├── uploads/
└── instance/
```

---

## 💬 License and Credits

- MIT License
- Powered by [LibreTranslate](https://libretranslate.com/), [gTTS](https://pypi.org/project/gTTS/), [pytesseract](https://pypi.org/project/pytesseract/), and [Bootstrap](https://getbootstrap.com/).

---

## 📧 Contact

For support or questions, open an issue or contact [yourusername](mailto:your@email.com).

---

**Enjoy translating like never before! 🌐🗣️📸**