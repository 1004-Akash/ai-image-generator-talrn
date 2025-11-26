# 🎨 AI-Powered Image Generator
### **Talrn ML Internship – Assessment Submission**

An end-to-end **Text-to-Image Generation System** powered by **Stable Diffusion v1.5**, featuring  
prompt enhancement, safety filtering, metadata logging, and an interactive Gradio UI.

---

## 📌 Project Highlights

- 🎨 **Five Style Presets:** Photorealistic, Artistic, Cartoon, Cinematic, Fantasy  
- 🛡️ **Safety Pipeline:** NSFW prompt filtering + transparent watermark  
- 🤖 **Smart Prompt Engineering:** Style enhancement & negative prompts  
- 💾 **Metadata Logging:** JSON file stored for every generated image  
- 🌐 **Gradio Web UI:** Clean, intuitive, real-time interface  
- ⚡ **Auto GPU/CPU Selection:** Optimized for both environments  

---

## OUTPUT

<img width="462" height="453" alt="Screenshot 2025-11-26 231052" src="https://github.com/user-attachments/assets/4703733a-d2b3-4f4f-810e-b16f203b6a3c" />
<img width="455" height="457" alt="Screenshot 2025-11-26 231124" src="https://github.com/user-attachments/assets/20e4fec8-b781-42da-9ab9-e07508a1dc46" />
<img width="460" height="457" alt="Screenshot 2025-11-26 231148" src="https://github.com/user-attachments/assets/c900dc0c-60f1-481f-8f0b-1eb5fce54f61" />



# 🏗️ Architecture Overview

┌──────────────────────────────────────────────┐
│ Gradio UI │
│ (Prompt, Style, Num Images, Steps, Seed) │
└───────────────────────────┬──────────────────┘
│
▼
┌──────────────────────────────────────────────┐
│ Prompt Engineering Module │
│ - Safety Keyword Filtering │
│ - Style Preset Enhancements │
│ - Quality Boost Tags + Negative Prompts │
└───────────────────────────┬──────────────────┘
│
▼
┌──────────────────────────────────────────────┐
│ Stable Diffusion v1.5 │
│ - CLIP Text Encoder │
│ - U-Net Diffusion Model │
│ - VAE Decoder │
│ - DPM-Solver++ Scheduler │
└───────────────────────────┬──────────────────┘
│
▼
┌──────────────────────────────────────────────┐
│ Post-Processing Layer │
│ - AI Watermark │
│ - Metadata Export (JSON) │
│ - File Storage (/outputs/) │
└──────────────────────────────────────────────┘


---

# 🛠️ Tech Stack

| Component  | Technology |
|-----------|------------|
| Model     | Stable Diffusion v1.5 |
| Framework | PyTorch 2.x |
| UI        | Gradio 4.x |
| Pipeline  | HuggingFace Diffusers |
| Scheduler | DPM-Solver++ |
| Metadata  | JSON + Pillow |
| Safety    | Keyword Filter + SD Safety Checker |

---

# 🚀 Installation & Setup

### **Prerequisites**
- Python **3.10+**  
- At least **5GB free storage**  
- RAM Requirements  
  - CPU: **16GB minimum**  
  - GPU: **8GB+ VRAM recommended**

---

## **1. Clone the Repository**

git clone https://github.com/YOUR-USERNAME/ai-image-generator-talrn.git
cd ai-image-generator-talrn

2. Install Dependencies
pip install -r requirements.txt

3. Launch the Notebook
Google Colab (Recommended)

Open ai_image_generator.ipynb

Runtime → Run all

Click the generated Gradio URL

Local Machine
jupyter notebook ai_image_generator.ipynb

💻 Hardware Requirements
Minimum (CPU Mode)

16GB RAM

2–5 minutes per image

Recommended (GPU Mode)

NVIDIA T4 / RTX 3060 / 3080+

~15–30 seconds per image

Performance Benchmarks
Platform	Device	RAM	Speed
Colab Free	CPU	12GB	3–4 min/image
Colab Pro	T4 GPU	25GB	20–25 sec/image
Local System	RTX 3080	32GB	12–18 sec/image
📖 Usage Guide
Generating Images

Launch Gradio interface

Enter a text prompt

Choose a style preset

Configure:

Number of images

Steps (20–50 recommended)

Seed (optional)

Click Generate Images

View & download output + metadata

✨ Example Prompts
Landscape

"A serene mountain lake at golden hour, mist rising, ultra detailed"

Portrait

"Cyberpunk warrior portrait, neon lights, hyper-realistic lens effects"

Fantasy

"Ancient mystical forest with glowing spirits and fog, fantasy art"

Cartoon

"Cute cat wizard casting a spell, colorful cartoon style"

💡 Prompt Engineering Tips

✔️ Be Specific
❌ "a car"
✔️ "A red sports car drifting on a mountain road during sunset"

✔️ Use Quality Enhancers

highly detailed

4K

sharp focus

professional lighting

✔️ Use Negative Prompts
Default negatives:

blurry, distorted, low quality, deformed, watermark

⚠️ Limitations

Output resolution: 512×512 (optimized for speed)

CPU mode is significantly slower

Gradio share links expire after 72 hours

Minor facial imperfections may occur

Some prompts may be incorrectly flagged as unsafe

🚀 Future Improvements
v2.0 (Near Term)

Support 768×768 & 1024×1024

Batch prompt input

ControlNet for pose/edge conditioning

Image-to-image generation

v3.0 (Mid Term)

LoRA fine-tuning

Inpainting & outpainting

Style transfer

v4.0 (Long Term)

Text-to-video

3D asset generation

Full REST API

Mobile application

📂 Project Structure
ai-image-generator-talrn/
│
├── ai_image_generator.ipynb     # Main notebook
├── README.md                     # This documentation
├── requirements.txt              # Dependencies
├── LICENSE                       # MIT License
│
├── outputs/                      # Generated images + metadata
│   ├── image_YYYYMMDD_HHMMSS.png
│   ├── image_YYYYMMDD_HHMMSS.json
│
├── samples/                      # Sample outputs
│
└── docs/                         # Additional documentation
    ├── ARCHITECTURE.md
    ├── PROMPT_GUIDE.md
    └── TROUBLESHOOTING.md
