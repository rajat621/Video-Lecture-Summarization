🎥 Video & Lecture Summarization

An AI-powered video and lecture summarization pipeline built in a Google Colab environment.
This project automatically converts long lecture or informational videos into concise, structured summaries using speech recognition and transformer-based NLP models.

✨ Features

Automatic Audio Extraction – Extracts audio track from input video files using MoviePy/FFmpeg.

Speech-to-Text Conversion – Transcribes spoken content into text using Whisper (ASR model).

Abstractive Text Summarization – Generates coherent summaries using transformer models like BART/T5.

Long Video Handling – Processes lengthy lectures by chunking transcripts before summarization.

Cloud Execution (Colab) – GPU-enabled processing without requiring high-end local hardware.

Exportable Summaries – Saves generated summaries as text files for later use.

📦 Installation (Google Colab)

Run the following in a Colab cell:

pip install -q torch transformers sentencepiece
pip install -q moviepy openai-whisper ffmpeg-python
pip install -q numpy pandas matplotlib


If using GPU in Colab:

Runtime → Change runtime type → GPU

🚀 Usage

1️⃣ Upload your lecture/video file in Colab

2️⃣ Run the pipeline cells sequentially

3️⃣ The system will:

Extract audio

Convert speech to text

Generate summary

4️⃣ The final summary will be displayed and saved

🛠 How It Works

Video Input – User provides a lecture or educational video.

Audio Extraction – Audio is separated from video using MoviePy/FFmpeg.

Speech Recognition – Whisper model converts audio into transcript text.

Text Processing – Transcript is cleaned and formatted.

Summarization – BART/T5 model generates an abstractive summary.

Output – Final summarized text is displayed and stored.

⚙ Configuration

You can modify parameters inside the configuration cell:

MAX_INPUT_LENGTH = 1024      # Token length per chunk
MAX_SUMMARY_LENGTH = 150     # Summary size
MIN_SUMMARY_LENGTH = 50
MODEL_NAME = "facebook/bart-large-cnn"


For Whisper:

WHISPER_MODEL = "base"   # tiny / base / small / medium / large

🧠 Technologies Used

Python

PyTorch

Hugging Face Transformers

OpenAI Whisper

MoviePy / FFmpeg

NumPy / Pandas

Google Colab (GPU runtime)

🎯 Capabilities

Summarizes long lecture videos

Reduces 1-hour lecture into short readable summary

Produces natural language (abstractive) summaries

Works entirely in cloud-based environment

Easily extendable to multilingual support

📜 License

This project is intended for educational and research purposes.
Please follow the respective licenses of:

Whisper

Hugging Face Transformers

BART / T5 models
