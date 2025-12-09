🎬 AI Chapter Generator Pipeline & Streamlit App

A complete workflow for video processing, transcription, and chapter generation.

<p align="center"> <img src="https://img.shields.io/badge/Framework-Streamlit-FF4B4B?logo=streamlit&logoColor=white" /> <img src="https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/Whisper-OpenAI-412991?logo=openai&logoColor=white" /> <img src="https://img.shields.io/badge/Video Processing-MoviePy%20%7C%20OpenCV-blue" /> <img src="https://img.shields.io/badge/License-MIT-green" /> </p>
📌 Overview

This repository contains a fully automated video/audio chapter-generation pipeline powered by:

OpenAI Whisper for transcription

MoviePy + OpenCV for media processing

YT-DLP for video downloads

Streamlit for an interactive UI

Cloudflared for secure tunneling & public sharing

All components are auto-generated from the notebook, making it easy to run locally or deploy anywhere.

📂 Project Structure

├── title (1).ipynb          # Notebook that generates pipeline + app files
├── chapter_pipeline.py      # Core logic for downloading, transcribing, chaptering
├── streamlit_app.py         # Streamlit frontend
└── outputs/                 # Generated transcripts, chapter JSON, etc.

✨ Features
🔥 Core Functionalities

✔ Download YouTube videos using YT-DLP
✔ Extract audio/video frames
✔ Run Whisper transcription (CPU/GPU)
✔ Auto-generate timestamps & chapter summaries
✔ Export results as .json or .txt
✔ UI to upload videos or paste URLs
✔ Cloudflared tunnel for one-click public access

🛠 Installation
1️⃣ Install Dependencies
pip install streamlit cloudflared plotly scikit-learn librosa accelerate
pip install opencv-python-headless moviepy yt-dlp openai-whisper

▶️ Running the Application
Local Run
streamlit run streamlit_app.py

🌐 Public URL via Cloudflared
cloudflared tunnel --url http://localhost:8501


This provides a secure public link you can share.

🧠 How It Works

Input: User uploads a video or pastes a YouTube URL

Pipeline:

Downloads video

Extracts audio

Runs Whisper transcription

Identifies chapter boundaries

Summaries timestamps + topics

Output:

Readable chapter summary

JSON metadata

Downloadable files

UI:

Results displayed on Streamlit with expanders, plots, and downloads

📦 Outputs
File Type	Description
transcript.json	Raw Whisper transcription with timestamps
chapters.json	Auto-generated chapters
.txt summary	Readable chapter summaries
Audio/video snippets	Optional generated segments
🧪 Example Use Cases

Auto-chapter long video lectures

Podcast → structured content

YouTube long-form summarization

Educational content indexing

Multi-speaker meeting archives

🚀 Deployment Options

You can deploy using:

Streamlit Cloud

HuggingFace Spaces

AWS EC2 / Lambda

GCP Cloud Run

Azure Container Apps

Ask me if you want the deployment guide!

🏗 Tech Stack
Component	Tools
Transcription	OpenAI Whisper
Video/Audio	MoviePy, OpenCV
Downloads	yt-dlp
Web UI	Streamlit
Tunneling	Cloudflared
🤝 Contributing

Pull requests are welcome!
Please open an issue if you’d like to request a new feature.

📜 License

This project is released under the MIT License.

⭐ Support

If you like this project, please give it a star ⭐ on GitHub!
