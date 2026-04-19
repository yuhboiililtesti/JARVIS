# JARVIS (v1 – Current State)

## Overview

JARVIS v1 is a **local AI assistant prototype** designed to run on Windows and Linux. It combines a web dashboard, local LLM integration (via Ollama), basic voice interaction, and system monitoring into a single project.

This version is **not a full autonomous assistant** yet. It is an early-stage foundation for a more advanced, system-controlling AI.

---

## Current Features

### Core

* FastAPI-based backend
* Web dashboard UI
* Local AI chat using Ollama
* SQLite memory and audit logging

### Voice (Prototype)

* Microphone input loop
* Speech-to-text via Google API
* Text-to-speech via pyttsx3
* Wake word detection (basic text match: “jarvis”)

### System Monitoring

* CPU, RAM, and disk usage stats
* Basic GPU detection (NVIDIA via `nvidia-smi`)
* Simple health summaries

### Automation (Limited)

* Basic command routing
* Predefined intent handling (keyword-based)
* Early sandbox execution system

---

## Limitations

* No real offline wake-word engine (not always-listening)
* Voice system is unstable across platforms (especially Linux)
* Limited system control (cannot fully operate apps or OS)
* Weak intent recognition (simple string matching)
* Minimal hardware diagnostics (no deep SMART/GPU analysis)
* Doctor script may not run without manual fixes
* Very limited testing coverage

---

## Supported Platforms

* Windows (partial support)
* Linux (partial support)

Cross-platform support is **incomplete and experimental**

---

## Setup (Basic)

```bash
# Clone repo
git clone <repo-url>
cd JARVIS

# Install dependencies
pip install -r requirements.txt

# Run backend
python main.py
```

Optional:

* Install and run Ollama locally for AI features
* Ensure microphone access is enabled for voice

---

## Project Structure

```
jarvis/
  api/          # FastAPI routes
  core/         # Config, logging
  voice/        # Voice loop + wake word (basic)
  system/       # Hardware + telemetry
  memory/       # SQLite memory + audit
  skills/       # Command handling
  sandbox/      # Restricted execution
scripts/
tests/
```

---

## Status

This is a **prototype (v1)**:

* Functional in parts
* Not production-ready
* Intended as a base for a full JARVIS system

---

## Roadmap (High-Level)

* Real wake-word engine (offline, always listening)
* Stable cross-platform voice system
* Full OS control (apps, windows, commands)
* Smarter intent + task execution
* Deep hardware diagnostics
* Improved safety and permissions

---

## License

Open-source (see LICENSE file if included)

---

## Notes

JARVIS v1 should be treated as a **development foundation**, not a finished assistant.
