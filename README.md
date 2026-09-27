# Fire and Smoke Detection with Automated Fire Suppression

> **Portfolio Showcase**  
> This repository documents the system without distributing its application source, trained model files, datasets, device configuration, or control implementation.

## Overview

A real-time **AI-assisted fire detection and automated suppression prototype** combining computer vision, thermal validation, embedded control, and a motorized suppression mechanism.

Rather than relying on a single sensor, the system uses an RGB/IP camera for visual detection and thermal imaging to validate and localize the heat source before directing the suppression mechanism.

## Project Images

<p align="center">
  <img width="284" alt="Fire suppression prototype" src="https://github.com/user-attachments/assets/dc90c2d6-4075-48e1-b61f-c53a3a32698d">
  <img width="233" alt="Fire suppression hardware" src="https://github.com/user-attachments/assets/caf49a6b-ae2a-4da6-8e14-5b6aa6ddd13e">
  <img width="299" alt="Fire detection prototype" src="https://github.com/user-attachments/assets/da64bb2b-98a9-44d3-b03b-54b3775ebdc7">
  <img width="217" alt="Suppression system" src="https://github.com/user-attachments/assets/1e90d8de-8241-4fa4-888c-7b74a4e6fcfa">
</p>

## System Workflow

```text
RTSP / IP Camera
       ↓
YOLO Fire Detection
       ↓
Thermal Validation
       ↓
Heat-Source Localization
       ↓
Turret Tracking
       ↓
Target Alignment
       ↓
Automated Suppression
       ↓
Monitoring Reset
```

The controller operates through three primary states:

1. **Monitoring** — computer vision continuously evaluates the camera feed.
2. **Tracking** — thermal imaging validates and localizes the detected heat source.
3. **Suppressing** — the motorized system aligns with the target and activates suppression.

## Core Capabilities

- Real-time fire/smoke detection using YOLO
- RTSP/IP-camera monitoring
- Thermal validation and heat-source tracking
- Adaptive thermal thresholding and contour filtering
- Motorized turret tracking
- Dead-zone target alignment
- Automated suppression activation
- Emergency-stop behavior
- Automatic return to monitoring

## Technology

**AI:** YOLOv11  
**Computer Vision:** OpenCV  
**Thermal Imaging:** FLIR Lepton  
**Edge Platform:** Raspberry Pi 5  
**Camera:** IP/RTSP CCTV camera  
**Hardware Control:** Arduino  
**Application:** Python, PyTorch, NumPy, serial communication

## Evaluation

Project testing recorded an **average response time of approximately 21.28 seconds** and a **91.7% suppression success rate** under the project's test conditions.

These values describe prototype testing and should not be interpreted as certification for production fire-safety use.

## Engineering Contribution

The project required integration across several engineering domains:

- Machine-learning inference
- RGB and thermal computer vision
- Real-time video processing
- Embedded communication
- Motor and servo control
- Automated state management
- Physical prototype integration and testing

The main challenge was coordinating these components into one autonomous detection-to-suppression pipeline.

## Repository Notice

This is a **showcase-only repository**. Source code, trained weights, datasets, credentials, hardware-specific configuration, and detailed control implementation are intentionally excluded.

The system is an academic engineering prototype and is not presented as a certified commercial fire-protection system.
