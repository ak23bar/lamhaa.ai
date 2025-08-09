# Lamhaa.ai ⚡

**AI-powered photo culling that processes thousands of images in minutes, not hours**

> *Lamhaa* (لمحہ) means "moment" in Urdu — because that's all the time you need to transform photo chaos into organized brilliance.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

---

## Overview

Lamhaa.ai is an early-stage, open-source project aimed at solving one of the most time-consuming tasks in professional photography — manual image culling.

The goal is to build a local-first platform that uses computer vision, deep learning embeddings, and clustering algorithms to automatically:

- Find the best shots from large collections
- Remove duplicates and group similar photos  
- Deliver a curated, ready-to-review set in minutes instead of hours

This README outlines the vision, market opportunity, and planned roadmap. Implementation is in progress — the MVP will be built in phases to ensure scalability and maintainability from the ground up.

---

## Market Opportunity

Manual photo organization is a significant workflow bottleneck across industries:

- Wedding photographers spend 6-8 hours culling 3,000+ images per event
- E-commerce platforms require strict quality control across millions of SKUs
- Marketing agencies and media teams manage vast visual asset libraries

**Relevant market sizes:**
- Global photography market: $105.2B (2023)
- Photo management software market: $3.6B in 2023 → projected $5.9B by 2032

---

## Planned Technical Approach

**Quality Scoring** — Sharpness, exposure, contrast, and composition metrics using computer vision
**Duplicate Detection** — Perceptual hashing to identify identical/near-identical images
**Content Clustering** — CLIP embeddings + DBSCAN/HDBSCAN to group similar shots
**Keeper Selection** — Rule-based initially, evolving to ML-based predictions with user feedback
**Local-First Processing** — Zero-trust design; no mandatory cloud uploads

---

## Target Applications

### Photography Professionals
Event, wedding, and studio photographers processing thousands of images weekly

### Commercial & Enterprise  
- E-commerce platforms automating quality control
- Marketing agencies organizing multi-client assets
- Publishing companies managing image archives

### Content Platforms
- Stock photography platforms for metadata and quality scoring
- Social media teams managing high-volume content pipelines

---

## Development Roadmap

### Phase 1 — Core Infrastructure (MVP)
- CLI and API-based end-to-end pipeline
- Basic quality scoring, duplicate detection, and grouping
- FastAPI backend with job tracking

### Phase 2 — Feedback & ML Integration  
- User review system for keeper selection
- Train ML model (RandomForest or similar) to adapt to preferences
- Model persistence for continuous learning

### Phase 3 — User Interface
- Minimal React dashboard for uploads and results
- Hugging Face Space for a free, public mini-demo
- Enhanced result visualization

### Phase 4 — Enterprise Features
- Brand/style consistency scoring
- Bulk tagging and categorization
- Batch processing optimization

---

## Technical Stack

**Core Technologies:**
- **Backend**: FastAPI with asynchronous processing
- **Computer Vision**: OpenCV, Pillow for image processing
- **Machine Learning**: PyTorch, scikit-learn, OpenAI CLIP embeddings
- **Algorithms**: DBSCAN clustering, perceptual hashing, quality metrics

**Architecture Principles:**
- Local-first processing with privacy by design
- Scalable pipeline capable of handling enterprise workloads
- Modular design for easy feature addition and testing

---

## Current Status

**Project Stage**: Initial development phase

- Repository structure and tech stack confirmed
- Core architecture design completed  
- Implementation of MVP pipeline in progress
- First priority: Complete Phase 1 core functionality

**What's Built**: Project foundation and technical planning  
**What's Next**: MVP processing pipeline with basic quality scoring and duplicate detection

---

## Installation (Coming Soon)

Setup instructions will be added once the MVP pipeline is ready. Planned workflow:

```bash
git clone https://github.com/ak23bar/lamhaa.ai.git
cd lamhaa.ai

python3 -m venv lamhaa_env
source lamhaa_env/bin/activate  # Windows: lamhaa_env\Scripts\activate

pip install -r requirements.txt

# Run the API server
uvicorn app.main:app --reload
```

---

## Contributing

This is an active work in progress. Contributions, ideas, and feedback are welcome as Lamhaa.ai grows from concept to production-ready platform.

**How to contribute:**
- Star the repository to follow development progress
- Open issues for feature suggestions or feedback  
- Reach out via email for collaboration opportunities

---

## License

MIT License — free to use, modify, and distribute.

---

## Contact

**Email**: akbaraman797@gmail.com  
**GitHub**: [@ak23bar](https://github.com/ak23bar)

---

*Note: This is an active work in progress. The vision is ambitious, the technical approach is sound, and development is underway to deliver a powerful solution for photography workflow automation.*
