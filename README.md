# Speech Insight Demo

An early-stage scaffold for a speech-analysis pipeline aimed at noisy, real-world audio
(e.g. construction-site voice notes): transcribe → extract structured fields → optionally
generate spoken follow-up questions.

> **Status: scaffold / work in progress.** The intended structure and stack are laid out
> below, but the modules under `src/` are not implemented yet. This is a design sketch I'm
> building out, not a working demo.

## Intended pipeline

1. **Preprocess** (`src/preprocess.py`) — clean and segment noisy audio.
2. **Transcribe** (`src/transcribe.py`) — speech-to-text with Whisper.
3. **Extract** (`src/extract_info.py`) — pull key fields from the transcript with an LLM.
4. **Follow-up** (`src/generate_followup.py`) — optionally voice clarifying questions (TTS).
5. **Serve** (`src/app.py`) — expose the pipeline behind a small FastAPI app.

## Intended stack

- Whisper / faster-whisper (ASR)
- LLM-based information extraction
- FastAPI
- Optional TTS (gpt-4o-mini-tts / Bark)

## Progress

- [x] Project scaffold + dependency setup
- [ ] Audio preprocessing
- [ ] Transcription
- [ ] Information extraction
- [ ] Follow-up generation (TTS)
- [ ] FastAPI app

## Note

No proprietary or client data is included.
