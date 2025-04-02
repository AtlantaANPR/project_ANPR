# project_ANPR

# This is Automatic Number Plate Recognition.


# License Plate Recognition Pipeline

This document outlines the workflow for Automated Number Plate Recognition (ANPR) using YOLO for detection and EasyOCR (or a custom OCR model) for recognition.

## Workflow

### Detection
1. **ANPR Camera** - Captures images or video frames.
2. **Image/Video Capture** - Acquires frames from the camera.
3. **Pre-Processing** - Enhances image quality.
4. **License Plate Detection (Using YOLO models)** - Identifies and localizes the license plate.
5. **License Plate Cropping** - Extracts the detected license plate from the image.

### Recognition
6. **Image Processing** - 
   - Convert image to 255 scale
   - Convert to grayscale
   - Apply blurring, thresholding, and dilation
7. **Character Segmentation** - Determines contours of license plate characters.
8. **Character Recognition** - Uses EasyOCR or a custom OCR model to recognize characters.
9. **Post Processing** - Validates the recognized license plate text.
10. **Output** - Returns the recognized license plate number.
11. **API Endpoint** - Sends the output to an API for further processing.

This pipeline ensures accurate detection and recognition of license plates, enabling integration into various applications such as traffic monitoring, security systems, and automated toll collection.
