**PurpleBlotchDetection Python Script – Code Explanation**

This document provides a detailed explanation of the PurpleBlotchDetection Python script, which is designed to detect purple blotch disease on onion leaves using the YOLOv8 object detection framework.

**1. Project Initialization and Environment Setup**

The script begins by mounting Google Drive to access the agricultural dataset and to store training outputs. The Ultralytics YOLOv8 library is installed to enable object detection, training, and inference.

Libraries Used: Common data science libraries such as NumPy, Pandas, Matplotlib, and Seaborn are imported for data processing, analysis, and visualization.

Image Processing: OpenCV (cv2) is used for image preprocessing and color space conversions, while Pillow (PIL) is utilized for verifying image metadata and ensuring dataset integrity.

**2. Initial Model Inference (Pre-trained)**

Before model training, a pre-trained YOLOv8n (yolov8n.pt) model is loaded to perform baseline inference on a sample test image.

Inference Parameters: The image is resized to 640 × 640 pixels with a confidence threshold set to 0.5.

Visualization: Detected objects are annotated on the image, converted from BGR to RGB format for proper display using Matplotlib, and visualized with the title “Detected Objects in Sample Image by the Pre-trained YOLOv8 Model on COCO Dataset”.

**3. Dataset Configuration and Verification**

The script performs a detailed inspection of the custom agricultural dataset stored in Google Drive.

YAML Configuration: The data.yaml file is loaded to define dataset paths and class labels related to purple blotch disease.

Data Integrity Check: The training and validation directories are scanned to count the total number of .jpg images, verify image dimensions, and determine whether the dataset contains uniform or varying resolutions.

**4. Model Training Pipeline**

The core phase of the script fine-tunes the YOLOv8 model specifically for purple blotch disease detection.

Training Hyperparameters:

Epochs: 100

Image Size: 640

Batch Size: 16

Learning Rate (lr0): 0.0001

Dropout: 0.1

Random Seed: 0 (for reproducibility)

Optimization Strategy: The optimizer is set to auto, allowing YOLOv8 to automatically select the most suitable optimizer (such as SGD or Adam) based on the training environment.

**5. Learning Curve Analysis**

To monitor and analyze training performance, a custom function named plot_learning_curve is defined.

Visualized Metrics: The script plots Box Loss, Classification Loss, and Distribution Focal Loss (DFL) for both training and validation sets across epochs.

Iterative Analysis: Multiple training runs such as train, train2, train22, and train222 are analyzed to compare performance improvements.

**6. Validation and Final Inference**

After training completion, the best-performing model weights are used for evaluation and final prediction.

Model Loading: The trained model is loaded with weights from best.pt.

Validation: Model validation is performed on the validation dataset split to generate final performance metrics.

Refined Inference: Final inference is conducted on a sample image using a higher confidence threshold of 0.7, ensuring that only high-confidence detections are visualized.

**7. Results Export and Preservation**

To ensure long-term storage and reproducibility, the entire runs directory—containing trained weights, plots, and CSV result files—is transferred from the temporary Colab environment to Google Drive using shutil.move.

This preserves all experimental outputs for future reference, deployment, or publication.
