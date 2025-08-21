# AI Snippet Agent

The AI Snippet Agent is a desktop application that processes URLs (web pages and PDFs), extracts their content, generates AI-powered summaries and SEO keywords, and then saves the processed information into a Microsoft Word document.

## Features

*   **URL Processing:** Handles both standard web pages and PDF documents.
*   **Content Extraction:** Extracts titles and main content from web pages and text from PDFs.
*   **AI-Powered Summarization:** Generates concise summaries of the extracted content.
*   **AI-Powered SEO Keyword Generation:** Identifies relevant SEO keywords for the content's title.
*   **AI-Powered Summary Rewriting:** Rewrites summaries to naturally incorporate generated SEO keywords.
*   **Word Document Output:** Saves all processed data, including URLs, titles, SEO keywords, and final summaries, into a `.docx` file.
*   **Graphical User Interface (GUI):** Built with PyQt6 for an intuitive user experience.

## Prerequisites

Before running the application, ensure you have the following installed:

*   Python 3.x
*   Required Python libraries: `requests`, `beautifulsoup4`, `PyPDF2`, `python-docx`, `PyQt6`, `google-generativeai`
*   A Google Gemini API Key

## Installation

1.  **Clone the repository (if applicable) or download the project files.**

2.  **Install the required Python packages:**

    ```bash
    pip install requests beautifulsoup4 PyPDF2 python-docx PyQt6 google-generativeai
    ```

## Google Gemini API Key Setup

The application uses the Google Gemini API for AI functionalities (SEO keyword generation and summary rewriting). You need to provide your API key.

There are two ways to set up your API key:

1.  **Environment Variable (Recommended):**
    Set the `GEMINI_API_KEY` environment variable to your actual Gemini API key.

    *   **For Windows:**
        ```bash
        set GEMINI_API_KEY="YOUR_API_KEY"
        ```
    *   **For macOS/Linux:**
        ```bash
        export GEMINI_API_KEY="YOUR_API_KEY"
        ```
    Replace `"YOUR_API_KEY"` with your actual key.

2.  **`api_key.py` file:**
    Create a file named `api_key.py` in the same directory as `frontend.py` and `agent.py`. Add the following line to it:

    ```python
    GEMINI_API_KEY = "YOUR_API_KEY"
    ```
    Replace `"YOUR_API_KEY"` with your actual key.

## Usage

1.  **Run the frontend application:**

    ```bash
    python frontend.py
    ```

2.  **Enter URLs:** In the application window, enter a list of URLs, one per line, into the provided text area.

3.  **Start Processing:** Click the "Start Processing" button. The application will then fetch content, generate AI snippets, and update the progress bar and log display.

4.  **View Output:** Once processing is complete, a message box will confirm that the snippets have been saved to `Generated_Snippets.docx` in the project directory.
