# DermAI - Skin Disease Detection using Deep Learning

DermAI is a Streamlit web application that classifies skin lesions using a fine-tuned ConvNeXtV2 model trained on the HAM10000 dataset.

## Features
- Upload dermatoscopic image
- Classify into 7 skin lesion types
- View confidence and educational descriptions
- Firebase login system
- Downloadable report
- Deployed via Colab + Ngrok

## Tech Stack
- Python, Streamlit, Hugging Face Transformers, Firebase Auth
- Deployment via Google Colab + PyNgrok

## Setup
```bash
pip install -r requirements.txt
streamlit run dermAI.py

