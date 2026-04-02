
# 💪 EMG Gesture Classification
### Hand Gesture Recognition using 8-Channel EMG Signals for Prosthetic Control

<p align="center">
  <img src="https://img.shields.io/badge/status-Completed-brightgreen.svg" />
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Biosignal-EMG-purple" />
  <img src="https://img.shields.io/badge/ML-Classification-orange" />
  <img src="https://img.shields.io/badge/Model-Random%20Forest-success" />
  <img src="https://img.shields.io/badge/scikit--learn-Enabled-f7931e?logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/Preprocessing-StandardScaler-blueviolet" />
  <img src="https://img.shields.io/badge/Channels-8-informational" />
  <img src="https://img.shields.io/github/license/arshc0der/EMG-Gesture-Classification?color=green" />
  <img src="https://img.shields.io/github/stars/arshc0der/EMG-Gesture-Classification?style=social" />
  <img src="https://img.shields.io/github/forks/arshc0der/EMG-Gesture-Classification?style=social" />
  <img src="https://img.shields.io/github/issues/arshc0der/EMG-Gesture-Classification" />
  <img src="https://img.shields.io/github/last-commit/arshc0der/EMG-Gesture-Classification" />
</p>

---

## 🚀 Overview

This project builds a **machine learning pipeline for EMG signal classification** using **8-channel electromyography (EMG) data**.

The goal is to classify hand gesture classes for **prosthetic-control style applications**, where muscle activity signals are used to recognize intended movement patterns.

This project demonstrates a practical biosignal classification workflow including:

- dataset loading
- preprocessing
- normalization
- model training
- evaluation
- confusion matrix generation
- demo prediction

---

## 🎯 Project Objective

The main goals of this project are to:

- classify hand gesture classes from EMG signals
- build a baseline prosthetic-control style classifier
- demonstrate biosignal preprocessing and machine learning workflow
- generate clear evaluation outputs for model performance analysis

---

## 🧠 Project Overview

The model uses:

- **Input features:** `channel1` to `channel8`
- **Target label:** `class`
- **Model:** `RandomForestClassifier`
- **Preprocessing:** missing-value removal + normalization using `StandardScaler`

This makes the project a strong starting point for EMG-based gesture recognition systems.

---

## 📊 Final Demo Result

### Demo Prediction

```text
Predicted class: 0
Actual class: 0
Input values: {
  'channel1': -2e-05,
  'channel2': 1e-05,
  'channel3': 0.0,
  'channel4': -7e-05,
  'channel5': -3e-05,
  'channel6': 1e-05,
  'channel7': 0.0,
  'channel8': -1e-05
}
````

This example shows that the trained model correctly predicted the class for one test sample.

---

## 📦 Dataset

The dataset file is stored in compressed form to keep the repository lightweight.

### Expected dataset path

After extraction, the project should contain:

```bash
data/EMG-data.csv
```

### Compressed dataset file

You can keep the dataset in the repository as:

```bash
data/EMG-data.zip
```

or

```bash
data/EMG-data.csv.zip
```

Then extract it so the CSV becomes:

```bash
data/EMG-data.csv
```

---

## ⚠️ Why the Dataset is Zipped

The raw CSV file can be relatively large, while the zip file is much smaller.

Keeping it compressed helps to:

* reduce repository size
* improve cloning and downloading speed
* make the project easier to share with contributors

---

## 🏗 Project Structure

```text
EMG-Gesture-Classification/
│
├── data/
│   ├── EMG-data.zip               # or EMG-data.csv.zip
│   └── EMG-data.csv               # extracted dataset file
│
├── models/
│   ├── emg_random_forest.pkl
│   └── scaler.pkl
│
├── results/
│   ├── accuracy_report.txt
│   ├── confusion_matrix.png
│   └── demo_prediction.txt
│
├── train_emg.ipynb
├── README.md
└── .gitignore
```

---

## ⚙️ Machine Learning Pipeline

The classification workflow includes:

1. loading EMG data
2. selecting channels `channel1` to `channel8`
3. using `class` as the target label
4. removing missing rows
5. normalizing feature values
6. splitting data into training and testing sets
7. training a Random Forest model
8. evaluating predictions
9. saving model and result files

---

## 🧰 Tech Stack

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **scikit-learn**
* **SciPy**
* **joblib**

---

## 📦 Installation

Install Python 3.10+ and required libraries:

```bash
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

---

## 🐍 Virtual Environment Setup

### Windows PowerShell

```powershell
python -m venv emg_env
.\emg_env\Scripts\Activate.ps1
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

### Windows CMD

```cmd
python -m venv emg_env
emg_env\Scripts\activate.bat
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

### macOS / Linux

```bash
python3 -m venv emg_env
source emg_env/bin/activate
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

---

## 📥 Extract the Dataset

### If the dataset is `EMG-data.zip`

#### Windows PowerShell

```powershell
Expand-Archive -Path .\data\EMG-data.zip -DestinationPath .\data -Force
```

#### macOS / Linux

```bash
unzip data/EMG-data.zip -d data
```

### If the dataset is `EMG-data.csv.zip`

#### Windows PowerShell

```powershell
Expand-Archive -Path .\data\EMG-data.csv.zip -DestinationPath .\data -Force
```

#### macOS / Linux

```bash
unzip data/EMG-data.csv.zip -d data
```

After extraction, verify that this file exists:

```bash
data/EMG-data.csv
```

---

## ▶️ Run the Project

If you are using the notebook:

```bash
jupyter notebook
```

Then open:

```bash
train_emg.ipynb
```

and run all cells.

> Since this project uses a notebook, avoid writing `python train_emg.ipynb`.
> If you later convert it to a script, you can use:
>
> ```bash
> python train_emg.py
> ```

---

## 📁 Output Files

After running the project, the following files are generated:

```text
results/
├── accuracy_report.txt
├── confusion_matrix.png
└── demo_prediction.txt

models/
├── emg_random_forest.pkl
└── scaler.pkl
```

---

## 📝 Example Outputs

### Accuracy Report

Contains:

* overall model accuracy
* classification report
* class-wise performance summary

### Confusion Matrix

Shows how well the model predicts each class.

### Demo Prediction

Shows one sample prediction from the test set.

---

## 🖼 Visual Result

### Confusion Matrix

<p align="center">
  <img src="https://raw.githubusercontent.com/arshc0der/EMG-Gesture-Classification/refs/heads/main/results/confusion_matrix.png" width="70%" alt="EMG Confusion Matrix"/>
</p>

This matrix helps visualize how well the classifier distinguishes between gesture classes.

---

## 🔬 Features Used

The baseline model uses these EMG channels as input:

* `channel1`
* `channel2`
* `channel3`
* `channel4`
* `channel5`
* `channel6`
* `channel7`
* `channel8`

### Target Label

* `class`

---

## 📌 Notes

* This baseline version predicts the numeric values stored in the `class` column.
* The `time` and `label` columns are not used in the first version.
* If a mapping between class IDs and real gesture names becomes available later, the project can be upgraded to display gesture names instead of numeric classes.

---

## ✅ What This Project Demonstrates

* EMG biosignal preprocessing
* multi-channel feature-based classification
* normalization for stable model training
* supervised machine learning workflow
* confusion matrix based evaluation
* prosthetic-control style gesture recognition baseline

---

## ⚡ Current Strengths

* clean baseline machine learning pipeline
* practical biosignal classification use case
* easy-to-understand notebook workflow
* reusable saved model and scaler
* strong base for future signal-processing improvements

---

## 🛣 Future Improvements

* [ ] add EMG signal filtering
* [ ] implement window-based segmentation
* [ ] extract engineered EMG features such as:

  * MAV
  * RMS
  * Variance
  * Waveform Length
* [ ] compare with SVM, KNN, and XGBoost
* [ ] map numeric predictions to gesture names
* [ ] add live prediction support
* [ ] build a prosthetic-control demo interface
* [ ] evaluate feature importance across EMG channels

---

## 💡 Potential Applications

This kind of EMG gesture classification system can be extended for:

* prosthetic hand control
* human-computer interaction
* wearable biosignal interfaces
* rehabilitation systems
* gesture-based assistive technology

---

## 📄 Example `.gitignore`

```gitignore
__pycache__/
*.pyc
emg_env/
models/
results/
data/*.csv
```

> Adjust this depending on whether you want model files or images pushed to GitHub.

---

## 🤝 Contributing

Contributions are welcome.

If you'd like to improve preprocessing, add feature extraction, compare classifiers, or build a real-time EMG application, feel free to fork the repository and open a pull request.

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**arshc0der**

---

## 🌟 Repository Summary

This project is a practical implementation of:

* **EMG signal classification**
* **hand gesture recognition**
* **prosthetic-control style AI**
* **biosignal preprocessing**
* **machine learning classification**
* **performance evaluation with confusion matrix**

If you found this project useful, consider giving it a **star** on GitHub.
