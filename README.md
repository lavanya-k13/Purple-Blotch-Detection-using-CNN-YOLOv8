**Purple Blotch Detection Using Convolutional Neural Networks**



This repository contains the implementation of a deep learning-based approach to detect purple blotch disease in crops, specifically focusing on onion leaves. Purple blotch is a significant fungal infection affecting crops like onions, garlic, leeks, and shallots, leading to reduced yields and economic losses.



**Table of Contents**

• Abstract

• Keywords

• Introduction

• System Comparison

• Key Features

• System Architecture

• Methodology

• Project Timeline

• Evaluation and Results

• Conclusion and Future Enhancements

--------------------------------------------------------------------------------



**Abstract**

The project presents a novel approach using Convolutional Neural Networks (CNNs) and the YOLOv8 architecture to identify purple blotch lesions on onion leaves. By training on a comprehensive dataset of high-resolution images and employing transfer learning, the system achieves robust classification performance under varying real-world conditions.



**Keywords**

Purple Blotch, YOLOV8, Convolutional Neural Networks.


## 📄 Published Paper
The detailed research findings of this project are published in the following paper:

🔗 **Paper Link:** https://ijcrt.org/papers/IJCRT2403249.pdf


**Introduction**

Manual identification of crop diseases is proactive but often inefficient. This project leverages CNNs—a class of deep neural networks designed for object detection and image classification—to automate the detection of diseased areas on crop leaves. By utilizing annotated datasets, the model learns to accurately distinguish between healthy leaves and those with purple blotch lesions.



**Existing System**

Traditionally, detection relies on manual inspection by agricultural experts.

**• Limitations:** Time-consuming, labor-intensive, prone to human error, and lacks scalability for large agricultural fields.



**Proposed System**

An automated detection system based on CNNs and YOLOv8.

**• Improvements:** Achieves high accuracy, minimizes misdiagnosis, and enables real-time monitoring of crops.

**Key Features**

**• Automation:** Eliminates the need for manual inspection.

**• Scalability:** Can be deployed across large agricultural fields for comprehensive monitoring.

**• Adaptability:** The system can be adjusted to detect other diseases in various crops.

**• Efficiency:** Enables farmers to implement targeted management strategies quickly.



**System Architecture**

The system follows a standard CNN pipeline for image processing:

**1. Input Image:** High-resolution leaf images.

**2. Processing Layers:** Multiple stages of Convolution + ReLU and Pooling to extract features.

**3. Classification:** Full convolution and Softmax layers to generate labels (Diseased vs. Healthy).



**Methodology**

**Data Collection and Preprocessing**

**• Sources:** Agricultural research databases and field surveys.

**• Annotation:** Domain experts used bounding boxes to precisely label purple blotch lesions.

**• Preprocessing:** Images were resized, pixel values were normalized, and data augmentation (rotation, flipping, brightness adjustments) was applied to reduce overfitting.



**Model Selection and Setup**

**• Architecture:** YOLOv8 was selected for its real-time inference capabilities and high accuracy.

**• Framework:** PyTorch.

**• Transfer Learning:** Initialized with pre-trained weights from the COCO dataset to expedite convergence.



**Training the YOLOv8 Model**

The dataset was split into:

**• Training:** 70%.

**• Validation:** 15% (used for hyperparameter tuning).

**• Testing:** 15% (used for final evaluation). Training utilized Stochastic Gradient Descent (SGD) with momentum and a scheduled learning rate.



**Project Timeline**

The project was executed following a structured progression:

**1. Phase 1: Research \& Literature Survey -** Analyzing existing deep learning solutions for plant disease detection.

**2. Phase 2: Data Collection -** Gathering images via field surveys and databases.

**3. Phase 3: Annotation \& Preprocessing -** Labeling lesions with normalized coordinates and applying augmentation.

**4. Phase 4: Model Selection \& Training -** Configuring YOLOv8 and training on the 70/15/15 split.

**5. Phase 5: Evaluation \& Validation -** Testing the model on unseen data and real-world field images.



**Evaluation and Results**

The model’s performance was quantified using:

**• Metrics:** Precision, Recall, and F1-score.

**• Robustness:** The model demonstrated the ability to generalize to images captured under varying lighting and environmental conditions in onion fields.

**• Visual Validation:** Successful identification of "purpleBlotch" lesions was confirmed through bounding box predictions on test images.



**Conclusion and Future Enhancements**

The study successfully developed a robust system for the early detection of purple blotch disease.



**Future Enhancements**

**• Dataset Expansion:** Continuous augmentation with diverse images to improve generalization.

**• Model Optimization:** Exploring advanced architectures for better speed and accuracy.

**• Real-time Deployment:** Utilizing lightweight architectures for mobile or edge deployment.

**• System Integration:** Integrating with agricultural management systems for seamless decision-making.

--------------------------------------------------------------------------------

**Author:** 

Kanaparthi Lavanya  

