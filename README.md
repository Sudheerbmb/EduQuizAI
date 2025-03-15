# MCQ Generator Web Application

This Flask web application allows users to upload PDF, DOCX, or TXT files and generate multiple-choice questions (MCQs) using the Google Gemini Pro model.

## Prerequisites

- Python 3.6+
- Google Cloud API key (with access to Gemini Pro)
- Required Python libraries:
  - Flask
  - pdfplumber
  - python-docx
  - google-generativeai
  - werkzeug
  - fpdf

## Installation

1.  **Clone the repository (or create a new directory):**

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    ```

3.  **Activate the virtual environment:**

    -   On Windows:

        ```bash
        venv\Scripts\activate
        ```

    -   On macOS and Linux:

        ```bash
        source venv/bin/activate
        ```

4.  **Install the required libraries:**

    ```bash
    pip install Flask pdfplumber python-docx google-generativeai werkzeug fpdf
    ```

5.  **Set your Google Cloud API key:**

    -   Replace `"AIzaSyAVULbvvHDSZ1SkPxZFhOGbL2bnQA6kPK8"` in the `app.py` file with your actual API key.
    -   Alternatively, set the `GOOGLE_API_KEY` environment variable:

        ```bash
        export GOOGLE_API_KEY="YOUR_API_KEY" #For linux and mac
        set GOOGLE_API_KEY="YOUR_API_KEY" #For windows
        ```

## Usage

1.  **Run the Flask application:**

    ```bash
    python app.py
    ```

2.  **Open your web browser and navigate to `http://127.0.0.1:5000/`:**

3.  **Upload a PDF, DOCX, or TXT file.**

4.  **Enter the number of MCQs you want to generate.**

5.  **Click the "Generate MCQs" button.**

6.  **The generated MCQs will be displayed on the results page.**

7.  **You can download the MCQs as a text file or a PDF file.**

## File Structure
-   `app.py`: The main Flask application file.
-   `templates/`: Contains the HTML templates.
    -   `index.html`: The main page for uploading files and generating MCQs.
    -   `results.html`: Displays the generated MCQs and download links.
-   `uploads/`: Stores the uploaded files.
-   `results/`: Stores the generated MCQ files (TXT and PDF).

## Functionality

-   **File Upload:** Users can upload PDF, DOCX, or TXT files.
-   **Text Extraction:** The application extracts text from the uploaded files.
-   **MCQ Generation:** The Google Gemini Pro model generates MCQs based on the extracted text.
-   **File Saving:** The generated MCQs are saved as TXT and PDF files.
-   **File Download:** Users can download the generated MCQ files.
-   **Error Handling:** Basic error handling for invalid file formats and missing files.
-   **Dynamic Question Number:** The user can specify the number of questions they want to generate.

## Dependencies

-   Flask: A web framework for Python.
-   pdfplumber: For extracting text from PDF files.
-   python-docx: For extracting text from DOCX files.
-   google-generativeai: For interacting with the Google Gemini Pro model.
-   werkzeug: For secure file uploads.
-   fpdf: for creating pdf files.

## Notes

-   Ensure that your Google Cloud API key has access to the Gemini Pro model.
-   The quality of the generated MCQs depends on the quality of the input text and the capabilities of the Gemini Pro model.
-   This application is for demonstration purposes and may require further development for production use.
-   Consider adding more robust error handling and input validation.
-   Add more user friendly features.
  
