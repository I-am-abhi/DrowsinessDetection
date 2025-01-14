# Drowsiness Detection System

This project is a real-time drowsiness detection system designed to monitor signs of fatigue in individuals, particularly for applications like driver safety or workplace monitoring. It utilizes **OpenCV** for facial and eye detection, **TensorFlow** for machine learning-based analysis, and **Python** for implementation. An alarm sound is triggered when drowsiness is detected to alert the user.

## Table of Contents
- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [License](#license)
- [Contributing](#contributing)

## Overview
The drowsiness detection system continuously monitors the user's face, analyzing facial features like eye openness and head movements. When signs of drowsiness are detected, the system triggers an alarm sound to alert the user to take a break and improve safety.

## Technologies Used
- **Python**: Programming language used for implementing the system.
- **OpenCV**: Used for real-time computer vision tasks, including detecting faces and eyes.
- **TensorFlow**: Deep learning framework used for the detection model.
- **Haar Cascades**: OpenCV's pre-trained classifiers for detecting faces and eyes.
- **Alarm Sound**: A sound played through the system when drowsiness is detected (can be customized).

## Installation

To run this project on your local machine, follow these steps:

### Prerequisites
Make sure you have Python 3.x installed. You can download it from [python.org](https://www.python.org/).

### Step 1: Clone the repository
```bash
git clone https://github.com/yourusername/drowsiness-detection.git
cd drowsiness-detection
```

### Step 2: Install dependencies
Install the necessary Python packages using `pip`:
```bash
pip install -r requirements.txt
```

### Step 3: Download the required Haar Cascades
Ensure you have the pre-trained Haar Cascade files (`haarcascade_frontalface_default.xml` and `haarcascade_eye.xml`). You can download them from the [OpenCV GitHub repository](https://github.com/opencv/opencv/tree/master/data/haarcascades) and place them in the project directory.

### Step 4: Set up TensorFlow (if necessary)
If you're using TensorFlow models for further customization, ensure TensorFlow is installed:
```bash
pip install tensorflow
```

### Step 5: Download the alarm sound file
The system uses an alarm sound when drowsiness is detected. You can add a custom alarm sound or download a sample `.wav` file and place it in the project directory. You can find free sound files on sites like [freesound.org](https://freesound.org/).

## Usage

To run the drowsiness detection system, simply execute the main script:

```bash
python detect_drowsiness.py
```

The script will use your computer's webcam to monitor your face. When drowsiness is detected, an alarm sound will play, and a warning will be displayed on the screen.

### Configuration
You can adjust the sensitivity of the drowsiness detection by modifying the parameters in the script, such as:
- Eye aspect ratio threshold for detecting closed eyes
- The duration of eyelid closure before triggering the alarm

## How It Works
1. **Facial Detection**: The system uses OpenCV's Haar Cascade Classifiers to detect the face and eyes in real-time.
2. **Eye Detection & Blink Rate**: By monitoring the eye aspect ratio (EAR), the system determines if the user is blinking excessively or if their eyes are closed for an extended period.
3. **Machine Learning**: TensorFlow (if implemented) can be used to train a more complex model for detecting fatigue based on additional facial cues, such as yawning or head nodding.
4. **Alarm Trigger**: When drowsiness is detected (e.g., if the eyes are closed for too long), the system plays an alarm sound to alert the user.

### Example Output
- Webcam feed displaying a bounding box around the detected face.
- A message "Drowsiness Detected" will appear when the system identifies fatigue.
- An alarm sound will play to notify the user.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! If you find a bug or want to add a new feature, feel free to fork the repository and submit a pull request. Please make sure to write tests for any new functionality you add.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-name`).
6. Create a new pull request.

---

If you have any questions, feel free to open an issue in the repository!