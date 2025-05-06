# Audio Denoising Using Deep Learning (U-Net)

## Overview
This project aims to remove background noise from audio recordings using a deep learning model based on the U-Net architecture. It involves converting audio signals into spectrograms, training the model on noisy and clean pairs, and reconstructing denoised audio signals.

## Features
- Converts noisy audio to spectrogram using STFT (Short-Time Fourier Transform)
- Trains a U-Net model to learn noise-free representations
- Denoises unseen noisy audio files using the trained model
- Visualizes noisy, clean, and denoised spectrograms
- Audio playback for qualitative evaluation using IPython widgets

## Technologies Used
- Python
- PyTorch
- Torchaudio
- IPython & ipywidgets
- Matplotlib

## Dataset
- Clean and noisy audio samples (WAV format, 16kHz mono)
- Custom dataset or publicly available datasets like UrbanSound8K

## Model
- U-Net architecture with downsampling and upsampling paths
- Trained for 50 epochs with Mean Squared Error loss
- Optimized using Adam optimizer

## Steps to Run
1. Clone this repository
2. Place your audio files inside a `data/` folder
3. Run the training notebook to train the U-Net model
4. Evaluate the model using the test audio files
5. Use interactive buttons to listen to and compare noisy vs denoised outputs

## Results
- Model achieved around 80% accuracy in denoising performance
- Clear improvement in signal quality, verified through spectrograms and audio playback

## Future Scope
- Integration of advanced architectures like Transformers
- Real-time denoising on mobile and embedded devices
- Explainable AI for transparent model decisions
- Use of multimodal data fusion for robust denoising

## License
This project is intended for educational and research purposes.
