# PPE Detection Project

This project utilizes deep learning techniques to detect Personal Protective Equipment (PPE) worn by individuals in images or videos. The detection model is based on the YOLO (You Only Look Once) architecture and is implemented using the Ultralytics YOLO library. It can identify various PPE items such as hardhats, masks, safety vests, and more.

## Getting Started

To use this project, follow these steps:

1. Clone the repository to your local machine:

   ```
   git clone https://github.com/yourusername/ppe-detection.git
   ```

2. Install the required dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Run the detection script:

   ```
   python ppe_detection.py
   ```

## Usage

The detection script (`ppe_detection.py`) reads input from either an image file or a video file. It utilizes the YOLO model to detect PPE items in the input media and overlays bounding boxes and labels on the detected objects.

To run the script with a video file, update the `cap = cv2.VideoCapture("input.mp4")` line with the path to your video file.

## Example

Here's an example usage of the detection script:

```python
from ultralytics import YOLO
import cv2

# Load YOLO model
model = YOLO("best.pt")

# Open video file
cap = cv2.VideoCapture("input.mp4")

# Perform PPE detection
while True:
    success, img = cap.read()
    results = model(img, stream=True)
    # Process detection results and display annotated image
    # (Code for processing results is omitted for brevity)
    cv2.imshow("Image", img)
    cv2.waitKey(1)
```

## Contributing

Contributions to this project are welcome! If you have any ideas for improvements or encounter any issues, please feel free to open an issue or submit a pull request.
