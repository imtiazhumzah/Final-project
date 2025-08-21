# 🧠 DermAI – AI-Powered Skin Disease Classifier

DermAI is a **Streamlit-based AI app** that classifies skin lesions into **7 categories** using a fine-tuned [ConvNeXtV2 model](https://huggingface.co/ALM-AHME/convnextv2-large-1k-224-finetuned-Lesion-Classification-HAM10000-AH-60-20-20).  
It is trained on the **HAM10000 dataset** and provides **predictions with confidence scores**, **educational insights**, and an **exportable report**.  

⚠️ **Disclaimer:** This tool is for **research and educational purposes only**. It is **not a substitute** for professional medical diagnosis.

---

## 🚀 Features

- 📂 Upload dermoscopic images (`.jpg`, `.jpeg`, `.png`)  
- 🩺 **AI Predictions** with confidence scores  
- 📖 **Educational explanations** for each disease class (layman-friendly)  
- 📝 **Downloadable report** with prediction results  
- 🎨 User-friendly Streamlit UI  
- ☁️ Deployable via **Colab + ngrok** or **Streamlit Cloud**  

---

## 🔧 Tech Stack

- **Language:** Python 3.10+  
- **Framework:** [Streamlit](https://streamlit.io/)  
- **Model Hub:** Hugging Face Transformers  
- **Model:** ConvNeXtV2 Large, fine-tuned on HAM10000  
- **Other:** PyTorch, PIL, ngrok (for Colab hosting)  

---

## 📂 Repository Structure

DermAI/

├─ dermAI.py # Main Streamlit app

├─ requirements.txt # Python dependencies

├─ docs/

│ ├─ screenshot.png # UI preview

│ └─ results.png # Example results/confusion matrix

└─ README.md


---

## ▶️ Getting Started

1) Clone Repo
```bash
git clone https://github.com/imtiazhumzah/Final-project/DermAI.git
cd DermAI

2) Create virtual environment
python -m venv .venv
source .venv/bin/activate   # (Windows: .venv\Scripts\activate)

3) Install Dependencies
pip install -r requirements.txt

4) Run Streamlit app
streamlit run dermAI.py

The app will be available at:
👉 http://localhost:8501

☁️ Run in Google Colab

You can also run DermAI in Google Colab with public access using ngrok:
!pip install streamlit pyngrok
from pyngrok import ngrok
ngrok.kill()

# Set up ngrok auth token (replace with your own or Colab secret)
ngrok.set_auth_token("<YOUR_AUTH_TOKEN>")

# Run Streamlit
!streamlit run dermAI.py &> /dev/null &

# Expose tunnel
public_url = ngrok.connect('8501')
print(f"Streamlit app is live at: {public_url}")

🧠 Model Information

Base Model: ConvNeXtV2 Large

Dataset: HAM10000

Classes:

mel – Melanoma

nv – Melanocytic Nevus

bcc – Basal Cell Carcinoma

akiec – Actinic Keratoses

bkl – Benign Keratosis

df – Dermatofibroma

vasc – Vascular Lesions

📊 Example Prediction

Input:


Output:

🩺 Prediction: Melanoma

🎯 Confidence: 92.14%

📖 Description: “Melanoma is a serious and aggressive form of skin cancer...”


🛣️ Roadmap (Planned Features)

 🔥 Grad-CAM visualization → highlight lesion areas influencing the decision

 🌍 Multilingual support (English, German, French, Urdu)

 📲 Mobile-friendly UI → deploy as PWA or TFLite model for offline use

 📦 Cloud hosting → deploy on Streamlit Cloud / Hugging Face Spaces

 ⚖️ Bias & fairness analysis → evaluate across skin tones and demographics

 🛡️ Privacy-first mode → ensure no image is stored after inference


🙌 Contributing

We welcome contributions! To contribute:

Fork the repo

Create a feature branch (git checkout -b feature-x)

Commit changes and push

Submit a Pull Request 🚀


👏 Acknowledgements

HAM10000 Dataset

Hugging Face Transformers

Streamlit Team


## 📸 Screenshots

### Home Page
![Home Page](assets/Front page.png)

### Upload Image
![Upload Image](assets/uploaded image.png)

### Prediction Result
![Prediction Result](assets/predicitons.png)

