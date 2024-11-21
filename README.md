# Autonomous Vehicle Project 🚗🤖

## Overview
This project involves building an autonomous vehicle prototype using **Raspberry Pi**, **Computer Vision**, and **Machine Learning**. The primary goal is to detect lanes and steer the vehicle autonomously based on live video input. The project is divided into three main steps: **Data Collection**, **Training**, and **Implementation**.

---

## Components 🧰

- **Raspberry Pi 4 Model B**  
- **Pi Camera**: To capture the road images.  
- **Motor Driver Module**: For controlling the car’s wheels.  
- **DC Motors**: To drive the car’s movement.  
- **Battery Pack**  
- **SD Card**: With Raspberry Pi OS installed.  
- **USB Power Bank**: For powering the Raspberry Pi.  
- **Jumper Wires**  

---

## Setup ⚙️

### Step 1: Set Up the Raspberry Pi
1. Install the Raspberry Pi OS on an SD card.
2. Boot up the Raspberry Pi and set up the system (enable SSH, camera, and GPIO).
3. Connect the Pi Camera to the CSI port on the Raspberry Pi.

### Step 2: Install Required Libraries
Open a terminal and enter the following commands to set up the environment:
```bash
python -m venv myenv
source myenv/bin/activate
pip install -r requirements.txt


## Project Workflow 🛠️

### Step 1: Data Collection
In this phase, we collect data required to train the machine learning model:
- **Inputs:**
  - **Joystick:** Used to manually steer the vehicle and collect control commands.
  - **Webcam:** Captures live video footage of the road.
  - **Motor:** Captures real-time movement data.
- **Outputs:**
  - **Images Folder:** Stores images captured by the webcam.
  - **Log File:** Logs the corresponding steering angles and motor states for each image.

---

### Step 2: Training
This phase focuses on training the machine learning model:
- **Inputs:**
  - **Images folder** (collected road footage).
  - **Log file** (steering angles and movement data).
- **Process:**
  - The data is fed into a **Convolutional Neural Network (CNN)** for training.
- **Output:**
  - A trained model (`model.h`) that predicts steering angles based on input images.

---

### Step 3: Implementation
In the final phase, the trained model is deployed for real-time lane detection:
- **Inputs:**
  - **Webcam:** Provides live road footage.
  - **Trained model (`model.h`).**
- **Process:**
  - The model predicts the appropriate steering angle.
- **Output:**
  - Commands sent to the motor for autonomous vehicle control.

---
