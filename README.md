# YouTube Video Summarizer

A Django web application that generates concise summaries of YouTube videos using Natural Language Processing (NLP). The application extracts the transcript from YouTube videos and creates a summary highlighting the key points.

## Features

- Clean, minimalist user interface
- YouTube video transcript extraction
- Automatic text summarization using spaCy NLP
- Responsive design that works on both desktop and mobile devices
- Error handling for invalid YouTube URLs

## Prerequisites

- Python 3.x
- Django 4.1.7
- spaCy with English language model
- youtube-transcript-api

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd <project-directory>
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the required packages:
```bash
pip install -r requirements.txt
```

4. Download the spaCy English language model:
```bash
python -m spacy download en_core_web_sm
```

5. Run migrations:
```bash
python manage.py migrate
```

6. Start the development server:
```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`

## Usage

1. Visit the application's homepage
2. Enter a valid YouTube video URL in the input field
3. Click the "Submit" button
4. The application will display a summary of the video content

## Technical Details

- The application uses the `youtube-transcript-api` to extract video transcripts
- Text processing and summarization is performed using spaCy's NLP capabilities
- The summary is generated using extractive summarization techniques
- The frontend is built with HTML and CSS, featuring a responsive design

## Project Structure

```
s8project/
├── home/                   # Main application directory
│   ├── utils.py           # Contains transcript and summarization logic
│   ├── views.py           # View functions
│   └── urls.py            # URL routing
├── templates/             # HTML templates
│   └── index.html         # Main page template
├── s8project/             # Project configuration
│   ├── settings.py        # Django settings
│   └── urls.py            # Project URL configuration
├── manage.py              # Django management script
└── requirements.txt       # Project dependencies
```

## Security Notes

- For production deployment, make sure to:
  - Set `DEBUG = False` in settings.py
  - Update `SECRET_KEY` with a secure value
  - Configure `ALLOWED_HOSTS`
  - Set up proper security middleware

## Known Limitations

- Only works with YouTube videos that have available transcripts
- Summary quality depends on the video transcript quality
- Currently only supports English language videos

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

[Add your chosen license here]
