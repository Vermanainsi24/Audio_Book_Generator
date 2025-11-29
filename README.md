# 🎧 AudioBook Generator

A Streamlit-based application that converts **PDF, DOCX, and TXT** files into **multilingual audiobooks** with optional AI-powered text rewriting and translation.

---

## 🚀 Features

### 📄 Fast Document Extraction
- PDF extraction using **PyMuPDF**
- DOCX extraction using **python-docx**
- TXT extraction with UTF-8 decoding
- Quick preview mode for performance

### 📝 Optional Text Rewriting
#### 🔁 Local Rewrite (Offline)
- Breaks long sentences  
- Improves narration flow  
- No API required  

#### 🤖 Gemini Rewrite (Cloud)
- Uses Google Gemini models  
- Retry + backoff for quota handling  
- Automatically falls back to local rewrite when needed  

### 🌍 Translation Before TTS
Translate English text into:
- **Hindi (`hi`)**
- **French (`fr`)**
- **Spanish (`es`)**
- **Tamil (`ta`)**
- **Telugu (`te`)**
- **English (`en`)**

Powered by **googletrans**.

### 🗣️ Multi-Language & Multi-Voice TTS
Using **Edge-TTS (Microsoft Neural Voices)**:
- 140+ voices  
- Natural speech  
- Multiple accents & genders  
- Saves output as **MP3**

### 💾 Audio History Storage
All audio files are saved inside:

History table includes:
- File name  
- Duration  
- Created date  
- Playback button  
- Download button  

### 🎨 Modern UI
- Clean Streamlit design  
- Sidebar with About section  
- Two-column layout  
- Expandable sections  
- Paginated history table  

---

## 🧩 Folder Structure
```
AudioBook-Generator/
│
├── app.py # Main Streamlit application
├── requirements.txt # Dependencies
├── README.md # Documentation
│
├── generated_audio/ # Generated MP3 files
│ └── (audio files)
│
├── modules/
│ ├── tts_engine.py # Text-to-speech engine
│ ├── translator.py # Language translation
│ └── llm_enrichment.py # Gemini + local rewriting
│
└── .env # Environment variables (ignore in Git)
```

---
## 🔑 Environment Variables

Create a .env file:
```
GEMINI_API_KEY=YOUR_API_KEY_HERE
FFMPEG_PATH=C:\ffmpeg\bin\ffmpeg.exe
```
## ▶️ Run the Application
```
streamlit run app.py
```


Open the URL displayed in the terminal (usually http://localhost:8501).

## 👩‍💻 Author

Nainsi Verma
- AI & Full-Stack Developer
- Building intelligent tools for accessibility and productivity.
