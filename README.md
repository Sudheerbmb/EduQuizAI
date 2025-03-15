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
