# ATS-Analyzer 📄✨

An intelligent Applicant Tracking System (ATS) analyzer that evaluates resume compatibility with job descriptions using AI-powered analysis. This tool helps job seekers optimize their resumes to pass through ATS filters and improve their chances of landing interviews.

## 🚀 Features

- **Resume Analysis**: Upload PDF resumes for comprehensive evaluation
- **Job Description Matching**: Compare resumes against specific job requirements
- **ATS Score Calculation**: Get percentage match scores for resume optimization
- **Keyword Analysis**: Identify missing keywords and skills
- **Improvement Suggestions**: Receive actionable feedback to enhance your resume
- **User-Friendly Interface**: Clean and intuitive web-based interface
- **Real-time Processing**: Fast analysis with immediate results

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **Backend**: Python
- **AI/ML**: Google Gemini Pro / OpenAI GPT (AI-powered analysis)
- **PDF Processing**: PyPDF2 / pdfplumber
- **Additional Libraries**: 
  - pandas
  - numpy
  - streamlit
  - python-dotenv

## 📋 Prerequisites

Before running this application, make sure you have:

- Python 3.8 or higher
- pip package manager
- API key for AI service (Google Gemini Pro or OpenAI)

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Muhammadcodearif/ATS-Analyzer.git
   cd ATS-Analyzer
   ```

2. **Create virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` file and add your API keys:
   ```
   GOOGLE_API_KEY=your_google_gemini_api_key
   # or
   OPENAI_API_KEY=your_openai_api_key
   ```

## 🚀 Usage

1. **Start the application**
   ```bash
   streamlit run app.py
   ```

2. **Open your browser** and navigate to `http://localhost:8501`

3. **Upload your resume** in PDF format

4. **Paste the job description** in the provided text area

5. **Choose analysis type**:
   - Resume Overview
   - Percentage Match
   - Missing Keywords
   - Improvement Suggestions

6. **Get your results** and optimize your resume accordingly!

## 📊 Analysis Features

### Resume Overview
Get a comprehensive summary of your resume including:
- Professional strengths
- Key skills identified
- Experience highlights
- Areas for improvement

### Percentage Match
Receive a numerical score (0-100%) indicating how well your resume aligns with the job description.

### Missing Keywords
Identify important keywords and skills from the job description that are missing from your resume.

### Improvement Suggestions
Get specific, actionable recommendations to enhance your resume's ATS compatibility.

## 📁 Project Structure

```
ATS-Analyzer/
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── .env.example          # Environment variables template
├── .gitignore           # Git ignore file
├── README.md            # Project documentation
├── utils/
│   ├── __init__.py
│   ├── pdf_processor.py # PDF text extraction
│   ├── ai_analyzer.py   # AI analysis functions
│   └── helpers.py       # Utility functions
└── assets/
    └── images/          # UI images and icons
```

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
# Google Gemini Pro (recommended)
GOOGLE_API_KEY=your_google_api_key_here

# Alternative: OpenAI GPT
OPENAI_API_KEY=your_openai_api_key_here

# App Configuration
DEBUG=False
MAX_FILE_SIZE=10  # MB
SUPPORTED_FORMATS=pdf
```

### API Key Setup

#### Google Gemini Pro (Recommended)
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a new API key
3. Add it to your `.env` file

#### OpenAI Alternative
1. Visit [OpenAI Platform](https://platform.openai.com/api-keys)
2. Create a new API key
3. Add it to your `.env` file

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Issues

If you encounter any issues or have suggestions, please [create an issue](https://github.com/Muhammadcodearif/ATS-Analyzer/issues) on GitHub.

## 🙏 Acknowledgments

- Google Gemini Pro for AI-powered analysis
- Streamlit for the amazing web framework
- The open-source community for inspiration

## 📞 Contact

- **Developer**: Muhammad Arif
- **GitHub**: [@Muhammadcodearif](https://github.com/Muhammadcodearif)
- **Project Link**: [https://github.com/Muhammadcodearif/ATS-Analyzer](https://github.com/Muhammadcodearif/ATS-Analyzer)

---

⭐ **If this project helped you, please give it a star!** ⭐

## 🚀 Quick Start Example

```python
# Example usage in your own code
from utils.ai_analyzer import analyze_resume
from utils.pdf_processor import extract_text

# Extract text from PDF
resume_text = extract_text("path/to/resume.pdf")
job_description = "Your job description here..."

# Analyze resume
result = analyze_resume(resume_text, job_description)
print(f"Match Score: {result['score']}%")
print(f"Suggestions: {result['suggestions']}")
```

---

**Happy Job Hunting! 🎯**
