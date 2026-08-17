# Eye Blink Detection for Drowsy Driver Alert System Using CNN

## 📌 Project Overview

**Eye Blink Detection for Drowsy Driver Alert System Using CNN** is a computer vision and deep learning project designed to detect signs of driver drowsiness by monitoring the driver's eyes.

The system uses a **Convolutional Neural Network (CNN)** to classify eye images as **Open** or **Closed**. By continuously monitoring the driver's eye state, the system can identify prolonged eye closure and trigger an alert to warn the driver.

The main goal is to improve road safety by providing an early warning when signs of drowsiness are detected.

---

## 👨‍💻 Author

**Mahidhar Yadav**
Artificial Intelligence and Data Science Student

---

## 🎯 Objectives

* Detect whether the driver's eyes are open or closed.
* Monitor eye closure continuously.
* Identify prolonged eye closure as a possible sign of drowsiness.
* Generate an alert when drowsiness is detected.
* Develop a foundation for a real-time driver safety system.

---

## 🧠 Technologies Used

* **Python**
* **TensorFlow**
* **Keras**
* **Convolutional Neural Network (CNN)**
* **OpenCV**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Pygame / Playsound** for alerts
* **Jupyter Notebook / Google Colab**

---

## 🔄 System Workflow

```text
Camera / Video Input
        ↓
Face Detection
        ↓
Eye Detection
        ↓
Image Preprocessing
        ↓
CNN Model
        ↓
Eye State Classification
        ↓
Open / Closed
        ↓
Monitor Eye Closure Duration
        ↓
Drowsiness Detected?
      ↙       ↘
    No         Yes
    ↓           ↓
Continue     Alert Driver
Monitoring
```

---

## 📊 Dataset

The CNN model requires images representing different eye states.

A typical dataset structure is:

```text
dataset/
│
├── Open_Eyes/
│   ├── open_001.jpg
│   ├── open_002.jpg
│   └── ...
│
└── Closed_Eyes/
    ├── closed_001.jpg
    ├── closed_002.jpg
    └── ...
```

The dataset is divided into **training, validation, and testing** sets.

---

## 🤖 Why CNN?

A **Convolutional Neural Network (CNN)** is suitable for this project because it can automatically learn visual features from eye images.

The CNN learns patterns that help distinguish between:

* **Open eyes**
* **Closed eyes**

The trained model can then classify eye images captured from a live camera.

---

## 🏗️ CNN Model Architecture

```text
Input Eye Image
       ↓
Convolutional Layer
       ↓
ReLU Activation
       ↓
Max Pooling
       ↓
Convolutional Layer
       ↓
ReLU Activation
       ↓
Max Pooling
       ↓
Flatten
       ↓
Dense Layer
       ↓
Dropout
       ↓
Output Layer
       ↓
Open / Closed
```

---

## 🚨 Drowsiness Detection Logic

The system does not treat every blink as drowsiness.

Instead, it monitors the duration or frequency of eye closure.

Example:

```text
Eyes Open
    ↓
Normal Monitoring
    ↓
Eyes Closed
    ↓
Measure Closure Duration
    ↓
Short Closure → Normal Blink
    ↓
Prolonged Closure → Possible Drowsiness
    ↓
Trigger Alert
```

The threshold can be adjusted depending on the application's requirements.

---

## 📁 Project Structure

```text
Eye-Blink-Drowsiness-Detection/
│
├── dataset/
│   ├── Open_Eyes/
│   └── Closed_Eyes/
│
├── model/
│   └── eye_blink_cnn.h5
│
├── notebooks/
│   └── drowsiness_detection.ipynb
│
├── src/
│   ├── train.py
│   ├── detect_eye.py
│   └── drowsiness_alert.py
│
├── requirements.txt
│
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Eye-Blink-Drowsiness-Detection.git
```

### 2. Open the Project Directory

```bash
cd Eye-Blink-Drowsiness-Detection
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Example `requirements.txt`:

```text
tensorflow
keras
opencv-python
numpy
matplotlib
scikit-learn
pillow
pygame
```

---

## 🚀 How to Run

### Step 1: Prepare the Dataset

Place the eye images into the `Open_Eyes` and `Closed_Eyes` folders.

### Step 2: Train the CNN

```bash
python src/train.py
```

The trained model will be saved inside the `model` directory.

### Step 3: Start Real-Time Detection

```bash
python src/drowsiness_alert.py
```

The system will access the camera and monitor the driver's eye state.

---

## 🖥️ Expected Output

During real-time monitoring, the system can display:

```text
Eye Status: OPEN
Drowsiness: NORMAL
```

When prolonged eye closure is detected:

```text
Eye Status: CLOSED
Drowsiness: DETECTED
ALERT!
```

An audio warning can also be triggered to alert the driver.

---

## 📈 Model Evaluation

The CNN model can be evaluated using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **Confusion Matrix**

The training and validation accuracy/loss can also be visualized using graphs.

---

## 💡 Applications

This system can be used as a foundation for:

* Driver safety systems
* Vehicle monitoring
* Transportation safety
* Fleet monitoring
* Automotive research
* Real-time fatigue monitoring

---

## 🔮 Future Enhancements

* Add **yawning detection**.
* Use facial landmarks for improved eye tracking.
* Integrate with vehicle systems.
* Add vibration-based alerts.
* Send emergency notifications.
* Deploy the model on Raspberry Pi or edge devices.
* Use advanced deep learning models for improved accuracy.
* Develop a mobile or embedded version.

---

## ⚠️ Limitations

* Poor lighting can affect eye detection.
* Sunglasses may make eye detection difficult.
* Camera position can affect performance.
* Individual differences in blinking patterns may affect detection.
* The system should be considered a safety aid and not a replacement for responsible driving.

---

## 🎓 Project Purpose

This project demonstrates how **Deep Learning and Computer Vision** can be used to address driver safety problems.

By detecting eye closure using a CNN and monitoring prolonged closure, the system provides an automated warning mechanism that can help alert drivers when signs of drowsiness are detected.

---

## 👨‍💻 Developed By

**Mahidhar Yadav**
**Artificial Intelligence and Data Science**

> *Using Computer Vision and Deep Learning to build safer driving solutions.*
