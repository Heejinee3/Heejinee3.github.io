---
index: 7 # labs number
num: 1 # lab number
permalink: /lab/Robocam/Light-Control # link
category: lab # project or lab
---

#### **Purpose**

---

The purpose of this lab is to control two lights for illumination: hardwired LED lights using GPIO hardware and software of command lines, shell script, C program, and device driver module.

<br>

#### **Problem Statement**

---

- Light Control

  Implement an illumination light controller with two white LEDs with Beaglebone: Wire two LEDs using GPIO and transistor array, and drive these using commands with sys file system (sysfs), shell script, C program, and device driver module.

  We start from the simplest and perform step-by-step improvements.

1. Light Control Commands with sysfs

   ```
   Wire two LEDs using GPIO and transistor array.
   Test commands with sysfs to control the user LED0 on Bone, and then test commands with sysfs for two hard-wired LED lights.
   ```

2. Light Control Shell Script

   ```
   Control two hard-wired LED lights using shell script.
   ```

3. Light Control C Program

   ```
   Control two hard-wired LED lights using C program.
   ```

4. Test Example Device Driver Program

   ```
   Test an example device driver using Linux module.
   ```

5. Light Control Application and Module

   ```
   Control two hard-wired LED lights using application program and device driver module for lights control.
   ```

<br>

#### **Link**

---

[Github](https://github.com/Heejinee3/Robocam/tree/master/Light%20Control)

<br>

#### **Glossary**

---

[GPIO](https://velog.io/@chunjakim/GPIOGeneral-Purpose-InputOutput)

[sysfs](https://velog.io/@chunjakim/sysfs-sys-File-System)
