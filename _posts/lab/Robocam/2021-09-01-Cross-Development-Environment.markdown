---
index: 7 # labs number
num: 0 # lab number
permalink: /lab/Robocam/Cross-Development-Environment # link
category: lab # project or lab
---

#### **Purpose**

---

Suitable Linux software cross development system based on a PC will be constructed and tested. This cross development system will be used for developing a specific embedded system. We test various aspects: PC Ubuntu on PC, Debian on Beaglebone, cross-compile, NFS, module build, and reaction time measurement application.

<br>

#### **Problem Statement**

---

- Cross Development Environment and an Application

  Construct a cross-development system on a PC for application and module programs development, and implement a reaction timer application program.
  We start from the simplest and perform step-by-step improvements.

1.  An Example of Embedded Application Program

    ```
    Construct a cross-development system on a Lab PC (or your own notebook PC).
    Edit and cross compile an example embedded application program.
    Download to the embedded system or use NFS, and then run.
    ```

2.  An Example of Embedded Module Program

    ```
    Construct a module program development environment on a PC.
    Edit and cross compile an example embedded module program.
    Download to the embedded system or use NFS, and then run.
    ```

3.  Design of Reaction Timer Application

    ```
    Implement a program which measures your response time from message display to key input.

    i. Computer displays a message at random time (2 to 5 s) with a lowercase alphabet ‘f’ or ‘j’ (random):

      “Type ‘f’ key without Enter: “ or
      “Type ‘j’ key without Enter: “

    ii. You type the designated key without Enter key as soon as possible.

    iii. Computer computes your reaction time from i to ii in ms, and compares the required key and the
      response key.

    iv. Computer reports:

      “Correct answer ‘f’ in ab.cde ms.” or
      “Wrong answer ‘j’ in ab.cde ms.”

    Of course, quotation marks do not appear on terminal.
    Test on PC to debug, and then run on Beaglebone.
    ```

<br>

#### **Link**

---

[Github](https://github.com/Heejinee3/Robocam/tree/master/Cross%20Development%20Environment)

<br>

#### **Glossary**

---

[Beaglebone Debian](https://velog.io/@chunjakim/Beaglebone-Debian)

[NFS](https://velog.io/@chunjakim/NFSNetwork-File-System)
