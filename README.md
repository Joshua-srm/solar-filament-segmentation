# Solar Filament Detection and Instance Segmentation Using YOLO11n-seg

## Overview

This project applies deep learning to detect and segment solar filaments in H-alpha solar images. Solar filaments are elongated structures of relatively cool, dense plasma in the Sun's atmosphere. Studying their structure and evolution is relevant to solar physics and space-weather research.

The goal is to automate the identification of individual filaments and generate pixel-level segmentation masks.

## Problem Statement

Manually identifying and outlining solar filaments can be time-consuming. Their irregular shapes, varying sizes, and low contrast make automated segmentation challenging.

This project explores YOLO11n-seg as a deep-learning approach for detecting individual solar filaments and producing instance segmentation masks.

## Model

* **Architecture:** YOLO11n-seg
* **Task:** Instance segmentation
* **Framework:** Ultralytics
* **Training platform:** Kaggle
* **Training hardware:** NVIDIA Tesla T4 GPU
* **Training duration:** 25 epochs
* **Image size:** 1024 pixels
* **Batch size:** 4

## Dataset

The project uses the Solar Filament Segmentation Challenge 2026 dataset.

* 707 unique annotated training images
* 180 test images
* 600 training images
* 107 validation images
* 4,336 selected training instances
* 873 selected validation instances

The dataset annotations were processed and the physical images were divided into training and validation sets without image overlap.

## Evaluation

The model was evaluated using object-detection and instance-segmentation metrics, including:

* Precision
* Recall
* Mean Average Precision (mAP)
* Intersection over Union (IoU)
* Dice score
* Panoptic Quality (PQ), where calculated

Actual metric values and the evaluation procedure should be documented in the results section after verification.

## Repository Structure

* `notebooks/` — Training and experimentation
* `evaluation/` — Evaluation code and metrics
* `app/` — Optional interactive demonstration
* `models/` — Instructions for obtaining trained weights
* `results/` — Prediction samples and result visualizations

## Limitations

The model's performance depends on the quality and distribution of the training data. It may miss faint filaments, produce false detections, or generate imperfect boundaries.

This model segments solar filaments; it does not directly predict solar flares, coronal mass ejections, or future space-weather events.

## Future Improvements

* Experiment with alternative segmentation architectures.
* Improve small and faint filament detection.
* Perform systematic confidence-threshold tuning.
* Evaluate on additional unseen solar images.
* Improve inference speed and deployment.

## Reproducibility

The training notebook, evaluation code, dependency information, and available model weights or download instructions should be provided to help others reproduce the project.
