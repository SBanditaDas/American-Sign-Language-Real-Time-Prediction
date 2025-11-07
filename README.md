---

# 🧾 ASL Detection – Image-Based Sign Language Recognition 

_Recognizing American Sign Language gestures from images using Convolutional Neural Networks (CNNs), data augmentation, and real-time webcam prediction._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>

This project detects ASL gestures from image inputs using a deep learning pipeline built in Google Colab. It leverages CNNs and real-time webcam prediction to classify hand gestures with high accuracy. The workflow includes image preprocessing, model training, evaluation, and live prediction — all within a Colab notebook.

---

<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

ASL recognition can empower inclusive communication for the hearing-impaired. This project aims to:
- Automate ASL gesture detection from webcam feeds
- Reduce reliance on manual interpretation
- Enable real-time prediction in browser-based environments
- Support accessibility in digital platforms

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Image dataset uploaded to `/content/data/` in Colab with folders per gesture (A–Z)
- Includes training and validation sets
- Augmented using rotation, flip, zoom, and brightness tuning
- Stored temporarily in Colab runtime or mounted from Google Drive

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- Python (TensorFlow, OpenCV, NumPy, Matplotlib)
- Google Colab (GPU acceleration, webcam access)
- GitHub (for version control and notebook hosting)
- Google Drive (optional dataset mounting)

---

<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
asl_detection/
│
├── README.md
├── train_model.ipynb                # Main training notebook
├── realTime_prediction.ipynb        # Webcam prediction notebook
│
├── asl_dataset                      # Uploaded image dataset
│   ├── A/
│   ├── B/
│   └── ...Z/
│
├── models/                          # Saved models (.h5)
│   └── asl_model.h5
├── requirements.txt
├──asl_detection.pdf                 # summery pdf
```

---

<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

- Removed blurry and mislabeled gesture images  
- Resized all images to 64x64 pixels  
- Applied augmentation to balance gesture classes  
- Encoded labels and split into train/val sets  

---

<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

**Class Distribution:**  
- 26 ASL gesture classes (A–Z)  
- Balanced using augmentation for underrepresented gestures  

**Image Quality Checks:**  
- Verified resolution and gesture clarity  
- Removed grayscale and low-contrast images  

**Sample Visuals:**  
- Grid plots of gesture samples  
- Bar chart of image count per class  

---

<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

- Model Accuracy: Achieved 92.8% accuracy on validation set  
- Misclassifications: Most confusion between M vs. N and U vs. V  
- Augmentation Impact: Boosted accuracy by 6.3% on minority gestures  
- Confidence Scores: Average prediction confidence = 0.89  
- Real-Time Prediction: Webcam latency <1.2s per frame  

---

<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

- Real-time webcam interface via `cv2.VideoCapture()` in Colab  
- Displays:  
  - Live gesture prediction  
  - Confidence score overlay  
  - Frame-by-frame classification  


---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Open the training notebook in Colab:  
   🔗 [ASL_Detection_Training.ipynb](https://github.com/SBanditaDas/asl-detection/blob/main/ASL_Detection_Training.ipynb)

2. Upload your dataset to `/content/data/` or mount Google Drive:
```python
from google.colab import drive
drive.mount('/content/drive')
```

3. Train the model:
```python
# Run all cells in ASL_Detection_Training.ipynb
```

4. Run real-time webcam prediction:  
   🔗 [ASL_RealTime_Prediction.ipynb](https://github.com/SBanditaDas/asl-detection/blob/main/ASL_RealTime_Prediction.ipynb)

---

<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Expand dataset with dynamic hand gestures and backgrounds  
- Integrate hand tracking for better localization  
- Use Grad-CAM for gesture explainability  
- Collaborate with accessibility-focused organizations for real-world testing  

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Sushree Bandita Das**  
 
 📧 Email: sushreebanditadas01@gmail.com  
🔗 [LinkedIn](http://www.linkedin.com/in/sushree-bandita-das-160651309)  
🔗 [Portfolio](http://datascienceportfol.io/sushreebanditadas01)

---

