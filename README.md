# Pipeline Leak Detection Using YOLO11 and Vision Language Models

An AI-powered pipeline monitoring and leak detection system that combines real-time computer vision, severity estimation, risk scoring, and intelligent corrective guidance for oil and gas pipeline infrastructure.

This project integrates:

- YOLO11 for real-time leak detection
- Vision Language Models (Gemini 2.5 Flash) for intelligent analysis
- Severity estimation using bounding-box analysis
- Automated risk scoring
- AI-generated corrective recommendations
- Audio-based response generation

The system provides a scalable and low-cost alternative to traditional sensor-heavy monitoring systems for pipeline integrity management.

---

# Project Overview

Pipeline leakage presents a major operational, environmental, and safety challenge in the oil and gas industry. Undetected leaks can lead to:

- Environmental contamination
- Product loss
- Infrastructure damage
- Fire and explosion hazards
- Economic losses

Traditional leak detection methods such as:

- Pressure monitoring
- Flow imbalance analysis
- Sensor-based systems

often suffer from:

- High latency
- False alarms
- Expensive hardware integration
- Limited scalability

This project proposes an AI-driven visual monitoring framework capable of detecting leaks directly from image streams using deep learning and computer vision.

The proposed framework combines:

- Real-time visual leak detection
- Severity estimation
- Risk assessment
- Intelligent recommendation generation
- Audio and text feedback

to create an end-to-end intelligent pipeline monitoring solution.

---

# Live Demo

Try the deployed application on Hugging Face:

🚀 Demo: https://huggingface.co/spaces/Sgobir/pipeline_leak_detection2

---

# Key Features

## Real-Time Leak Detection

The system uses a trained YOLO11 object detection model to identify:

- Gas leaks
- Water leaks

from pipeline monitoring images and video streams.

---

## Severity Estimation

Detected leak regions are analyzed using:

- Bounding box dimensions
- Detection confidence
- Spatial characteristics

to estimate leak severity levels.

---

## Risk Scoring

The system automatically calculates operational risk scores based on:

- Leak size
- Detection confidence
- Severity level
- Leak category

Risk categories may include:

- Low Risk
- Medium Risk
- High Risk
- Critical Risk

---

## AI-Powered Corrective Guidance

A Vision Language Model (Gemini 2.5 Flash) analyzes detected leak scenarios and generates:

- Structured recommendations
- Corrective actions
- Safety guidance
- Maintenance suggestions
- Emergency response instructions

The recommendations are professionally formatted for operational use.

---

## Audio Response Generation

The system can convert generated recommendations into audio output for:

- Field operators
- Remote monitoring stations
- Accessibility support
- Hands-free operational environments

---

# System Architecture

```text
Pipeline Image/Video
          ↓
YOLO11 Leak Detection
          ↓
Leak Localization
          ↓
Severity Estimation
          ↓
Risk Scoring
          ↓
Vision Language Model Analysis
          ↓
Corrective Recommendations
          ↓
Text + Audio Response
```

---

# Dataset Information

The dataset used for training was sourced from Roboflow under the CC BY 4.0 License.

Dataset Source:
https://universe.roboflow.com/gas-leak/pipeline-leak-prediction

---

## Dataset Summary

| Category | Value |
|---|---|
| Total Images | 3,586 |
| Training Images | 3,453 |
| Validation Images | 49 |
| Test Images | 84 |
| Classes | Gas Leak, Water Leak |

---

# Model Training

## Training Configuration

| Parameter | Value |
|---|---|
| Framework | Ultralytics YOLO11 |
| Epochs | 20 |
| Image Size | 640 × 640 |
| Optimizer | SGD |
| Batch Size | Auto-configured |

---

## Hardware

| Component | Specification |
|---|---|
| GPU Memory | 20GB |
| Training Time | ~1.5 min/epoch |

---

# Model Performance

| Metric | Score |
|---|---|
| Precision | 81.6% |
| Recall | 79.4% |
| mAP@50 | 88.2% |
| mAP@50-95 | 71.7% |

The model demonstrates strong detection capability suitable for practical deployment scenarios.

---

# Technologies Used

## Programming Language

- Python

---

## Computer Vision & Deep Learning

- Ultralytics YOLO11
- PyTorch
- OpenCV

---

## AI & Language Models

- Gemini 2.5 Flash
- Vision Language Models (VLMs)

---

## Deployment & Interface

- Hugging Face Spaces
- Gradio

---

# Repository Structure

```bash
pipeline-leak-detection/
│
├── models/                  # Trained YOLO weights
├── dataset/                 # Dataset files
├── results/                 # Detection outputs
├── app.py                   # Deployment application
├── requirements.txt         # Dependencies
├── README.md                # Documentation
└── notebooks/               # Experiment notebooks
```

---

# Installation

## Clone the Repository

```bash
git clone https://github.com/yourusername/pipeline-leak-detection.git
```

Move into the project directory:

```bash
cd pipeline-leak-detection
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Usage

## Training the Model

```bash
yolo train model=yolo11n.pt data=pipeline_leak.yaml epochs=20 imgsz=640
```

---

## Model Validation

```bash
yolo val model=best.pt data=pipeline_leak.yaml
```

---

## Inference on Images or Videos

```bash
yolo detect model=best.pt source=your_image_or_video.mp4
```

---

# Research Contribution

This work contributes to intelligent pipeline monitoring by integrating:

- Real-time computer vision
- AI-based risk assessment
- Vision-language reasoning
- Automated decision support

Unlike traditional leak monitoring systems that rely heavily on physical sensors, this framework demonstrates the feasibility of scalable visual AI systems for industrial monitoring applications.

The proposed system establishes a foundation for:

- Smart pipeline infrastructure
- AI-assisted industrial safety systems
- Intelligent digital oilfield operations
- Automated maintenance support systems

---

# Experimental Evaluation

Experimental results demonstrate that the proposed framework:

- Accurately detects pipeline leaks
- Provides practical operational guidance
- Supports real-time deployment
- Reduces dependence on expensive sensing infrastructure

The integration of Vision Language Models further enhances interpretability and operational usefulness beyond conventional object detection systems.

---

# Future Improvements

Potential future developments include:

- Thermal imaging integration
- Drone-based pipeline inspection
- Edge AI deployment
- Real-time video analytics
- Multi-modal sensor fusion
- Explainable AI for industrial safety
- Autonomous emergency response systems
- IoT integration for smart monitoring

---

# Example Applications

This system can be applied in:

- Oil and gas pipeline monitoring
- Industrial plant safety
- Environmental monitoring
- Smart infrastructure systems
- Refinery monitoring
- Remote field surveillance
- AI-assisted maintenance operations

---

# Author

## Sunusi Muhammad Ibrahim

Petroleum Engineer | AI Researcher | Computer Vision Developer

### Research Interests

- Computer Vision
- Vision Language Models (VLMs)
- Multimodal AI
- AI for Energy Systems
- Deep Learning
- Industrial AI
- Intelligent Monitoring Systems

GitHub: https://github.com/MSunusi

---

# Citation

If you use this project in your research or academic work, kindly cite:

```bibtex
@misc{sunusi_pipeline_leak_detection,
  author       = {Sunusi Muhammad Ibrahim},
  title        = {Pipeline Leak Detection Using YOLO11 and Vision Language Models},
  year         = {2026},
  publisher    = {GitHub},
  journal      = {GitHub Repository},
  howpublished = {\url{https://github.com/yourusername/pipeline-leak-detection}}
}
```

---

# Dataset Citation

```text
Pipeline-leak-prediction > 2023-10-15 2:31pm
https://universe.roboflow.com/gas-leak/pipeline-leak-prediction
Provided by a Roboflow user
License: CC BY 4.0
```

---

# Acknowledgements

Special thanks to:

- Roboflow for providing the dataset
- Ultralytics for the YOLO framework
- Hugging Face for deployment infrastructure
- Google Gemini for Vision Language Model capabilities
- The open-source AI community

---

# License

This project is licensed under the MIT License.
