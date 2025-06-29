🧠 MRI Brain Tumor Detection using Deep Learning & Flask
This project enables automatic brain tumor detection and classification from MRI images using a deep learning model (VGG16 Transfer Learning) and a Flask-based web application for real-time user interaction.

📌 Project Overview
 Users can upload MRI images (PNG/JPG) via a web interface.
 
The trained model predicts:

Tumor presence/absence

Tumor type (Glioma, Meningioma, Pituitary)

Confidence score

 Results and uploaded images are displayed clearly for user understanding.

🛠️ Technologies Used
Python

TensorFlow / Keras (for deep learning and transfer learning)

OpenCV, Pillow (image processing)

NumPy, Matplotlib, scikit-learn (data preprocessing and evaluation)

Flask (backend server)

HTML, CSS, Bootstrap (frontend for file upload and display)

📈 Workflow

1️⃣ Data Preparation
Dataset: MRI images categorized into no_tumor, glioma, meningioma, pituitary.

Preprocessing:

Resize to 128x128.

Brightness/contrast adjustments using Pillow.

Data augmentation for robustness.

Labels are encoded into integers using a custom encoder.

2️⃣ Model Training
Transfer Learning: VGG16 (pre-trained on ImageNet) used with custom dense layers for classification.

Initial layers frozen; final layers fine-tuned for the MRI dataset.

Compiled with Adam optimizer (lr=0.001).

Trained for 5 epochs with batch size 20.

Visualization:

Accuracy and loss plots across epochs.

Confusion matrix and ROC curves for evaluation.

Achieved ~95% accuracy on validation data.

3️⃣ Model Saving & Loading
Saved as .h5 for easy reuse.

Loaded using tf.keras.models.load_model() for testing and deployment.

4️⃣ Flask Web Application

### 📦 Project Structure

```plaintext
/models
    model.h5

/templates
    index.html

/static
    (optional CSS/images)

main.py
```


⚙️ Functionality:
Users upload MRI images.

Flask handles file uploads and saves them dynamically.

Model predicts tumor type and confidence.

Results and the uploaded image are displayed on the web page.

## 🚀 How to Run

1️⃣ **Clone the repository:**

```bash
git clone https://github.com/yourusername/mri-brain-tumor-detector.git
cd mri-brain-tumor-detector
```

2️⃣ **Install dependencies:**

```bash
pip install -r requirements.txt
```

3️⃣ **Run Flask server:**

```bash
python main.py
```

4️⃣ **Open your browser:**

```
http://127.0.0.1:5000/
```

Upload an MRI image, view predictions, and test the system.



💡 Key Highlights
✅ Efficient data handling and augmentation
✅ Transfer learning for high accuracy with fewer epochs
✅ User-friendly web interface for real-time testing
✅ Clear visualization of predictions and confidence levels
✅ Lightweight, fully open-source, and extendable

