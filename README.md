# Lamhaa.ai 📸

**AI-Powered Image Organization & Curation**

**Lamhaa.ai** is an intelligent image organization tool that automatically curates your photo collections by content relevance and visual quality. It analyzes uploaded images to identify your best shots, group similar photos, and filter out low-quality ones — all through an automated and scalable backend.

The name *Lamhaa* (لمحہ) comes from the Urdu word for "moment" — reflecting the project's goal of helping users rediscover meaningful moments through intelligent visual organization.

## ✨ Features

- **🧠 Intelligent Image Grouping**: Content-based similarity analysis for automatic photo clustering
- **🔍 Quality Assessment**: Automatic sharpness and quality filtering to surface your best shots
- **🗂️ Organized Output**: Clean folder structure (`Best`, `Groups`, `Trash`) for effortless browsing
- **⚡ FastAPI Backend**: High-performance API with support for bulk uploads
- **🔌 Extensible Architecture**: Ready for tagging, search, cloud sync, and advanced AI features
- **🛡️ Privacy-First**: All processing happens locally — your photos never leave your machine

## 🚀 Tech Stack

- **Backend Framework**: FastAPI
- **Computer Vision**: OpenCV, PIL (Pillow)
- **AI/ML**: scikit-learn, NumPy
- **Image Processing**: Custom sharpness detection algorithms
- **API Documentation**: Automatic OpenAPI/Swagger integration
- **Python**: 3.9+

## 📋 Prerequisites

- Python 3.9 or higher
- pip package manager
- Virtual environment (recommended)
- JPEG images only (currently supported)

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/lamhaa.ai.git
cd lamhaa.ai
```

### 2. Create Virtual Environment (Linux/macOS)
```bash
# Create virtual environment
python3 -m venv lamhaa_env

# Activate virtual environment
source lamhaa_env/bin/activate

# Upgrade pip
pip install --upgrade pip
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Application
```bash
# Start the FastAPI server
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

The API will be available at `http://localhost:8000`

## 📖 API Usage

### Interactive Documentation
Visit `http://localhost:8000/docs` for the automatic Swagger UI documentation.

### Upload Photos (Postman/cURL)

**Endpoint**: `POST /upload`

**Using Postman**:
1. Set method to `POST`
2. URL: `http://localhost:8000/upload`
3. Go to "Body" → "form-data"
4. Add key: `files` (set type to "File")
5. Select multiple JPEG files
6. Send request

**Using cURL**:
```bash
curl -X POST "http://localhost:8000/upload" \
  -H "accept: application/json" \
  -H "Content-Type: multipart/form-data" \
  -F "files=@photo1.jpg" \
  -F "files=@photo2.jpg"
```

### Response Example
```json
{
  "status": "success",
  "processed_files": 15,
  "best_shots": 8,
  "groups_created": 3,
  "moved_to_trash": 4,
  "processing_time_seconds": 12.3
}
```

## 📁 Output Structure

After processing, Lamhaa.ai organizes your photos into a clean, intuitive structure:

```
output/
├── Best/
│   ├── IMG_001.jpg    # Highest quality shots
│   ├── IMG_005.jpg
│   └── IMG_012.jpg
├── Groups/
│   ├── group_1/       # Similar content cluster
│   │   ├── IMG_003.jpg
│   │   └── IMG_008.jpg
│   ├── group_2/       # Another content cluster
│   │   ├── IMG_002.jpg
│   │   └── IMG_011.jpg
│   └── group_3/
│       └── IMG_007.jpg
└── Trash/
    ├── IMG_004.jpg    # Blurry/low quality
    └── IMG_009.jpg    # Poor sharpness
```

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the root directory:

```env
# Server Configuration
HOST=0.0.0.0
PORT=8000

# Processing Settings
MAX_FILE_SIZE_MB=10
SUPPORTED_FORMATS=jpg,jpeg
SHARPNESS_THRESHOLD=100.0

# Output Paths
OUTPUT_DIR=./output
BEST_DIR=./output/Best
GROUPS_DIR=./output/Groups
TRASH_DIR=./output/Trash
```

## 🧪 Development

### Running Tests
```bash
# Install development dependencies
pip install -r requirements-dev.txt

# Run tests
pytest tests/

# Run with coverage
pytest --cov=src tests/
```

### Code Formatting
```bash
# Format code with black
black src/

# Sort imports
isort src/

# Lint with flake8
flake8 src/
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with FastAPI for high-performance async capabilities
- Computer vision powered by OpenCV and PIL
- Inspired by the need for intelligent, privacy-first photo management
- *Lamhaa* (لمحہ) - helping you rediscover meaningful moments

---

**Made with ❤️ for photographers and AI enthusiasts**

*Lamhaa.ai - Where AI meets your cherished moments*
