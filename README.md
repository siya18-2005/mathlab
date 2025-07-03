# 🫀 ECG Signal Processing and Heart Rate Analysis (PhysioNet Data)

This MATLAB project demonstrates end-to-end ECG signal processing using data from the **PhysioNet MIT-BIH Arrhythmia Database**. It includes filtering, R-peak detection, heart rate calculation, and a basic health assessment.

---

## 📁 Dataset

The code uses a `.mat` file (e.g., `01911m.mat`) containing ECG recordings from PhysioNet.  
You can download similar files from: [https://physionet.org/content/mitdb/](https://physionet.org/content/mitdb/)

---

## ⚙️ Steps Performed

### 1. 📈 Original Signal Plot
- Load and visualize the raw ECG data.

### 2. 🧹 Baseline Wander Removal
- Use a **median filter** to remove low-frequency baseline drift.

### 3. 🎚️ Bandpass Filtering
- Apply a **Butterworth bandpass filter** (0.5–45 Hz) to clean the signal.

### 4. ❤️ R-Peak Detection
- Detect R-peaks using `findpeaks` with adaptive thresholding.
- Visualize R-peaks overlaid on the cleaned ECG.

### 5. 💓 Heart Rate & Rhythm Analysis
- Compute RR intervals and Heart Rate (HR).
- Perform a basic **risk assessment**:
  - Bradycardia: HR < 50 BPM
  - Tachycardia: HR > 100 BPM
  - Irregular rhythm (high HR variance)
  - Otherwise: Normal sinus rhythm

---

## 🖥️ Requirements

- MATLAB (tested with R2020 or later)
- Signal Processing Toolbox

---

## 🚀 How to Run

```matlab
% Load your PhysioNet ECG .mat file
data = load('01911m.mat');

% Then paste and run the script provided in this repo
