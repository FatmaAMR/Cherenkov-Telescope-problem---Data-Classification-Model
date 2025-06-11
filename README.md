# Cherenkov-Telescope-problem---Data-Classification-Model
🛰️ Gamma/Hadron Classification with Cherenkov Telescope Data
This notebook presents a complete machine learning pipeline designed to classify high-energy gamma rays from hadronic background noise using data simulated from an atmospheric Cherenkov gamma-ray telescope. The goal is to accurately distinguish between signal events (gamma rays) and background noise (hadrons) by analyzing patterns produced by particle showers in the telescope's image plane.

## 🎯 Problem Statement

Ground-based Cherenkov telescopes detect high-energy cosmic events by capturing the Cherenkov radiation emitted during particle showers in the Earth's atmosphere.  
The challenge is to **discriminate between gamma-ray initiated showers (signal)** and **hadron-induced showers (background)** using derived image parameters.  
This classification task is crucial in astrophysics and cosmic ray research to filter meaningful events from background noise.

---

## 📊 Dataset Description

- **Source:** Monte Carlo–generated using the CORSIKA simulation software  
- **Total Instances:** 19,020  
- **Features:** 10 real-valued physics-based features  
- **Target:** Binary classification – Gamma (1) vs. Hadron (0)  
- **Missing Values:** None  

The features represent physical properties of elliptical shower images (known as **Hillas parameters**), used widely in gamma-ray astronomy for event reconstruction and classification.

---

## ⚙️ Workflow Overview

The notebook follows a complete supervised machine learning pipeline:

1. **Problem Formulation:**  
   - Understanding the physical context  
   - Defining a binary classification task  

2. **Data Loading & Exploration:**  
   - Visualizing feature distributions  
   - Checking class balance  

3. **Preprocessing:**  
   - Shuffling and splitting into train/validation/test sets  
   - Handling class imbalance using oversampling techniques  

4. **Model Implementation & Evaluation:**  
   - Applied initial models:
     - **TomekLinks + Naive Bayes** (ToneNav)
     - **K-Nearest Neighbors** (KNN)  
   - Performance metrics:
     - Accuracy
     - Precision
     - Recall
     - F1-score
     - Confusion matrix  

5. **Iteration:**  
   I plan to implement and evaluate each ML algorithm I study — updating this notebook regularly as I progress through different modeling techniques.

6. **Goal:**  
   Achieve robust classification accuracy while maintaining interpretability based on physics-informed features.

---

## 🧪 Algorithms Implemented So Far

✅ **ToneNav** (TomekLinks for cleaning + Naive Bayes for classification)  
✅ **K-Nearest Neighbors (KNN)**  

🔄 **More algorithms coming soon**, including:  
- Decision Trees  
- Random Forest  
- Support Vector Machines  
- Gradient Boosting  
- Neural Networks  

---

## 📌 Future Enhancements

- Advanced feature engineering based on Hillas parameters  
- Hyperparameter tuning for each model  
- ROC curve and AUC analysis  
- Exporting best models for inference  
- Possibly integrating the pipeline into an interactive web app  

---

## 📁 File Structure

