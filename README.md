# WebCam2VirtualCam

- [WebCam2VirtualCam](#webcam2virtualcam)
- [Project Overview: WebCam-VirtualCam](#project-overview-webcam-virtualcam)
  - [Major Components:](#major-components)
    - [1. Webcam Transmission via HTML/JavaScript](#1-webcam-transmission-via-htmljavascript)
    - [2. Python Implementation](#2-python-implementation)
    - [3. Communication between Python and JavaScript](#3-communication-between-python-and-javascript)
    - [4. Virtual Camera Driver](#4-virtual-camera-driver)
    - [5. Driver Functionality Validation](#5-driver-functionality-validation)
    - [6. Integration of Web Client with Python and Virtual Camera](#6-integration-of-web-client-with-python-and-virtual-camera)


# Project Overview: WebCam-VirtualCam

## Major Components:

### 1. [Webcam Transmission via HTML/JavaScript](https://github.com/linuslau/WebCamJs)
This part establishes video transmission from one device to another using HTML/JavaScript and a Node.js-based signal server. It supports various combinations such as phone-to-phone, phone-to-PC, and PC-to-PC communication.

### 2. [Python Implementation](https://github.com/linuslau/WebCamPy)
Replaces HTML/JavaScript with Python for both the sending and receiving ends of the video transmission.

### 3. Communication between Python and JavaScript
In this phase, JavaScript handles the sending side, while Python manages the receiving side, ensuring seamless integration between the two languages.

### 4. [Virtual Camera Driver](https://github.com/linuslau/VirtualCamDriver)
The core functionality revolves around creating a virtual camera driver. This driver ensures a virtual device node appears in the device manager, enabling all camera-enabled applications (e.g., Teams, Skype) to use this virtual camera. The key difference from a traditional camera driver is that this driver sources data directly from the user rather than a physical camera.

### 5. [Driver Functionality Validation](https://github.com/linuslau/VirtualCamera)
A demonstration verifies that the virtual camera driver supports both image and video input. It confirms that any camera-enabled application can display the input content.

### 6. Integration of Web Client with Python and Virtual Camera
The final part integrates the video stream from a JavaScript-based web client, receives it through Python, and forwards the stream to the virtual camera driver. This enables any third-party app that uses a camera to access the video stream from the web client.
