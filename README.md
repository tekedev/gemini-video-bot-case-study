# Gemini Video Bot — Automated AI Video Script & Synthesis Case Study

> **Notice:** This repository is an **Architectural Case Study & Engineering Showcase**. Production bot scripts and raw video output pipelines remain air-gapped on local infrastructure.

---

## 🏛️ Executive Summary

**Gemini Video Bot** is an autonomous video production pipeline that leverages Google Gemini AI to research trending topics, generate structured multi-scene scripts, synthesize natural voiceover audio (TTS), and composite dynamic short-form videos automatically.

---

## ⚡ Key Engineering & Algorithmic Achievements

- **Structured Prompting Pipeline:** Enforces JSON schema outputs from Gemini API for automated video timeline segmentation (scene text, duration, visual style, caption markers).
- **Automated Video Compositing:** Integrates MoviePy and FFmpeg to composite audio tracks, background video loops, and animated subtitle captions automatically.
- **Voiceover TTS Synchronization:** Synchronizes generated text-to-speech audio durations with video scene transitions to eliminate audio-visual drift.

---

## 📐 System Architecture

```
   ┌────────────────────────────────────────────────────────┐
   │                 Topic Research Trigger                 │
   └───────────────────────────┬────────────────────────────┘
                               │
                               ▼
   ┌────────────────────────────────────────────────────────┐
   │          Gemini AI Script & Timeline Generator         │
   └───────┬───────────────────┬────────────────────┬───────┘
           │                   │                    │
           ▼                   ▼                    ▼
  ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
  │ TTS Voice Engine│ │ Asset Fetcher   │ │ Subtitle Sync   │
  │ (Audio Track)   │ │ (Video Clips)   │ │ (SRT Generator) │
  └────────┬────────┘ └────────┬────────┘ └────────┬────────┘
           │                   │                    │
           └───────────────────┼────────────────────┘
                               ▼
   ┌────────────────────────────────────────────────────────┐
   │         FFmpeg / MoviePy Video Compositing Core        │
   └────────────────────────────────────────────────────────┘
```

---

## 📊 Technical Performance Benchmarks

| Metric | Benchmark Value |
|--------|-----------------|
| **Script Generation Time** | ~2.1 seconds |
| **Video Compositing Speed** | 1080p Short in < 35 seconds |
| **Subtitle Sync Accuracy** | ± 50 ms per word |

---

## 🛠️ Tech Stack & Tooling

- **AI Model:** Google Gemini API (Structured JSON Schema)
- **Media Engine:** Python 3.12, MoviePy, FFmpeg, Pillow
- **Voice Synthesis:** Edge-TTS / gTTS Async Integrations

---
*Architected and engineered by **Enes Teke (tekedev)**.*
