# 🚑 Ambulance-ER-PreArrival-Sync-Powered-by-LLM

## 🏥 Project Overview

This project enables real-time synchronization between ambulance teams and ER doctors by transcribing ambulance conversations and summarizing key medical details. It ensures that ER personnel receive critical patient information before arrival, enhancing preparedness and response time.

---

## ✨ Features

- **🎙️ Real-Time Speech-to-Text**: Converts ambulance conversations into structured text using Whisper (ASR).
- **📄 Medical Summary Generation**: Summarizes patient details and emergency levels using Llama.
- **📡 Data Transmission**: Sends transcriptions and summaries to ER staff for quick decision-making.
- **📑 Report generation** : Generates a comprehensive patient report with treatment recommendations.
- **💻 Web Dashboard**: Displays transcriptions and summaries in an intuitive, structured format.

---

## 🛠️ Technologies Used

- **Programming Language**: Python 🐍
- **Generative AI**: Whisper (ASR) for speech-to-text, Llama for summarization and report generation 🧠
- **Retrieval-Augmented Generation (RAG) Pipeline**: For enhanced data retrieval 📚
- **Audio Processing**: `pydub` 🎧
- **Frontend**: Streamlit (real-time dashboard) 🌐
- **Deployment**: Virtual environment setup using `venv` or `conda` 🚀

---

## 📁 Project Structure

```

Ambulance-ER-Near-real-time-Synchronization/
├── README.md # Documentation
├── .env # Sample environment variables
├── client/
│ ├── requirements.txt # Dependencies
│ ├── app.py # Main Streamlit application
│ └── assets/
│ └── styles.css # CSS for web interface
└── utils/
├── Generator.py # Generates global patient reports & recommendations
├── Processor.py # Processes transcribed text for analysis
├── Summarizer.py # Summarizes patient condition & emergency level
└── Transcripter.py # Converts audio to text using Whisper

```

---

## 🚀 Installation

### 🔹 1. Clone the Repository

```bash
git clone https://github.com/AnasBenAmor10/Ambulance-ER-PreArrival-Sync-Powered-by-LLM.git
cd Ambulance-ER-PreArrival-Sync-Powered-by-LLM
```

### 🔹 2. Create a Virtual Environment

```bash
python3 -m venv myenv
source myenv/bin/activate  # Windows: myenv\Scripts\activate
```

### 🔹 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 🔹 4. Set Up Environment Variables

Create a `.env` file with:

```
GROQ_API_KEY=your_groq_api_key
PINECONE_API_KEY=your_pinecone_api_key
```

---

## ⚙️ How It Works

1. **Transcripter.py** captures and converts ambulance audio to text using the Whisper model.
2. **Processor.py** cleans and structures the transcribed text for medical analysis.
3. **Summarizer.py** generates a medical summary and emergency assessment using Llama.
4. **Generator.py** produces a detailed patient report and treatment recommendations.
5. **app.py** displays results on a web interface for ER staff, utilizing Streamlit for real-time updates.

---

## 🏃 Running the Application

### ➤ Start the Web Server

```bash
streamlit run client/app.py
```

Visit `http://127.0.0.1:8501/` in your browser to see the dashboard.

### ➤ Run Individual Modules

- **Test Speech-to-Text**

```bash
python utils/Transcripter.py sample_audio.wav
```

- **Generate Summary from Text**

```bash
python utils/Summarizer.py "Patient is experiencing chest pain and difficulty breathing."
```

---

## 🤝 Contributing

We welcome contributions!

1. Fork the repository.
2. Create a new branch.
3. Submit a pull request (PR).
