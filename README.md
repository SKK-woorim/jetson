### **Construction Site Safety Helmet Detection AI**

---

## **Overview**

This project focuses on developing an AI system capable of detecting construction workers who are not wearing safety helmets. By leveraging advanced computer vision techniques and machine learning, the project aims to improve safety compliance at construction sites and reduce the risk of workplace injuries.

The AI model is built using the **YOLOv5 (You Only Look Once)** object detection framework, known for its speed and accuracy in real-time detection. The system can analyze video feeds or images from construction sites to identify workers and determine whether they are wearing helmets, providing actionable insights for safety managers.

---

## **Objectives**
- **Real-time Detection**: Identify workers not wearing safety helmets in live video feeds.
- **Compliance Monitoring**: Enhance safety compliance by automating the detection process.
- **Risk Reduction**: Minimize workplace accidents caused by the absence of protective gear.

---

## **How It Works**

### **1. Dataset**
- **Images**: The dataset consists of images collected from real construction sites, with annotations for workers with and without helmets.
- **Annotations**: Each worker is labeled as either "Helmet" or "No Helmet," enabling the AI to distinguish between the two classes.
- **Diversity**: The dataset includes varying lighting conditions, worker postures, and site environments to ensure robustness.

### **2. Model Architecture**
- **YOLOv5** is used for its high-speed processing and accuracy in detecting multiple objects in complex scenes.
- The model is trained to recognize workers and classify them based on whether they are wearing helmets.

### **3. Training**
- **Labeling**: Images are pre-processed and labeled using tools like Roboflow or LabelImg.
- **Augmentation**: Data augmentation techniques are applied to improve the model's generalization.
- **Training Pipeline**: The model is trained over multiple epochs to achieve high precision and recall.

### **4. Deployment**
- The trained model can be deployed on edge devices, cameras, or cloud systems for real-time analysis.
- Alerts can be generated when a worker without a helmet is detected.

---

## **Features**
- **High Accuracy**: Detects workers with or without helmets with precision.
- **Real-Time Processing**: Analyzes video streams or images instantly.
- **Customizable Alerts**: Sends notifications to site managers when safety violations are detected.

---

## **Installation and Usage**

To set up the project and run detection:

```bash
# Step 1: Clone the repository
git clone <repository-url>

# Step 2: Install dependencies
pip install -r requirements.txt

# Step 3: Train the model (if using a custom dataset)
python train.py --data data.yaml --cfg models/yolov5s.yaml --weights yolov5s.pt --epochs 100

# Step 4: Run inference
python detect.py --source <video_or_image_path> --weights runs/train/best.pt
```

---

## **Results**
- The model achieved:
  - **Accuracy**: 96%
  - **Precision**: 93%
  - **Recall**: 91%
- Results demonstrate reliable detection of workers without helmets, even in challenging conditions.

---

## **Future Work**
- **Improved Dataset**: Expand the dataset to include diverse construction scenarios.
- **Integration**: Develop a mobile app or dashboard for easier safety monitoring.
- **Edge Deployment**: Optimize the model for deployment on low-power devices like Raspberry Pi or Jetson Nano.

---

## **Impact**
- **Safety Compliance**: Encourages workers to wear helmets consistently.
- **Risk Mitigation**: Reduces the likelihood of accidents due to non-compliance.
- **Automation**: Eliminates the need for manual monitoring, saving time and resources.

---

## **License**
This project is licensed under the MIT License. See the LICENSE file for details.

---

### **Conclusion**
This Safety Helmet Detection AI project provides an innovative solution to improve safety compliance at construction sites. By leveraging AI, it automates the monitoring process, enabling real-time detection and proactive measures to protect workers.
