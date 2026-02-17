# 🎥 Video & Lecture Summarization  

An AI-powered video and lecture summarization pipeline built in Google Colab.  
The system converts long lecture or informational videos into concise, structured summaries using speech recognition and transformer-based NLP models.

---

## ✨ Features  

- **Audio Extraction** – Extracts audio from video using MoviePy / FFmpeg  
- **Speech-to-Text** – Converts speech into text using OpenAI Whisper  
- **Abstractive Summarization** – Generates natural summaries using BART / T5  
- **Long Video Support** – Handles large transcripts using chunk processing  
- **Cloud-Based Execution** – Runs efficiently on Google Colab (GPU supported)  
- **Exportable Output** – Saves generated summaries as text files  

---

## 📦 Installation (Google Colab)

Run in a Colab cell:

```bash
pip install -q torch transformers sentencepiece
pip install -q moviepy openai-whisper ffmpeg-python
pip install -q numpy pandas matplotlib
```

Enable GPU:
```
Runtime → Change runtime type → GPU
```

---

## 🚀 Usage  

1. Upload your video file in Colab  
2. Run all cells sequentially  
3. The pipeline will:
   - Extract audio  
   - Transcribe speech  
   - Generate summary  
4. Final summary is displayed and saved  

---

## 🛠 How It Works  

1. **Video Input** – User provides lecture video  
2. **Audio Extraction** – Separate audio track  
3. **Speech Recognition** – Whisper generates transcript  
4. **Text Cleaning** – Preprocessing & formatting  
5. **Summarization** – Transformer model generates summary  
6. **Output Generation** – Summary saved & displayed  

---

## ⚙ Configuration  

Inside the configuration cell:

```python
MAX_INPUT_LENGTH = 1024
MAX_SUMMARY_LENGTH = 150
MIN_SUMMARY_LENGTH = 50
MODEL_NAME = "facebook/bart-large-cnn"

WHISPER_MODEL = "base"  # tiny / base / small / medium / large
```

---

## 🧠 Technologies Used  

- Python  
- PyTorch  
- Hugging Face Transformers  
- OpenAI Whisper  
- MoviePy / FFmpeg  
- NumPy / Pandas  
- Google Colab  

---

## 🎯 Capabilities  

- Summarizes long lecture videos  
- Produces natural language summaries  
- Reduces content review time  
- Scalable and extendable for multilingual support  

---

## 📜 License  

For educational and research purposes.  
Follow the respective licenses of Whisper and Hugging Face models.
