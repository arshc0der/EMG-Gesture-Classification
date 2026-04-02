# EMG Signal Classification for Hand Gesture Recognition

This project builds a machine learning pipeline for **EMG signal classification** using 8-channel EMG data.  
The goal is to classify hand gesture classes for prosthetic-control style applications.

## Project Overview

The model uses:

- **Input features:** `channel1` to `channel8`
- **Target label:** `class`
- **Model:** `RandomForestClassifier`
- **Preprocessing:** missing-value handling + feature normalization with `StandardScaler`

## Dataset

The dataset file is stored in compressed form to keep the repository lightweight.

### Expected dataset path

After extraction, the project should contain:

```bash
data/EMG-data.csv
```

### Compressed file

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

## Why the dataset is zipped

The raw CSV is large, while the zip file is much smaller.  
This makes it easier for contributors to clone or download the project.

## Project Structure

```bash
emg_project/
│
├── data/
│   ├── EMG-data.zip          # or EMG-data.csv.zip
│   └── EMG-data.csv          # extracted file used by the script
│
├── models/
│   └── emg_random_forest.pkl
│
├── results/
│   ├── accuracy_report.txt
│   ├── confusion_matrix.png
│   └── demo_prediction.txt
│
├── train_emg.ipynb
└── README.md
```

## Requirements

Install Python 3.10+ and these libraries:

```bash
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

## Create Virtual Environment

### Windows PowerShell

```bash
python -m venv emg_env
.\emg_env\Scripts\Activate.ps1
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

### Windows CMD

```bash
python -m venv emg_env
emg_env\Scripts\activate.bat
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

### Mac/Linux

```bash
python3 -m venv emg_env
source emg_env/bin/activate
pip install numpy pandas matplotlib scikit-learn scipy joblib
```

## Extract the Dataset

### If the dataset is `EMG-data.zip`

#### Windows PowerShell

```powershell
Expand-Archive -Path .\data\EMG-data.zip -DestinationPath .\data -Force
```

#### Mac/Linux

```bash
unzip data/EMG-data.zip -d data
```

### If the dataset is `EMG-data.csv.zip`

#### Windows PowerShell

```powershell
Expand-Archive -Path .\data\EMG-data.csv.zip -DestinationPath .\data -Force
```

#### Mac/Linux

```bash
unzip data/EMG-data.csv.zip -d data
```

After extraction, verify this file exists:

```bash
data/EMG-data.csv
```

## Run the Project

```bash
python train_emg.ipynb
```

## What the Script Does

The script:

1. Loads `data/EMG-data.csv`
2. Selects `channel1` to `channel8` as features
3. Uses `class` as the target label
4. Removes missing rows
5. Normalizes the feature values
6. Splits the data into train and test sets
7. Trains a Random Forest model
8. Evaluates the model
9. Saves the results and trained model

## Output Files

After running the script, these files are generated:

```bash
results/accuracy_report.txt
results/confusion_matrix.png
results/demo_prediction.txt
models/emg_random_forest.pkl
models/scaler.pkl
```

## Example Outputs

### Accuracy report
Contains the overall model accuracy and classification report.

### Confusion matrix
Shows how well the model predicts each class.

### Demo prediction
Shows one example prediction from the test set.

## Notes

- This baseline version predicts the numeric values in the `class` column.
- The `time` and `label` columns are not used in the first version.
- If you later obtain a mapping from class IDs to gesture names, you can replace numeric classes with real gesture labels.

## Future Improvements

Possible next improvements:

- EMG signal filtering
- Window-based segmentation
- Feature extraction such as:
  - MAV
  - RMS
  - Variance
  - Waveform Length
- Comparison with SVM or KNN
- Mapping predicted classes to gesture names

## Internship Summary

This project demonstrates:

- EMG data preprocessing
- Multi-channel biosignal classification
- Machine learning model training
- Performance evaluation using:
  - accuracy
  - classification report
  - confusion matrix
  - demo prediction

## Author

arshc0der
