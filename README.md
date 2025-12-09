# 🎬 AI Chapter Generator Pipeline & Streamlit App  
*A complete workflow for video processing, transcription, and chapter generation.*

<p align="center">
  <img src="https://img.shields.io/badge/Framework-Streamlit-FF4B4B?logo=streamlit&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Whisper-OpenAI-412991?logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/Video Processing-MoviePy%20%7C%20OpenCV-blue" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
</p>

## 📌 Overview
This repository contains a **fully automated video/audio chapter-generation pipeline** powered by:

- **OpenAI Whisper** for transcription  
- **MoviePy + OpenCV** for media processing  
- **YT-DLP** for video downloads  
- **Streamlit** for an interactive UI  
- **Cloudflared** for secure tunneling & public sharing  

All components are auto-generated from the notebook, making it easy to run locally or deploy anywhere.

## 📂 Project Structure
```
.
├── title (1).ipynb          # Notebook that generates pipeline + app files
├── chapter_pipeline.py      # Core logic for downloading, transcribing, chaptering
├── streamlit_app.py         # Streamlit frontend
└── outputs/                 # Generated transcripts, chapter JSON, etc.
```

## ✨ Features
### 🔥 Core Functionalities
✔ Download YouTube videos using YT-DLP  
✔ Extract audio/video frames  
✔ Run Whisper transcription (CPU/GPU)  
✔ Auto-generate timestamps & chapter summaries  
✔ Export results as `.json` or `.txt`  
✔ UI to upload videos or paste URLs  
✔ Cloudflared tunnel for one-click public access  

## 🛠 Installation
```bash
pip install streamlit cloudflared plotly scikit-learn librosa accelerate
pip install opencv-python-headless moviepy yt-dlp openai-whisper
```

## ▶️ Running the Application
### Local Run
```bash
streamlit run streamlit_app.py
```

### 🌐 Public URL via Cloudflared
```bash
cloudflared tunnel --url http://localhost:8501
```

## 🧠 How It Works
1. User uploads a video or pastes URL  
2. Pipeline downloads → extracts → transcribes → chapters  
3. Streamlit displays results and download links  

## 📦 Outputs
| File Type | Description |
|----------|-------------|
| `transcript.json` | Raw Whisper transcription |
| `chapters.json` | Auto-generated chapters |
| `.txt` | Human-readable chapter summaries |

## 🧪 Use Cases
- Lecture chaptering  
- Podcast indexing  
- Long YouTube video summarization  
- Meeting archives  


