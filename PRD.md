## 🧱 Product: “Speech Upgrade AI”

### 🎯 Core Value

> Upload messy spoken English → get clean, natural, same-timing audio.

---

## 🔄 Pipeline

### 1. Input

* Video or audio file

---

### 2. Speech-to-Text

* Model: Whisper / Deepgram
* Output:

  * transcript
  * timestamps per sentence/phrase

---

### 3. Language Refinement

LLM prompt:

```
Rewrite the following spoken English:
- Fix grammar and fluency
- Keep meaning identical
- Keep sentence length similar
- Preserve speaking style (casual, not formal)
- Do NOT shorten too much
```

👉 Also enforce:

* ±10% length constraint (important for timing)

---

### 4. Timing Alignment Layer

Options:

* naive: keep sentence durations
* advanced:

  * stretch/compress TTS speed slightly
  * or split long sentences

---

### 5. Voice Generation

* ElevenLabs API or similar
* Inputs:

  * refined script
  * target voice
  * speed parameter

---

### 6. Output

* New audio file
* Optional:

  * auto-overlay on original video

---

## 🧠 Differentiation (important)

Most tools:

* translate OR dub

this product:

* **improves thinking clarity + language quality**

👉 That’s a different category:
**“AI speech polishing”**

---

## ⚡ MVP stack (fast build)

* Node / Electron Desktop App
* AI SDK: Use Vercel's AI SDK.
* STT: Whisper API
* LLM Options: Google Gen AI, OpenAI, and OpenRouter
* TTS: ElevenLabs API, 
* Optional UI: simple upload + preview

---

## 💡 Customization features (if you go further)

* “Make me sound more confident”
* “Make it sound native American”
* “Keep my personality but clearer”
* slider:

  * raw → polished → professional
