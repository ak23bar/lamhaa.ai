# Lamhaa.ai

**Lamhaa.ai** is an AI-powered image curation tool that intelligently organizes your photo collections by semantic content and perceptual quality. Built with FastAPI and powered by the CLIP model, it analyzes uploaded photos, identifies top picks based on sharpness, clusters similar images, and moves low-quality ones into a Trash folder.

Derived from the Urdu word **"Lamhaa"** (لمحہ) — meaning *moment* — this project is designed to help you preserve what matters most, automatically.

---

## ✨ Features

- 📸 **Semantic Clustering** using CLIP embeddings
- 🧠 **Perceptual Quality Ranking** via image sharpness
- 🗂️ **Smart Folder Output**: `Best`, `Clusters`, `Trash`
- ⚡ **FastAPI Backend** for easy integration and scaling

---

## 🧾 Prerequisites

- Python 3.9 or higher
- JPEG-format images only (for now)

---

## ⚙️ Setup & Run

1. **Clone the repository**
```bash
git clone https://github.com/your-username/lamhaa.ai.git
cd lamhaa.ai
