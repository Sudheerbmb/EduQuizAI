# EduQuizAI - Intelligent MCQ Generator

EduQuizAI is an intelligent web-based application that automatically generates multiple-choice questions (MCQs) from educational documents using artificial intelligence. Built with Flask and powered by Groq's AI models, it helps teachers, students, and trainers quickly create assessment questions from PDF, DOCX, and TXT files.

## Features

- **Multi-format Support**: Upload PDF, DOCX, or TXT files
- **AI-Powered Generation**: Uses Groq's GPT-OSS model to generate high-quality MCQs
- **Customizable**: Specify the number of questions to generate
- **Export Options**: Download generated MCQs as TXT or PDF files
- **Modern UI**: Beautiful, responsive interface with drag-and-drop file upload
- **Secure**: Validates file types and handles uploads safely

## Prerequisites

- Python 3.6 or higher
- Groq API key ([Get one here](https://groq.com/))
- Required Python libraries (see Installation)

## Installation

1. **Clone the repository:**

   ```bash
   git clone <repository_url>
   cd EduQuizAI
   ```

2. **Create a virtual environment (recommended):**

   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment:**

   - On Windows:
     ```bash
     venv\Scripts\activate
     ```

   - On macOS and Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install the required dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

   Or install manually:
   ```bash
   pip install Flask pdfplumber python-docx groq fpdf Werkzeug python-dotenv
   ```

5. **Set up your Groq API key:**

   Create a `.env` file in the project root directory:

   ```bash
   # .env
   GROQ_API_KEY=your_groq_api_key_here
   ```

   **Important**: Never commit your `.env` file to version control. It's already included in `.gitignore`.

## Usage

1. **Start the Flask application:**

   ```bash
   python app.py
   ```

2. **Open your web browser and navigate to:**

   ```
   http://127.0.0.1:5000/
   ```

3. **Upload a document:**
   - Drag and drop a PDF, DOCX, or TXT file, or click to browse
   - Enter the number of MCQs you want to generate
   - Click "Generate MCQs"

4. **View and download:**
   - Review the generated MCQs on the results page
   - Download as TXT or PDF using the download buttons

## Project Structure

```
EduQuizAI/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (create this)
├── .gitignore            # Git ignore file
├── templates/            # HTML templates
│   ├── index.html       # Homepage with file upload
│   └── results.html     # Results page with generated MCQs
├── static/              # Static files (CSS, images)
│   └── logo.jpg         # Application logo
├── uploads/             # Uploaded files (auto-created)
└── results/             # Generated MCQ files (auto-created)
```

## Technologies Used

- **Backend Framework**: Flask
- **AI Integration**: Groq API (GPT-OSS 120B model)
- **Text Extraction**: 
  - `pdfplumber` for PDF files
  - `python-docx` for DOCX files
- **PDF Generation**: FPDF
- **Frontend**: HTML5, CSS3, JavaScript
- **Templating**: Jinja2
- **Security**: Werkzeug for secure file handling

## How It Works

1. User uploads a document (PDF, DOCX, or TXT)
2. The application extracts text from the document
3. The extracted text is sent to Groq's AI model with a structured prompt
4. The AI generates MCQs with four options and correct answers
5. Results are displayed on the web interface
6. Users can download MCQs as TXT or PDF files

## Configuration

The application uses environment variables for configuration. Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_api_key_here
```

## Error Handling

The application includes basic error handling for:
- Invalid file formats
- Missing files
- API connection issues
- Encoding problems

## Limitations

- Generation time depends on document size and API response time
- Quality of MCQs depends on the quality and structure of input documents
- Very large documents may require chunking (not currently implemented)
- Scanned PDFs without OCR support are not handled

## Future Enhancements

- User authentication and question history
- Question difficulty level selection
- Support for more file formats
- Batch processing for multiple documents
- Question categorization and tagging
- Integration with Learning Management Systems (LMS)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is developed as part of an internship project at Futurense Technologies.

## Author

**Thati Sudheer Kumar**

## Acknowledgments

- Futurense Technologies for the internship opportunity
- Groq for providing the AI API
- Flask community for excellent documentation

## Support

For issues, questions, or suggestions, please open an issue on the repository.

---

**Note**: This application is for educational and demonstration purposes. For production use, consider adding more robust error handling, authentication, rate limiting, and security measures.
