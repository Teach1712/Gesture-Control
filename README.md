# Hand Gesture Detection with MediaPipe and OpenCV

This project uses the latest MediaPipe Tasks API and OpenCV to detect hand gestures in real-time from your webcam.

## Features
- Detects hands and classifies gestures as "Open", "Closed Fist", or "Partial".
- Displays hand landmarks and gesture labels on the video feed.
- Uses the new MediaPipe `tasks` API (v0.10.32+).

## Requirements
- Python 3.10+
- OpenCV (`opencv-python`)
- MediaPipe (`mediapipe` v0.10.32+)

## Setup
1. Install dependencies:
   ```bash
   pip install opencv-python mediapipe
   ```
2. Download the hand landmarker model (already included if you followed the instructions):
   - [hand_landmarker.task](https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task)
   - Place it in the same directory as `main.py`.

## Usage
Run the script:
```bash
python main.py
```
- The webcam will open and start detecting hand gestures.
- Press `q` to quit.

## Notes
- If you get errors about the webcam, make sure no other application is using it.
- The code uses the new MediaPipe Tasks API. The old `mp.solutions.hands` API is not supported in recent versions.

## File Structure
- `main.py` - Main script for hand gesture detection
- `hand_landmarker.task` - Model file for hand detection
- `README.md` - This file

## References
- [MediaPipe Tasks Documentation](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker)
- [OpenCV Documentation](https://docs.opencv.org/)
