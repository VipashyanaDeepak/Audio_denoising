# Audio_denoising

# 🎧 Audio Denoising using Python

This repository demonstrates a basic approach to audio denoising using signal processing techniques. It focuses on reducing unwanted background noise from `.wav` audio files using spectral gating, a widely-used technique in noise suppression.

---

## 📌 Overview

Audio recordings often contain ambient noise that reduces clarity, especially in voice-based applications. This project provides a step-by-step implementation to remove such noise using Short-Time Fourier Transform (STFT) and spectral gating in Python.

---

## 🛠️ Technologies and Libraries Used

The project uses the following Python libraries:

### ✅ **Librosa**
- For loading and manipulating audio signals.
- Converts audio into frequency domain using STFT.
- `librosa.load()` helps load `.wav` files into numpy arrays.

### ✅ **NumPy**
- Core numerical library used for array operations, manipulating spectrograms, and performing masking operations.

### ✅ **Matplotlib**
- Used to visualize audio waveforms and spectrograms before and after denoising.
- Helps in understanding the impact of the denoising algorithm.

### ✅ **IPython.display.Audio**
- To play audio directly inside the notebook for before/after comparisons.

---

## 🚀 How it Works

### 1. **Loading Audio**
- The noisy audio file is loaded using `librosa`.
- Sampling rate is standardized for consistency.

### 2. **Spectrogram Transformation**
- Convert the audio signal to the frequency domain using STFT.
- Calculate magnitude and phase from the complex STFT result.

### 3. **Noise Profiling**
- Assumes the beginning of the audio has only noise.
- Calculates a mean noise profile over this segment.

### 4. **Spectral Gating**
- Subtracts the estimated noise profile from the rest of the spectrogram.
- Uses a thresholding technique to zero out low-power frequencies.

### 5. **Reconstruction**
- The denoised magnitude is combined with the original phase.
- Inverse STFT is applied to get back the time-domain waveform.
- Resulting waveform is written to a `.wav` file.

---

## 📁 Folder Structure

```bash
audio-denoising/
├── denosing.ipynb       # Jupyter notebook with the full implementation
├── input.wav            # Original noisy audio input (example)
├── denoised_output.wav  # Output after denoising
├── README.md            # Project documentation
