# Event Report Generator

## Overview

The Event Report Generator is a Django-based application that generates event reports in `.docx` format using OpenAI's GPT-2 model. This tool allows users to input event details and receive a formatted report as a downloadable `.docx` file.

## Features

- Generate detailed event reports with a preset template.
- Use GPT-2 to create event descriptions based on user prompts.
- Download the generated report as a `.docx` file.

## Requirements

- Python 3.7 or higher
- Django 3.2 or higher
- `transformers` library for model handling
- `huggingface_hub` library for Hugging Face login
- `python-docx` library for creating `.docx` files

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/event-report-generator.git
   cd event-report-generator
   ```

2. **Create a virtual environment and activate it:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up your Django project:**

   Make sure you have Django installed and configure the `settings.py` file as needed. Ensure you add `django.contrib.staticfiles` to your `INSTALLED_APPS` if not already present.

5. **Apply migrations:**

   ```bash
   python manage.py migrate
   ```

6. **Run the development server:**

   ```bash
   python manage.py runserver
   ```

## Usage

1. **Access the application:**

   Open your web browser and navigate to `http://127.0.0.1:8000/`.

2. **Generate a report:**

   - Go to the page where you can input event details.
   - Enter your event details in the provided form.
   - Click "Generate Report" to receive a `.docx` file with the event report.

## Configuration

To use the GPT-2 model from Hugging Face, you need to log in with your Hugging Face token. Replace the placeholder token in `views.py` with your own token:

```python
login(token="your_hugging_face_token_here")
```

## Project Structure

- `cems/` - Main Django project directory
  - `urls.py` - URL configurations
- `generate_report/` - Django app for report generation
  - `views.py` - Contains view functions for generating reports
  - `templates/` - HTML templates
    - `generate_report.html` - Form for generating reports
- `requirements.txt` - List of required Python packages

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Transformers](https://huggingface.co/transformers/) by Hugging Face
- [python-docx](https://python-docx.readthedocs.io/en/latest/) for creating `.docx` files


