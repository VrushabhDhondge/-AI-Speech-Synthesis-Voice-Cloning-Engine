# 🎙️ VoxClone: AI Speech Synthesis & Voice Cloning Engine

VoxClone is a production-ready Generative AI system designed for zero-shot voice cloning and high-fidelity text-to-speech (TTS) synthesis. Powered by neural audio codecs and transformer-based autoregressive generation, the engine replicates target vocal characteristics from short (~3 to 5 second) audio samples without model fine-tuning.

---

## ⚡ Key Features

* **Zero-Shot Voice Cloning:** Clone target voices using a short reference audio clip (`.wav`/`.mp3`).
* **Neural Audio Tokenization:** Discretize audio waveforms into compact latent representations using neural audio codecs (e.g., EnCodec / VQ-VAE).
* **Controllable Prosody & Expressiveness:** Adjust speech pace, emotion, and emphasis via inline tags and conditioning vectors.
* **Low-Latency Streaming API:** Built-in FastAPI server optimized for real-time inference and low-latency audio streaming.
* **Cross-Lingual Synthesis:** Synthesize multi-language speech while retaining the speaker's original voice identity.

---

## 🏗️ System Architecture

The pipeline addresses the 6 core dimensions of Generative AI system design:

1. **Data Pipeline:** Paired audio-transcript datasets (e.g., LibriTTS) and reference voice embeddings.
2. **Tokenization:** Text grapheme-to-phoneme (G2P) conversion alongside multi-codebook neural audio tokenization.
3. **Embeddings:** Fixed-length speaker embeddings ($d$-vectors) combined with positional and phoneme embeddings.
4. **Neural Network:** Decoder-only transformer predicting frame-by-frame acoustic tokens.
5. **Conditioning:** Dynamic cross-attention using speaker voice latents, emotion tags, and timestep conditioning.
6. **Evaluation Metrics:** Evaluated using Mean Opinion Score (MOS) prediction, ASR Word Error Rate (WER), and cosine similarity of speaker embeddings.

