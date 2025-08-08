# Plant Diagnosis – Code and Notebooks

This folder contains the key scripts and notebooks used for the **plant health classification** project, including model development, inference, and dataset inspection.

---

## 📓 SimSiam_ConvNextXLarge

**Purpose:**  
Main notebook for **final model development**.  
- Designed for execution on **Kaggle**.  
- Implements SimSiam pretraining with **ConvNextXLarge** backbone.  
- Trains the final classifier on the full plant diagnosis dataset.  
- Includes data preprocessing, augmentation, and evaluation pipelines.

---

## 📓 Inference-Notebook

**Purpose:**  
Run inference with a trained model.  
- Also designed for **Kaggle** execution.  
- Usage:
  1. Import your trained model folder into the Kaggle notebook inputs.
  2. Import the dataset into the Kaggle notebook inputs.
  3. Modify the relevant import lines to match your model and dataset paths.
- Outputs performance metrics (accuracy, F1 score, etc.) and confusion matrix.

---

## 🐍 labeling.py

**Purpose:**  
Identify and label **troll images** in the dataset (e.g., “shrek” and “trolololo”) so they can be removed before training.

---

## 🐍 plot.py

**Purpose:**  
Manually inspect dataset images.  
- Useful for understanding dataset characteristics.
- Helps detect anomalies and assess class balance visually.

---

### 🛠 Workflow Overview

1. **Data Cleaning:**  
   Use `labeling.py` to detect and tag non-plant images for removal.

2. **Model Development:**  
   Use `SimSiam_ConvNextXLarge` notebook to pretrain and train the plant diagnosis model.

3. **Dataset Inspection (Optional):**  
   Use `plot.py` to visually inspect and understand dataset samples.

4. **Model Inference:**  
   Use `Inference-Notebook` to evaluate the trained model and generate predictions.

---

### 📄 References
This code is based on the methodology described in the **CNN Plant Diagnosis** report, combining:
- Self-supervised learning with SimSiam.
- Transfer learning with ConvNextXLarge backbone.
- Manual dataset cleaning to remove irrelevant/outlier images.
