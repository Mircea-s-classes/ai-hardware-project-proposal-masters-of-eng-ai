# Hardware Design

### Supportive Files
For the Hardware Design, the following files were with Arduino IDE:

- **Arduino_OV767X.zip** - Camera library for Arduino Nano 33 BLE Sense to communicate with the OV7675 camera module
- **nano33_tinyml_kit_image_serial.ino** - Arduino sketch that captures images from the camera and transmits them as base64-encoded data over serial
- **base64.h** - Header file for base64 encoding functionality
- **nano33_camera_live_inference.ino** - Arduino sketch for performing real-time interference with the deployed model


- **serial-image-capture.py** - Python serial that provides a GUI for capturing images from the Arduino camera via serial connection

- **ei-image-augmentation.ipynb** - Google Colab notebook for data augmentation and automatic upload to Edge Impulse