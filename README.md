# ESPCAM-HTTP-RTSP
Run a http or rtsp from a ESPCAM from scratch

<p align="center"><img src="https://raw.githubusercontent.com/procrastinando/ESPCAM-HTTP-RTSP/main/espcam.png" width="800"></p>

## 1. Setting up
Install the driver according the system, install arduino.
In arduino: file/preferences/additional boards Managerl URLSs: add ```https://dl.espressif.com/dl/package_esp32_index.json```
In Tools/Board/Boards manager find esp32 and install it.
Select Tools/ESP32 Arduino/AI thinker ESP32-CAM

## 2. Flash the board
Open 'ESPCAM.ino' and edit the row ```172``` with the resolution:

```
FRAMESIZE_UXGA (1600 x 1200)
FRAMESIZE_QVGA (320 x 240)
FRAMESIZE_CIF (352 x 288)
FRAMESIZE_VGA (640 x 480)
FRAMESIZE_SVGA (800 x 600)
FRAMESIZE_XGA (1024 x 768)
FRAMESIZE_SXGA (1280 x 1024)
```

Edit 'wifikeys.h' with the wifi credentials.

The http address is: http://<espcam_ip>/
The rtsp address is: rtsp://<espcam_ip>:8554/mjpeg/1/
