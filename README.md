
# Vehicle Sound Classification

Hybrid Fingerprinting & Deep Learning with Streamlit Web App

(USE AUDIO FILES WITHIN GIT TO TEST THE WEBSITE, MAY NEED TO RUN WHOLE CODE AGAIN TO GET SITE)

***

## Overview

This project automatically classifies short audio clips as either **car** or **not car**. It combines two approaches:

- **Audio Fingerprinting:** Rapid, Shazam-style identification for known sounds.
- **Convolutional Neural Network (CNN):** Mel-spectrogram-based deep learning for new or noisy recordings.

A simple web app (built with Streamlit) lets users upload audio and get instant predictions.

***

## Features

- Hybrid system: automatic selection between fingerprinting and CNN
- Real-time prediction in web browser
- Support for `.wav`, `.mp3`, and most audio formats
- Modular, easy-to-extend codebase

***

## Quick Start

1. **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/vehicle-sound-classification.git
    cd vehicle-sound-classification
    ```

2. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **Prepare your dataset**
    - Place audio files in the `data/` folder.  
    - Use or adapt [Kaggle Vehicle Sounds Dataset](https://www.kaggle.com/abderrahimjanboubi/vehicle-sounds-dataset).

4. **Run the web app**
    ```bash
    streamlit run app.py
    ```

***

## How It Works

- **Fingerprinting:** Extracts spectrogram peaks and matches fingerprints in a database. If match found, returns label.
- **CNN:** If no strong match, processes the audio's mel-spectrogram through a neural network.
- **Hybrid logic:** Automatically selects the best method for each prediction.

***

## Example Results

| Model            | Accuracy         | Coverage      | Notes                        |
|------------------|:---------------:|:-------------:|:-----------------------------|
| Fingerprinting   | 76%              | ~45%          | Precise, but limited         |
| CNN              | 60–65%           | 100%          | Generalizes well             |
| Hybrid           | 67%              | 100%          | Best overall balance         |

***

## Roadmap

- Multi-class vehicle detection
- More data cleaning & augmentation
- Advanced CNN architectures
- Additional deployment options

