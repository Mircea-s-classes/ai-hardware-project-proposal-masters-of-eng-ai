# University of Virginia

## Department of Electrical and Computer Engineering

---

# AI Hardware Project Proposal

## Project Title

TinyML: Waste Sorting Visual Classifier

#### [Presentation](https://docs.google.com/presentation/d/1ZxCNk8CfvOTLMQ2DKfZHajKMgD14Uccm1HQ3gBI3OfU/edit?usp=sharing)

## Team name

Masters of Eng-Ai

## Team members

  Martha Michael<br>
  Yatzil Romero Rodriguez<br>
  Meng Xu<br>

## 2. Platform Selection

**Selected Platform**: TinyML - Arduino Nano 33 BLE Sense with Camera Module

We selected the TinyML platform due to its capabilities of producing real-time, on-device machine learning using minimal power and memory resources. The Arduino Nano 33 BLE Sense has integrated sensors and BLE connectivity, and the camera module provides direct visual input for classification tasks without requiring external processors or cloud resources.  

We will use the Arduino TinyML Kit and Camera, programming in the Arduino IDE with Python. Model training and testing may utilize Google Colab for dataset preprocessing and optimization.  

## 3. Problem Definition

Traditional waste sorting systems are often ineffective, as many people struggle to distinguish between recycling, organics, and general waste. To address this issue, we aim to provide a more accessible solution for correctly disposing and separating waste. Our approach involves developing a low-latency, efficient visual waste sorting classifier capable of identifying and sorting materials into three main categories, trash, compost, and recycle such as plastic, metal, paper, non-recyclables, and discarded food.

Using a TinyML model and an onboard camera, we plan to build a real-time image classification system that operates directly on embedded hardware. The goal is to design and deploy a lightweight model that can accurately categorize waste relying on cloud based processing. This problem is highly relevant to AI hardware, as it tests the limits of efficiency and latency while demonstrating how AI can be both environmentally sustainable and hardware efficient for real-world edge applications.

## 4. Technical Objectives

• Classify waste with at least an accuracy of 75%, using unseen testing data.

• Inference latency of at most 1s, maintain real-time classification.

• Reduce power consumption via quantization of the trained model.

## 5. Methodology

Use the Arduino Nano 33 BLE Sense with the OV7670 VGA camera module. The camera captures images of waste items, and the Nano runs a TinyML model locally to classify them (paper, plastic, metal).

**Project Workflow**:

1. Collect and label waste images (Edge Impulse or TrashNet).
2. Train a small CNN model and optimize for TinyML deployment.
3. Quantize and upload the model to the Nano 33 BLE Sense.
4. Test real-time inference and measure accuracy and latency.
5. Refine model or dataset based on performance.

**Metrics**:
    Accuracy >= 75%
    Latency <= 1 s
    Model fits with device memory limits

**Validation**: Run live tests on different waste samples and record classification results for comparison with the test dataset.

## 6. Expected Deliverables

A TinyML system that is able to capture, identify, and categorize waste into the correct disposal bin using real-time waste detection, with at least 75% accuracy.
The final report and GitHub repository will contain detailed project documentation, presentation slides, measurable goals and objectives, and user guidance on how to interact with the Waste Sorting Visual Classifier system.

## 7. Team Responsibilities

| Name           | Role | Responsibilities |
|----------------|------|------------------|
| Martha Michael | Team Lead | Coordinate project timeline, manage documentation, integrate model with Arduino hardware. |
| Yatzil Romero  | Hardware Engineer | Setup and test the camera and board, handle data collection, assist with deployment. |
| Meng Xu        | Software Engineer | Train and optimize the CNN model, handle quantization, and implement interference testing. |

## 8. Timeline and Milestones

| Week | Milestone | Deliverable |
|------|------------|-------------|
| 2 | Proposal + Presentation | Planning & Research + GitHub submission |
| 4 | Midterm presentation, Model Implementation (Phase 1) | Presentation Slides, initial model results (non-live results)|
| 6 | Integration & testing with physical objects (Phase 2) | Working prototype (real-time results) |
| Dec. 18 | Final product & Presentation | Report, demo (video), GitHub archive, detailed documentation|

## 9. Resources Required

- Arduino Nano 33 BLE Sense
- microUSB cable (should be included with the given Arduino board)
- OV7670 VGA camera module
- Breadboard along with jumper cables
- Diverse image dataset of various waste types described above     (ex. TrashNet), we can also collect some of our own to put into the model as additional training data.
- Arduino IDE with Python

## 10. References

Include relevant papers, repositories, and documentation.

- Benefits of sorting waste and how AI hardware can prove useful: [Link](https://challenges.robotevents.com/uploads/0025368_original.pdf)
- Datasheet for Arduino Nano 33 BLE Sense board: [Link](https://docs.arduino.cc/resources/datasheets/ABX00031-datasheet.pdf)
- Datasheet for OV7670 VGA camera module: [Link](https://web.mit.edu/6.111/www/f2016/tools/OV7670_2006.pdf)
- TrashNet GitHub repository: [Link](https://github.com/garythung/trashnet)
