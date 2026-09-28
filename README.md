# Final Project: Emotion Detection

A Flask-based web application that analyzes text input and detects the underlying emotional tone. The application identifies five core emotions—anger, disgust, fear, joy, and sadness—and determines which emotion is most dominant in the given text.

⚠️ **Note**: This application uses IBM Watson NLP services that are only accessible  from the IBM Skills Network Cloud IDE environment provided in the Coursera course.

## Features

- **Real-time emotion analysis**: Submit any text and receive instant emotion scores
- **Multi-emotion detection**: Analyzes text across five emotional dimensions
- **Dominant emotion identification**: Automatically highlights the strongest detected emotion
- **Web interface**: Clean, user-friendly UI for text input and results display
- **REST API**: Programmatic access via the `/emotionDetector` endpoint
- **Input validation**: Graceful handling of invalid or empty text submissions

## Tech Stack

- **Backend**: Python, Flask
- **Frontend**: HTML, JavaScript
- **NLP**: Watson NLP / Embedded AI for emotion analysis

## Project Structure

```
emotion-detector/
├── EmotionDetection/
│   ├── __init__.py
│   └── emotion_detection.py    # Core emotion detection logic
├── static/
│   └── mywebscript.js          # Frontend JavaScript
├── templates/
│   └── index.html              # Web interface template
├── server.py                   # Flask application entry point
├── test_emotion_detection.py   # Unit tests
├── LICENSE
└── README.md
```

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/JunaYdSheikh/emotion-detector.git
   cd emotion-detector
   ```

2. **Create and activate a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install flask requests
   ```

## Usage

### Running the Application

Start the Flask server:

```bash
python server.py
```

The application will be available at `http://localhost:5000`.

### Web Interface

1. Open your browser and navigate to `http://localhost:5000`
2. Enter the text you want to analyze in the input field
3. Click the analyze button to see the emotion breakdown

### API Endpoint

Send a GET request to the `/emotionDetector` endpoint:

```bash
curl "http://localhost:5000/emotionDetector?textToAnalyze=I%20am%20so%20happy%20today"
```

**Response format:**
```
For the given statement, the system response is 'anger': 0.01, 'disgust': 0.02, 
'fear': 0.01, 'joy': 0.95, 'sadness': 0.01. The dominant emotion is joy.
```

## Running Tests

Execute the unit test suite:

```bash
python -m unittest test_emotion_detection
```

## Emotions Detected

| Emotion | Description |
|---------|-------------|
| Anger | Frustration, irritation, or hostility |
| Disgust | Revulsion or strong disapproval |
| Fear | Anxiety, worry, or apprehension |
| Joy | Happiness, contentment, or excitement |
| Sadness | Sorrow, grief, or disappointment |

## Course Context

This project was developed as the final project for the **IBM AI Engineering Professional Certificate** on Coursera, specifically for the course on developing AI applications with Python and Flask.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Author

**Junaid Sheikh**  
- GitHub: [@JunaYdSheikh](https://github.com/JunaYdSheikh)


## Acknowledgments

- IBM Developer Skills Network for the course template and guidance
- Watson NLP for emotion detection capabilities
