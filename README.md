Real-Time ALPR System with Domain Adaptation (YOLOv8s + ASTER)
This project presents a robust two-stage Automatic License Plate Recognition (ALPR) pipeline that operates effectively on both visible and thermal images. It integrates YOLOv8s for license plate detection and ASTER for character recognition, deployed with ONNX for efficient, cross-platform, real-time inference.

🚀 Overview
To address the domain gap between visible and thermal imagery, the system incorporates domain adaptation techniques such as:

Adversarial Learning

Semi-Supervised Learning

CORAL Loss (Correlation Alignment)

These methods help the model adapt from the labeled visible domain to the unlabeled or weakly labeled thermal domain, ensuring accurate performance in both environments.

🧠 Pipeline Architecture
Stage 1 – Detection (YOLOv8s)
Detects license plates in visible or thermal images with high speed and accuracy.

Stage 2 – Recognition (ASTER)
Recognizes plate characters using a robust scene text recognition model.

Domain Adaptation
Aligns features between visible and thermal domains using CORAL loss and adversarial training.

Post-Processing
Includes Non-Maximum Suppression (NMS), character cleaning, and error logging to ensure reliability.

📦 Deployment
Models are converted to ONNX for optimized inference.

Runs on the PGuard mobile robot for real-time deployment, including in low-visibility scenarios (e.g., night or thermal).

📊 Evaluation
Image Type	mAP@0.5	Precision	Recall
Visible (Validation)	95.9%	0.969	0.905
Thermal (Test)	73.1%	0.832	0.500

✅ Key Features
Dual-domain support: visible + thermal

Domain adaptation with adversarial & CORAL loss

Real-time deployment using ONNX

Two-stage modular design

Error logging & robustness mechanisms

📁 Future Work
Improve recall on thermal data with more annotated samples

Extend adaptation to other adverse conditions (e.g., rain, blur)

Test with alternative text recognition models
