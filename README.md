# ATS Resume Tracker

An AI-powered Applicant Tracking System that analyzes resumes against job descriptions using Google's Gemini AI to provide professional feedback and match percentages.

## Features

- **Resume Analysis**: Professional evaluation of candidate profiles
- **ATS Matching**: Percentage match between resume and job description
- **Missing Keywords**: Identifies gaps in resume content
- **PDF Processing**: Converts PDF resumes to images for AI analysis

## Prerequisites

- Google API Key (Gemini AI)
- Python 3.7+

## Installation

```bash
pip install streamlit google-generativeai pdf2image pillow python-dotenv
```

## Setup

1. **Create `.env` file**:
   ```
   GOOGLE_API_KEY=your_google_api_key_here
   ```

2. **Get Google API Key**:
   - Visit [Google AI Studio](https://aistudio.google.com/)
   - Generate an API key

## Usage

1. **Run the Application**:
   ```bash
   streamlit run app.py
   ```

2. **Using the Interface**:
   - Enter job description in the text area
   - Upload resume (PDF format only)
   - Choose analysis type:
     - **"Tell Me About the Resume"**: Professional evaluation
     - **"Percentage Match"**: ATS compatibility score

## How It Works

1. **PDF Conversion**: Converts uploaded PDF resume to JPEG image
2. **AI Analysis**: Uses Google Gemini to analyze resume content
3. **Comparison**: Matches resume against job description
4. **Feedback**: Provides detailed analysis and recommendations

## Analysis Types

### Professional Evaluation
- Strengths and weaknesses assessment
- Alignment with job requirements
- HR manager perspective

### ATS Matching
- Percentage compatibility score
- Missing keywords identification
- Final recommendations

## File Structure

```
├── app.py              # Main Streamlit application
├── .env               # Environment variables (API key)
└── requirements.txt   # Python dependencies
```

## Supported Formats

- **Input**: PDF resumes only
- **Job Descriptions**: Text format

## Technical Details

- **AI Model**: Google Gemini 2.0 Flash
- **PDF Processing**: pdf2image library
- **Frontend**: Streamlit web interface
- **Image Format**: JPEG conversion for AI processing
