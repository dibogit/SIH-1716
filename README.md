---

# Indian Sign Language (ISL) Detection Web Application

This project is a web-based application that translates Indian Sign Language (ISL) gestures into text and speech in real-time. It aims to bridge the communication gap between the hearing population and the deaf or hard-of-hearing community. The application is built using HTML, CSS, JavaScript for the frontend, and Flask (Python) for the backend. It leverages machine learning models for gesture recognition and conversion to text and speech.

## Table of Contents
- [Project Structure](#project-structure)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Technologies Used](#technologies-used)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

```
├── app.py                   # Main Flask app file
├── /templates
│   └── index.html            # Frontend HTML page
├── /static
│   ├── /css
│   │   └── styles.css        # Stylesheet for the web app
│   └── /js
│       └── script.js         # JavaScript file for frontend logic
├── ISL_classifier.ipynb      # Jupyter notebook for model training and testing
├── dataset_key_point_generation.py  # Script for generating keypoints from ISL dataset
├── isl_detection.py          # Script for gesture recognition
├── keypoint.csv              # CSV file containing keypoints data
├── model.h5                  # Pre-trained model for ISL detection
├── requirements.txt          # Python dependencies
├── .gitignore                # Files and directories to ignore in Git
└── README.md                 # Project documentation
```

## Features
- **Real-Time ISL Gesture Recognition**: Detects hand gestures using a pre-trained model.
- **Text and Speech Output**: Converts ISL gestures to corresponding text and speech for seamless communication.
- **Responsive UI**: A user-friendly web interface to interact with the system.
  
## Installation

### Prerequisites
Ensure you have the following installed on your system:
- Python 3.x
- Flask
- TensorFlow or PyTorch
- MySQL/PostgreSQL (if using a database)
- OpenCV
- MediaPipe
- Docker (optional, for containerization)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/dibogit/SIH-1716.git
   cd SIH-1716
   ```

2. Create a virtual environment and activate it:
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # For Linux/Mac
   venv\Scripts\activate      # For Windows
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the application:
   ```bash
   python app.py
   ```

5. Open your browser and go to `http://localhost:5000`.

## Usage
- Upload your hand gesture image or enable your webcam for live gesture recognition.
- The system will recognize the ISL gesture and display the corresponding text, along with an option to convert it into speech.

## Model Details
- The `model.h5` file contains the pre-trained model used for recognizing ISL gestures.
- The model was trained on a dataset of Indian Sign Language keypoints, generated using MediaPipe and OpenCV.
- For more details on the training process, refer to the `ISL_classifier.ipynb` notebook.

## Technologies Used
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Flask (Python)
- **Machine Learning**: TensorFlow, Keras, MediaPipe, OpenCV
- **Database**: MySQL/PostgreSQL (optional)
- **Real-time Communication**: WebSockets
- **Deployment**: Docker, AWS/Google Cloud

## Future Enhancements
- **Mobile App Integration**: Extend the functionality to Android using React Native or Flutter.
- **Multi-Language Support**: Provide translation for multiple languages.
- **Improved Gesture Recognition**: Incorporate more gestures to expand vocabulary.

## Contributing
Contributions are welcome! Please fork this repository, create a new branch, and submit a pull request.

---
