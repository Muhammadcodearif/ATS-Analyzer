# ATS-Analyzer

An intelligent Applicant Tracking System (ATS) analyzer that evaluates resumes against job descriptions using AI-powered analysis. This tool helps job seekers optimize their resumes for better compatibility with ATS systems used by recruiters and hiring managers.

## 🚀 Features

- **Resume Analysis**: Parse and analyze resumes in various formats (PDF, DOCX, TXT)
- **Job Description Matching**: Compare resumes against specific job descriptions
- **Keyword Extraction**: Identify missing keywords crucial for job applications
- **ATS Score Calculation**: Get a percentage match score for resume-job compatibility
- **Improvement Suggestions**: Receive actionable recommendations to enhance your resume
- **Skills Assessment**: Analyze and categorize technical and soft skills
- **Entity Recognition**: Extract important entities like experience, education, and certifications

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Jupyter Notebook**: Interactive development environment
- **Natural Language Processing (NLP)**: Text analysis and processing
- **Machine Learning**: Resume scoring and matching algorithms
- **PDF/Document Processing**: Resume parsing capabilities
- **Streamlit** (if applicable): Web interface for user interaction

## 📋 Prerequisites

Before running this project, ensure you have the following installed:

- Python 3.7 or higher
- pip (Python package installer)
- Jupyter Notebook or JupyterLab

## 🔧 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Muhammadcodearif/ATS-Analyzer.git
   cd ATS-Analyzer
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

   If requirements.txt is not available, install common dependencies:
   ```bash
   pip install pandas numpy scikit-learn nltk spacy textblob
   pip install pypdf2 python-docx streamlit plotly
   pip install jupyter notebook
   ```

4. **Download required NLP models:**
   ```bash
   python -m spacy download en_core_web_sm
   python -m nltk.downloader punkt stopwords
   ```

## 🎯 Usage

### Running the Jupyter Notebook

1. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

2. **Open the main notebook:**
   - Navigate to `ATS_2.ipynb` in your browser
   - Run cells sequentially to execute the analysis

### Basic Usage Example

```python
# Import necessary libraries
from ats_analyzer import ATSAnalyzer

# Initialize the analyzer
analyzer = ATSAnalyzer()

# Load resume and job description
resume_path = "path/to/your/resume.pdf"
job_description = "Your job description text here..."

# Analyze resume
results = analyzer.analyze_resume(resume_path, job_description)

# View results
print(f"ATS Score: {results['ats_score']}%")
print(f"Missing Keywords: {results['missing_keywords']}")
print(f"Recommendations: {results['recommendations']}")
```

## 📊 Output Features

The ATS Analyzer provides comprehensive analysis including:

- **Match Percentage**: Overall compatibility score between resume and job description
- **Keyword Analysis**: 
  - Found keywords in the resume
  - Missing important keywords
  - Keyword frequency analysis
- **Skills Gap Analysis**: Identification of skills mentioned in JD but missing in resume
- **Recommendations**: Specific suggestions to improve ATS compatibility
- **Resume Summary**: AI-generated summary of the candidate's profile
- **Visualization**: Charts and graphs showing analysis results

## 🔍 How It Works

1. **Text Extraction**: Extracts text from uploaded resume files
2. **Preprocessing**: Cleans and normalizes text data
3. **Keyword Matching**: Compares resume keywords with job description requirements
4. **Scoring Algorithm**: Calculates compatibility score based on multiple factors:
   - Keyword overlap
   - Skills matching
   - Experience relevance
   - Education alignment
5. **Analysis Generation**: Provides detailed feedback and recommendations

## 📁 Project Structure

```
ATS-Analyzer/
│
├── ATS_2.ipynb              # Main Jupyter notebook
├── requirements.txt         # Python dependencies
├── data/                    # Sample data files
│   ├── sample_resumes/
│   └── job_descriptions/
├── models/                  # Trained models (if any)
├── utils/                   # Utility functions
│   ├── text_processing.py
│   ├── keyword_extraction.py
│   └── scoring.py
├── assets/                  # Images and other assets
└── README.md               # Project documentation
```

## 🤝 Contributing

We welcome contributions to improve the ATS-Analyzer! Here's how you can contribute:

1. **Fork the repository**
2. **Create a feature branch:**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes:**
   ```bash
   git commit -m 'Add some amazing feature'
   ```
4. **Push to the branch:**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

## 📈 Roadmap

- [ ] Support for more resume formats
- [ ] Integration with job portal APIs
- [ ] Real-time resume optimization suggestions
- [ ] Machine learning model improvements
- [ ] Multi-language support
- [ ] Resume template recommendations
- [ ] Bulk resume processing

## 🐛 Issues and Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/Muhammadcodearif/ATS-Analyzer/issues) page
2. Create a new issue with detailed description
3. Include error logs and system information

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Thanks to the open-source community for NLP libraries
- Inspired by modern ATS systems and recruitment processes
- Built with the goal of helping job seekers succeed

## 📞 Contact

- **Author**: Muhammad Code Arif
- **GitHub**: [@Muhammadcodearif](https://github.com/Muhammadcodearif)
- **Project Link**: [ATS-Analyzer](https://github.com/Muhammadcodearif/ATS-Analyzer)

---

⭐ **Star this repository if you find it helpful!**

*Made with ❤️ to help job seekers optimize their resumes for ATS systems*
