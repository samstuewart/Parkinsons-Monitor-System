# Dual-Mode Correlation System for Parkinson's Patients

This repository hosts the resources and files for the Dual-Mode Correlation System, which combines speech analysis and motion monitoring through machine learning models and wearable devices. The system is designed to detect and monitor Parkinson's disease symptoms, providing valuable insights into their progression and severity.

---

## Features

- **Dual-Mode Analysis**: Integrates speech patterns and motion data for comprehensive symptom tracking.
- **Machine Learning Integration**: Includes pre-trained models for efficient and accurate predictions.
- **Wearable Device Support**: Facilitates real-time motion monitoring.
- **Streamlit Interface**: User-friendly application interface for data input and visualization.

---

## Theoretical Background

Parkinson's disease (PD) is a progressive neurological disorder that primarily affects movement control and can lead to a variety of motor and non-motor symptoms. Early and accurate diagnosis is crucial for managing the disease and improving patient outcomes. However, traditional diagnostic methods can be subjective and rely heavily on clinical expertise.

This project leverages advancements in artificial intelligence and wearable technology to address these challenges. By analyzing speech patterns and motion data, it provides a more objective and quantitative approach to diagnosing and monitoring Parkinson's disease. The dual-mode system ensures a holistic analysis by capturing both vocal and physical manifestations of the disease.

### Speech Analysis

Changes in speech are one of the early indicators of Parkinson's disease. These changes may include reduced vocal intensity, slower speech, and variations in pitch. By using audio data, the system applies feature extraction techniques to identify patterns indicative of Parkinson's-related speech impairments.

### Motion Monitoring

Tremors, bradykinesia (slowness of movement), and rigidity are hallmark motor symptoms of Parkinson's disease. Wearable devices equipped with accelerometers and gyroscopes collect motion data, which is then analyzed using machine learning models to detect anomalies and assess symptom severity.

### Machine Learning Models

The repository includes pre-trained models such as Gradient Boosting, Random Forest, Support Vector Machine (SVM), and XGBoost. These models have been trained on curated datasets to identify patterns associated with Parkinson's disease. The system is designed to provide accurate predictions while allowing for retraining with updated data for continuous improvement.

---

## Repository Structure

### Core Files

| File                   | Purpose                                  |
|------------------------|------------------------------------------|
| `app.py`              | Main application script for deployment. |
| `parkinsons.ino`      | Code for hardware integration (Arduino).|
| `train_model.ipynb`   | Notebook for training ML models.         |

### Pre-Trained Models

- `gradient_boosting_model.pkl`
- `random_forest_model.pkl`
- `svc_model.pkl`
- `xgboost_model.pkl`

### Utility Files

- `scaler.pkl`: For feature scaling.
- `selector.pkl`: For feature selection.

### Dataset Folder

Contains audio and motion data files used for training and evaluation.

Example Structure:
```
dataset/
├── HC_AH/  # Healthy control samples
└── PD_AH/  # Parkinson's diagnosed samples
```

---

## Running the Application

### Step 1: Activate the Virtual Environment
```bash
source .venv/bin/activate  # For macOS/Linux
# OR
.venv\Scripts\activate  # For Windows
```

### Step 2: Launch the Application
```bash
streamlit run app.py
```

### Step 3: Input Data
Upload audio files or motion data as prompted by the interface for analysis.

---

## Training the Model

To retrain the machine learning models:

1. Open `train_model.ipynb` in Jupyter Notebook.
2. Follow the steps to preprocess the data and train the models.
3. Save the updated model files in the repository's root directory.

---

## Troubleshooting

### Common Issues

- **Missing Dependencies**: Ensure all required packages are installed:
  ```bash
  pip install -r requirements.txt
  ```

- **Dataset Errors**: Verify that the dataset is correctly structured and placed in the `dataset` folder.

### Debugging Tips

- Check application logs for detailed error messages.
- Validate the paths to dataset files and model files.

---

## Contributions

Contributions are welcome! Feel free to fork the repository, make your changes, and submit a pull request. Ensure that new features are well-documented.

---

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this software in compliance with the license terms.

---

Thank you for exploring the Dual-Mode Correlation System! Together, let's make a difference in Parkinson's care.

