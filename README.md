# MediScan AI - Professional Medical Image Analysis Platform

A cutting-edge web application for AI-powered medical image analysis, featuring a professional frontend and robust backend API.

## 🚀 Features

- **Professional Medical Website**: Modern, responsive design with medical aesthetics
- **AI-Powered Analysis**: Advanced Google Gemini AI for medical image diagnosis
- **FastAPI Backend**: High-performance REST API for image analysis
- **Secure & Private**: Enterprise-grade security for medical data
- **Real-time Processing**: Instant analysis results with loading indicators
- **Multi-format Support**: JPEG, PNG, JPG image formats
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile

## 🏥 Medical Capabilities

- **Disease Detection**: Cancer, cardiovascular diseases, neurological conditions
- **Image Analysis**: X-rays, CT scans, MRIs, ultrasounds
- **Structured Reports**: Detailed diagnosis with confidence levels
- **Clinical Insights**: Professional medical recommendations

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8+
- pip package manager
- Google Gemini API key

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Configure API Key
Update the `API_KEY` in `backend.py` with your Google Gemini API key:
```python
genai.configure(api_key="YOUR_API_KEY_HERE")
```

### 3. Run the Application

#### Option A: FastAPI Backend (Recommended)
```bash
python backend.py
```
The professional website will be available at: `http://localhost:8000`

#### Option B: Streamlit App (Backup)
```bash
streamlit run main.py
```
Streamlit app will be available at: `http://localhost:8501`

## 📁 Project Structure

```
DISEASE PREDICTION/
├── backend.py          # FastAPI backend with AI analysis
├── main.py            # Streamlit backup app
├── index.html         # Professional frontend
├── styles.css         # Modern CSS styling
├── script.js          # Frontend JavaScript
├── requirements.txt   # Python dependencies
└── README.md          # This file
```

## 🔧 API Endpoints

### POST `/api/analyze`
Upload and analyze medical images.

**Request:**
- Content-Type: `multipart/form-data`
- Body: `file` (image file)

**Response:**
```json
{
  "success": true,
  "analysis": "Detailed medical analysis report...",
  "filename": "xray.jpg",
  "file_size": 245760
}
```

### GET `/api/health`
Health check endpoint.

**Response:**
```json
{
  "status": "healthy",
  "service": "Medical Image Analysis API"
}
```

## 🎨 Frontend Features

- **Hero Section**: Professional landing with call-to-action
- **Drag & Drop Upload**: Intuitive file upload interface
- **Real-time Analysis**: Live processing with loading states
- **Results Display**: Formatted medical reports
- **Responsive Design**: Mobile-first approach
- **Medical Theme**: Healthcare-appropriate color scheme
- **Smooth Animations**: Professional transitions and effects

## 🔒 Security & Privacy

- **HIPAA Compliant**: Designed for medical data handling
- **Secure API**: Protected endpoints with proper validation
- **File Validation**: Type and size restrictions
- **Error Handling**: Comprehensive error management
- **No Data Storage**: Images processed in memory only

## 🚀 Deployment

### Local Development
```bash
# Install dependencies
pip install -r requirements.txt

# Run backend
python backend.py

# Open http://localhost:8000 in browser
```

### Production Deployment
- Use a WSGI server like Gunicorn for FastAPI
- Configure reverse proxy with Nginx
- Set up SSL certificates
- Use environment variables for API keys
- Implement proper logging and monitoring

## 📞 Support

For technical support or questions:
- Email: support@mediscan.ai
- Documentation: Check API endpoints above

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## ⚠️ Disclaimer

This application is designed to assist healthcare professionals and should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with qualified healthcare providers for medical decisions.
