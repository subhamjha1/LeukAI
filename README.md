# LeukAI — Leukemia Stage Classification Web App

**Delhi Technological University | Biotechnology Engineering | 2026**

Deep Learning & Vision–Language Framework for Automated Leukemia Stage Classification from Blood Smear Images.

## Features

- 🔬 Upload peripheral blood smear images (PNG/JPG)
- 🧬 4-class leukemia staging: Benign, Pre-leukemic, Early, Advanced (Pro)
- 📊 Probability distribution across all 4 classes
- 🧪 Morphological feature analysis
- ⚕ Clinical recommendations
- 📦 Batch analysis support (multiple images)
- 📱 Responsive design

## How It Works

This app simulates the CNN + VLM ensemble framework from the research paper:

1. **Inception V3 CNN** — Classifies blood smear images (visual feature extraction)
2. **Qwen3-VL Reasoning** — Independent vision-language analysis
3. **Ensemble Fusion** — Weighted combination: `P_final = 0.55×P_CNN + 0.45×P_VLM`

In this web demo, Claude Vision API (claude-opus-4-5) acts as the combined CNN+VLM system, providing calibrated probability estimates and morphological descriptions.

## Deploy on Render

### Option 1: Static Site (Recommended)

1. Upload this folder to GitHub
2. Go to [render.com](https://render.com) → New → Static Site
3. Connect your GitHub repo
4. Set **Publish directory** to `.`
5. Deploy!

### Option 2: Manual Deploy

```bash
# Just open index.html in browser — no server needed!
open index.html
```

## Usage

1. Open the app
2. Upload a blood smear image (Wright–Giemsa stained, 100× magnification works best)
3. Enter your Anthropic API key (`sk-ant-api...`)
4. Click **Analyze Sample**
5. View stage classification, probabilities, and clinical recommendations

## Research Paper

**"Calibration-Aware Ensemble Learning via CNN and VLM Fusion for Leukemia Stage Classification from Peripheral Blood Smear Images"**

- Authors: Subham Jha, Miss Sadia Sultana Juthi
- Supervisors: Dr. Shivani Khatri
- Institution: Delhi Technological University
- Model Accuracy: **99.18%** (Ensemble), **98.6%** (Inception V3 standalone)
- ECE (Calibration Error): **0.0053** (after VLM ensemble)

## Dataset

Kaggle Leukemia Blood Smear Dataset — 3,256 images across 4 classes:
- Benign: 504 images
- Pre-leukemic: 985 images  
- Early Leukemia: 963 images
- Advanced (Pro): 804 images

## Disclaimer

This tool is for **educational and research purposes only**. It is designed as a clinical decision-support tool and must not replace professional hematological diagnosis.
