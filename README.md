# 🎙️ Google Summer of Code 2026 — Proposal

<p align="center">
  <img src="https://img.shields.io/badge/GSoC-2026-red?style=for-the-badge&logo=google"/>
  <img src="https://img.shields.io/badge/Organization-Sugar%20Labs-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Submitted-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Project-SpeakAI%20Multilingual%20Voice%20Engine-purple?style=for-the-badge"/>
</p>

<p align="center">
  <b>Applicant:</b> Aditya Singh Tomar &nbsp;|&nbsp;
  <b>GitHub:</b> <a href="https://github.com/Aditya15-tomar">@Aditya15-tomar</a> &nbsp;|&nbsp;
  <b>Organization:</b> <a href="https://github.com/sugarlabs">Sugar Labs</a>
</p>

---

## 📄 Proposal

The full proposal PDF is available here:
👉 **[View Proposal (PDF)](./Gsoc_proposal2026.pdf)**

---

## 🚀 Project at a Glance

| Field | Details |
|-------|---------|
| **Project Title** | SpeakAI — Multilingual Voice Engine |
| **Organization** | Sugar Labs |
| **Program** | Google Summer of Code 2026 |
| **Applicant** | Aditya Singh Tomar |
| **Tech Stack** | Python, XTTS v2, SpeechRecognition, Deep Translator, PyTorch |
| **Project Repo** | [SpeakAI-Multilingual-Voice-Engine](https://github.com/Aditya15-tomar/SpeakAI-Multilingual-Voice-Engine) |

---

## 💡 What I'm Building

A real-time **speech-to-speech translation engine** that goes beyond just converting words — it focuses on making synthesized speech sound **natural and accurate** across languages that are historically underserved by TTS technology.

Most TTS tools handle English well. The moment you step into Hindi, Arabic, or Chinese — pronunciation breaks down completely. Devanagari vowel matras get ignored, Arabic consonant clusters get mangled, Chinese tones disappear.

**SpeakAI fixes that**, using voice cloning + XTTS v2 to generate speech that actually sounds right.

---

## 🔄 How It Works

```
🎤  Speak into microphone
      ↓
🧠  Google Speech Recognition  →  Text
      ↓
🌐  Language Detection
      ↓
🔄  Deep Translator            →  Translated Text
      ↓
🗣️  XTTS v2 + Voice Cloning   →  Natural Speech
      ↓
💾  output/ folder             →  .wav files per language
```

---

## 🌍 Supported Languages

| Language | Code | Script |
|----------|------|--------|
| Hindi | `hi` | Devanagari |
| French | `fr` | Latin |
| Spanish | `es` | Latin |
| Arabic | `ar` | Arabic |
| Chinese (Simplified) | `zh` | Hanzi |
| German | `de` | Latin |
| Japanese | `ja` | Kanji / Hiragana |

---

## 🗓️ GSoC Timeline (12 Weeks)

| Phase | Weeks | Goals |
|-------|-------|-------|
| **Community Bonding** | Pre-coding | Understand Sugar Labs codebase, finalize architecture, discuss with mentors |
| **Phase 1** | Week 1–2 | Implement real language detection, modularize codebase |
| **Phase 1** | Week 3–4 | Integrate G2P (Grapheme-to-Phoneme) for Hindi & Arabic |
| **Phase 1** | Week 5–6 | Build evaluation framework, benchmark pronunciation quality |
| **Midterm Eval** | Week 6 | Working multilingual pipeline with evaluation metrics |
| **Phase 2** | Week 7–8 | ONNX runtime integration, inference optimization |
| **Phase 2** | Week 9–10 | Extend language support (Bengali, Brazilian Portuguese) |
| **Phase 2** | Week 11 | Native speaker validation, community feedback integration |
| **Phase 2** | Week 12 | Final testing, documentation, demo video |
| **Final Eval** | Week 12 | Full working system with benchmarks and docs |

---

## 🔬 Core Technical Challenges

### 1. Pronunciation Quality
Generic TTS models treat non-Latin scripts as foreign objects. My approach:
- Use **XTTS v2** with language-specific tokens
- Integrate **G2P models** (phonemizer) for phoneme-level accuracy
- Handle **schwa deletion** in Hindi — a rule almost all models ignore
- Proper **tonal handling** for Chinese

### 2. Real Language Detection
Currently using a fallback — replacing with `langdetect` + confidence scoring for accurate auto-detection.

### 3. Performance at Scale
- Hash-based caching to skip redundant generation
- Single model load across all languages in a session
- ONNX export planned for low-resource device support

---

## 🤝 My Contributions to Sugar Labs

| Contribution | Type | Link |
|-------------|------|------|
| SpeakAI Multilingual Engine | Project | [Repo](https://github.com/Aditya15-tomar/SpeakAI-Multilingual-Voice-Engine) |
| PR Reviews | Community | MusicBlocks open PRs |
| Community Engagement | Discussion | Sugar Labs mailing list & chat |

---

## 👤 About Me

I'm **Aditya Singh Tomar**, a developer passionate about making technology accessible to people across language barriers. I believe that speech tools should work just as well for a Hindi speaker in Rajasthan as they do for an English speaker in San Francisco.

This project isn't just a GSoC proposal to me — it's a problem I genuinely care about solving.

**Skills relevant to this project:**
- Python (primary language)
- Machine Learning / Deep Learning (PyTorch)
- Audio processing (Torchaudio, librosa)
- Open source contribution workflow (Git, GitHub, PR reviews)
- Multilingual awareness (Hindi native speaker)

---

## 🔮 Beyond GSoC

This project is designed as a **long-term contribution** to Sugar Labs, not just a summer project. Planned post-GSoC work includes:

- REST API / WebSocket interface for real-time streaming
- Web UI for browser-based interaction
- Support for low-resource languages (Swahili, Quechua, Kinyarwanda)
- Community-driven pronunciation validation framework

---

## 📬 Contact

- **GitHub:** [@Aditya15-tomar](https://github.com/Aditya15-tomar)
- **Project Repo:** [SpeakAI-Multilingual-Voice-Engine](https://github.com/Aditya15-tomar/SpeakAI-Multilingual-Voice-Engine)

---

<p align="center">
  <i>"This project is not just about converting text to speech —<br>
  it's about making speech sound natural, accurate, and accessible across every language."</i>
</p># Gsoc_proposal_2026
🎙️ GSoC 2025 Proposal | Sugar Labs — SpeakAI Multilingual Voice Engine | Real-time speech-to-speech translation using XTTS v2
