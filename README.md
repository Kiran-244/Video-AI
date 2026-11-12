# 🎙️ AI Video Assistant

An AI-powered meeting and video assistant built with Python that transforms audio and video recordings into structured, searchable meeting insights.

The application uses speech-to-text models, Large Language Models (LLMs), and Retrieval-Augmented Generation (RAG) to help users understand meeting conversations, extract important information, and interact with their recordings.

## ✨ Features

- **Audio & Video Processing:** Accept YouTube URLs and locally uploaded audio/video files.
- **Multilingual Transcription:** Transcribe English using local OpenAI Whisper and Hindi/Hinglish using Sarvam AI.
- **Intelligent Summarization:** Generate concise meeting summaries in structured bullet points.
- **Action Item Extraction:** Identify tasks, assigned owners, and deadlines.
- **Decision Extraction:** Automatically identify important decisions made during meetings.
- **Open Questions:** Extract unresolved questions and required follow-ups.
- **AI-Powered Meeting Chat:** Ask questions about meeting content using RAG.
- **Semantic Search:** Retrieve relevant meeting information using ChromaDB.
- **Report Export:** Export meeting insights as PDF or TXT files.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| OpenAI Whisper | Local speech recognition |
| Sarvam AI | Hindi and Hinglish transcription |
| LangChain LCEL | LLM workflow orchestration |
| Mistral AI | AI-powered summarization and extraction |
| ChromaDB | Vector database |
| Hugging Face Embeddings | Text embeddings |
| Streamlit | Interactive web interface |

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone YOUR_REPOSITORY_URL
cd AI-Video-Assistant
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

**Windows:**

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure environment variables

Create a `.env` file in the root directory and add your API credentials:

```env
MISTRAL_API_KEY=your_mistral_api_key
SARVAM_API_KEY=your_sarvam_api_key
```

Get your API keys:

- [Mistral AI](https://console.mistral.ai/)
- [Sarvam AI](https://dashboard.sarvam.ai/)

Never upload your actual API keys to GitHub.

### 6. Run the application

```bash
streamlit run main.py
```

Check the project's entry point and configuration before running if your local folder structure differs.

## 🧠 How It Works

The application follows a multi-stage AI pipeline:

1. **Input Processing:** Accepts video URLs or uploaded media files.
2. **Audio Extraction:** Extracts and prepares audio for transcription.
3. **Speech Recognition:** Generates transcripts using Whisper or Sarvam AI.
4. **Text Processing:** Cleans and prepares transcripts for analysis.
5. **LLM Analysis:** Uses Mistral AI and LangChain to summarize conversations and extract structured information.
6. **Vector Embeddings:** Converts transcript content into embeddings and stores them in ChromaDB.
7. **RAG Pipeline:** Retrieves relevant context to answer user questions about the meeting.
8. **Report Generation:** Presents insights through Streamlit and supports report exports.

## 📂 Project Structure

```text
AI-Video-Assistant/
│
├── utils/
│   └── audio_processor.py
│
├── transcriber.py
├── translator.py
├── summarise.py
├── extractor.py
├── vector_store.py
├── rag_engine.py
├── main.py
│
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

*The structure above is illustrative; adjust it to match the actual files in your repository.*

## 🔮 Future Improvements

- Support for additional regional languages.
- Speaker identification and diarization.
- Real-time meeting transcription.
- Calendar and meeting platform integrations.
- Improved retrieval accuracy and conversational memory.
- Advanced analytics for meeting productivity.

