# AI Resume & Cover Letter Generator

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.25%2B-red.svg)](https://streamlit.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A powerful web application built with Streamlit that leverages the Mistral AI API to generate professional, one-page resumes and tailored cover letters. The application provides a user-friendly interface to input personal and professional details, which are then used to create well-formatted, downloadable PDF documents.

![Screenshot of the AI Resume Generator](https://i.imgur.com/kPz8C7F.png)

## 🌟 Features

-   **Dual Functionality**: Generate both resumes and cover letters via a clean, tabbed interface.
-   **AI-Powered Content**: Utilizes the `mistral-medium` model to draft concise, impactful, and professional content based on user inputs.
-   **Structured Resume Generation**: Creates a classic, single-page resume with clear sections and professional formatting.
-   **Tailored Cover Letters**: Generates personalized cover letters by combining user details with information about the target company and position.
-   **Instant PDF Export**: Automatically converts the generated text into a polished, downloadable PDF document using the `FPDF` library.
-   **Secure & Local**: Runs entirely on your local machine. Your data is not stored or shared.

## ⚙️ How It Works

1.  **User Input**: The user fills out the form fields in the Streamlit web interface for either a resume or a cover letter.
2.  **Prompt Engineering**: The application dynamically constructs a detailed prompt for the Mistral AI API, incorporating the user's data and specific formatting instructions.
3.  **API Call**: The prompt is sent to the Mistral AI API, which processes the request and returns professionally written text content.
4.  **PDF Generation**: The returned text is cleaned for `FPDF` compatibility and parsed to create a structured and visually appealing PDF document.
5.  **Download**: A download button appears, allowing the user to save the generated PDF file directly to their local machine.

## 🚀 Setup and Installation

Follow these steps to run the application on your local machine.

### Prerequisites

-   Python 3.8 or higher
-   A Mistral AI API Key. You can get one from the [Mistral AI Platform](https://console.mistral.ai/).

### 1. Clone the Repository (or Create Files)

You can clone a repository or simply create the files yourself.

Create a project folder and inside it, create two files:
- `app.py` (for the Python code)
- `requirements.txt`

### 2. Create `requirements.txt`

Paste the following content into your `requirements.txt` file:

```txt
streamlit
requests
fpdf
```

### 3. Create a Virtual Environment & Install

It's highly recommended to use a virtual environment.

```bash
# Navigate to your project folder in the terminal
cd path/to/your/project

# For macOS/Linux
python3 -m venv venv
source venv/bin/activate

# For Windows
python -m venv venv
.\venv\Scripts\activate

# Install the required packages
pip install -r requirements.txt
```

### 4. Configure API Key

Open the `app.py` file and replace the placeholder with your actual Mistral AI API key.

```python
# Find this line in app.py
MISTRAL_API_KEY = "USE YOUR API KEY HERE"

# Replace it with your key
MISTRAL_API_KEY = "your_actual_mistral_api_key_goes_here"
```

**⚠️ Important**: Do not commit your API key to a public repository. If you plan to deploy this project, use environment variables or Streamlit's secrets management.

## ▶️ How to Run

Once the setup is complete, run the application with a single command from your terminal:

```bash
streamlit run app.py
```

Your web browser should automatically open to the application's local URL (usually `http://localhost:8501`).

## 🛠️ Technologies Used

-   **Backend**: Python
-   **Web Framework**: Streamlit
-   **AI Model**: Mistral AI (`mistral-medium`)
-   **API Communication**: `requests`
-   **PDF Generation**: `fpdf` (`pyfpdf`)
