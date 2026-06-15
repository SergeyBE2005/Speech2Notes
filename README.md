# Speech2Notes – Lecture Speech Transcriber & Summarizer

This notebook converts an audio lecture (in Russian) into a structured, concise summary using **Faster-Whisper** for transcription and **Groq (Llama 3.1)** for intelligent summarization.

## Features

- Speech recognition with `faster-whisper` (large-v3 model, CUDA-accelerated)
- AI summarization via Groq's Llama 3.1 8B model
- Outputs:
  - Full transcription (`transcription.txt`)
  - Structured lecture notes (`summary.txt`) with:
    - Thematic sections and subheadings
    - Bold key terms and definitions
    - Bulleted lists
    - Final "Main takeaways" section
- Works in **Google Colab** (GPU runtime recommended)
- Saves outputs to Google Drive & downloads them locally

## How It Works

1. Mounts Google Drive to access the audio file.
2. Installs required packages (`groq`, `faster-whisper`).
3. Transcribes the audio using Faster-Whisper (Russian language).
4. Sends the transcription to Groq's LLM with a carefully designed prompt.
5. Saves and downloads both the raw transcription and the final summary.

## Requirements

- Google Colab with **GPU accelerator** (T4 or better)
- Audio file in a supported format (`.m4a` in the example)
- Groq API key (free tier available)

## Setup

1. Upload your audio lecture to Google Drive (e.g., `Colab Notebooks/Notes-maker/Data/`).
2. Update the `AUDIO_PATH` variable in the notebook.
3. Replace the `GROQ_API_KEY` with your own key.
4. Run all cells.

## Example Output (Summary Snippet)

```markdown
**Лекция: "Пропускание мира через себя"**

**Индийские корни**
В индийской философии и буддизме существует понятие **сопереживания** (санскрит: "каруна")...

**Главные выводы**
1. Сопереживание является ключевым аспектом индийской философии.
2. Пропускание мира через себя требует открытости и нейтральности.
...
