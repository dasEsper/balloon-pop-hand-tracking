# Balloon Pop: Real-Time Hand Tracking Game

Balloon Pop is a webcam-based interactive game built with Python. The game uses real-time hand tracking to detect the player's index finger and allows the player to pop moving balloons by touching them on the screen.

This project was originally developed in 2022 as a personal learning project to explore Python, computer vision, hand tracking, and game development.

## Project Overview

The main idea of this project is to combine a live webcam feed with a simple game mechanic. The player sees themselves on screen through the webcam, while a balloon moves upward. When the player touches the balloon using their detected index finger, the balloon pops, the score increases, and the balloon resets to a new position.

The game includes:

* Real-time webcam input
* Hand detection
* Index finger landmark tracking
* Collision detection between fingertip and balloon
* Score system
* Countdown timer
* Increasing difficulty as the game progresses

## Demo

Add demo video or GIF here:

```markdown
![Demo](demo/demo.gif)
```

or

```markdown
[Watch demo video](demo/demo.mp4)
```

## Tools and Libraries

This project uses:

* Python
* Pygame
* OpenCV
* NumPy
* cvzone
* MediaPipe Hands

## How It Works

The game uses OpenCV to capture frames from the webcam. The webcam frame is then converted and displayed inside a Pygame window.

Hand tracking is performed using `cvzone.HandTrackingModule`, which detects hand landmarks in real time. The game uses the landmark of the index finger tip as the interaction point. When the index finger touches the balloon area, the game detects the collision, increases the score, and resets the balloon position.

The balloon continuously moves upward. If it reaches the top of the screen without being popped, it resets to the bottom and the speed increases.

## Main Features

### 1. Webcam-Based Interaction

The game captures real-time webcam input and displays it as the background of the game window.

### 2. Hand and Finger Detection

The player's hand is detected using hand tracking. The index finger tip is used as the main input point.

### 3. Balloon Collision Detection

The balloon is represented as a Pygame rectangle. When the detected index finger touches the balloon rectangle, the game counts it as a successful pop.

### 4. Score and Timer

The player earns points by popping balloons. The game runs for a limited time and displays the final score when the time is over.

### 5. Increasing Difficulty

The balloon speed increases as the game continues, making the game more challenging over time.

## Installation

Clone this repository:

```bash
git clone https://github.com/your-username/balloon-pop-hand-tracking.git
cd balloon-pop-hand-tracking
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

## Requirements

The project requires the following Python libraries:

```txt
pygame
opencv-python
numpy
cvzone
mediapipe
```

## How to Run

Run the main Python file:

```bash
python balloon_pop.py
```

Make sure your webcam is connected and accessible.

## Project Structure

```text
balloon-pop-hand-tracking/
│
├── balloon_pop.py
├── requirements.txt
├── README.md
├── demo/
│   └── demo.mkv
├── assets/
│   ├── BalloonRed.png
│   └── Marcellus-Regular.ttf
└── .gitignore
```

## Notes

This project was created as a learning project. The original version used local file paths for image and font assets, so some paths may need to be adjusted depending on the folder structure.

## Ethical and Privacy Note

This project does not store webcam recordings or personal data. Webcam input is processed locally during gameplay and is only used for real-time interaction.

## Status

Archived learning project, uploaded as part of my technical portfolio.

## What I Learned

Through this project, I learned how to:

* Build a basic game loop using Pygame
* Integrate OpenCV webcam input into a Pygame window
* Use hand tracking for real-time interaction
* Work with image assets and object movement
* Apply collision detection in a game environment
* Combine computer vision with interactive game mechanics

## Author

Auzan Rama Satria
GitHub: [your GitHub profile link]
LinkedIn: [your LinkedIn profile link]
