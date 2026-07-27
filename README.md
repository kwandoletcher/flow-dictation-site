# Flow Dictation

**Local, privacy-first voice-to-text for Windows.** Press a hotkey, speak, and your words are transcribed, cleaned up, and pasted into whatever app you're using — email, Slack, your editor, anywhere.

Everything runs on your own machine. No cloud, no account, no audio ever leaving your computer.

> **Status: Open beta.** This repository hosts the product site and overview materials.

## How it works

```
Hold hotkey → speak → release
     └─ Whisper transcription (GPU-accelerated, local)
          └─ Local LLM cleanup — grammar, punctuation, formatting
               └─ Clean text pasted into your active app
```

Two local models working in sequence: [faster-whisper](https://github.com/SYSTRAN/faster-whisper) (`large-v3-turbo`) handles transcription, and a quantized Qwen2.5-7B pass fixes grammar, punctuation, and formatting — so what lands in your document reads like you wrote it, not like a transcript.

## Features

- **Push-to-talk** — hold Right Ctrl to record, release to transcribe and paste
- **App awareness** — detects the app you're in (Slack, Gmail, VS Code…) and switches writing style automatically
- **Dictation profiles** — General, Email/Formal, Chat/Casual, Code, Technical — plus your own
- **Rewrite mode** — select text, speak an instruction, get it rewritten in place
- **Custom dictionary** — teach it your names, jargon, and shortcuts
- **Searchable history** — every dictation logged locally, raw vs. cleaned side by side
- **System tray** — color-coded status (idle / recording / processing) with quick actions

## Privacy

- All transcription and cleanup runs **on-device**
- **Zero network calls** in the dictation path
- Your audio and history never leave your machine

This is the point of the product. If you handle confidential material — legal, medical, finance, client work — cloud dictation tools are a non-starter. Flow Dictation isn't cloud-optional; it's cloud-incapable by design.

## Hardware

Scales to what you have. GPU recommended, not required.

| Tier | GPU | Latency |
|------|-----|---------|
| CPU-only | none | ~5–10s |
| Budget | GTX 1060 6GB | ~3–5s |
| Mid | RTX 3060 8GB+ | ~1–2s |
| Comfortable | 12GB+ VRAM | ~1s |

**OS:** Windows 10/11

## Contact

Questions or beta access: [jackson@jacksoncode.com](mailto:jackson@jacksoncode.com)
