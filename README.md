# AI Green Tips Web Application

AI Green Tips is a Flask-based web application that provides environmentally friendly advice using the Google Generative Language API (Gemini-Pro). Users can enter a topic or question related to environmental conservation, and the app generates detailed eco-friendly tips. Safety filters ensure content is appropriate before displaying results.

---

## Overview

The application runs a Flask server that:

* Serves a clean, styled web interface
* Accepts user input related to environmental topics
* Sends requests to the Gemini-Pro API for AI-generated responses
* Displays detailed “Green Tips” on a results page
* Performs safety evaluation and error handling

A default helper text is prepended to user input to guide the AI toward generating environmental content.

---

## Features

* Web interface for entering environmental questions or topics
* AI-generated eco tips using Gemini-Pro
* Safety rating checks to filter unsafe output
* Displays generated content in a styled scrollable container
* Error handling for invalid input or failed API responses
* Responsive UI with custom CSS design

---

## Tech Stack

* **Backend:** Python, Flask
* **HTTP Client:** Requests
* **Frontend:** HTML, CSS
* **API:** Google Generative Language API (Gemini-Pro)
* **Logging:** Python logging module

---

## Project Structure

```
AI-Green-Tips-main/
│
├── app.py                     # Flask app and AI logic
├── requirements.txt           # Dependencies
│
├── static/
│   └── styles.css             # Global styling
│
└── templates/
    ├── index.html             # Input page
    └── result.html            # Result display page
```

---

## Installation

1. Ensure Python is installed.
2. Extract the project folder.
3. Open a terminal in the project directory.
4. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Configuration

The application requires a valid Gemini-Pro API key.

Open `app.py` and update:

```python
API_ENDPOINT = "https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=API_Key"
```

Replace `API_Key` with your actual Google Generative Language API key.

Internet access is required for API calls.

---

## Running the Application

Start the Flask server:

```bash
python app.py
```

The app runs in debug mode.
Open your browser and visit:

```
http://127.0.0.1:5000
```

---

## Usage

1. Open the web application.
2. Enter an environmental question or topic in the input field.
3. Click **Detect**.
4. If the response passes safety checks, detailed environmental tips are displayed.
5. If something goes wrong, an appropriate error message is shown.

---

## Notes

* Safety ratings are checked, and responses with a “HIGH” probability risk are rejected.
* The application logs useful debug details to the console.
* Internet connectivity is required.

---

## License

No license file is included in this project.
