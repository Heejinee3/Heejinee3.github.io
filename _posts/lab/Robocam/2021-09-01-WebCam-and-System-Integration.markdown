---
index: 7 # labs number
num: 4 # lab number
permalink: /lab/Robocam/WebCam-and-System-Integration # link
category: lab # project or lab
---

#### **Purpose**

---

The purpose of this lab is to design and implement a remote video viewer using off-the-shelf WebCam, and perform system integration of RoboCam.

<br>

#### **Problem Statement**

---

- WebCam and System integration

  Implement Video functionality. Also perform system integration of Video and control functionalities.

  We start from the simplest and perform step-by-step improvements.

1. Test Capture WebCam on Beaglebone

   ```
   Test capture image from WebCam with V4L2 (Video for Linux 2) on Beaglebone.
   ```

2. Learn SDL2 via Tutorials

   ```
   Learn SDL 2 (Simple DirectMedia Layer 2) via Tutorials.
   ```

3. Implement Video functionality

   ```
   Implement Video functionality composed of
   ● Camera on Beaglebone (Capture from WebCam and send video to network) and
   ● Viewer on PC (Receive video from network and display video to user) using SDL2.
   ```

4. System Integration

   ```
   Perform system integration of Video and control functionalities:

   A. Video functionality composed of
   ● Camera on Beaglebone (Capture from WebCam and send video to network) and
   ● Viewer on PC (Receive video from network and display video to user).

   B. Control functionality composed of
   ● Commander on PC (Get key input from user and send command packet to network) and
   ● Controller on Beaglebone (Receive command packet from network and actuate servos and lights on the robot).

   For recording photos and videos, Commander on PC sends user command to Viewer, which records photos and videos to storage device.
   Data Flow is summarized as follows:

   User      PC                 Network   Beaglebone   Robot
   Eye     ← Viewer           ← Video   ← Camera     ← WebCam
   Storage ← (Record command)
   Finger  → Commander        → Command → Controller → Servos & Lights
   ```

<br>

#### **Link**

---

[Github](https://github.com/Heejinee3/Robocam/tree/master/WebCam%20and%20System%20Integration)

<br>

#### **Glossary**

---

[SDL](https://velog.io/@chunjakim/SDL-Simple-DirectMedia-Layer)
