# Medical Appointment No-Show Prediction

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-teal?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?logo=plotly&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML%20Models-f7931e?logo=scikitlearn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

Predicting whether patients will miss their medical appointments using machine learning models. This project leverages advanced preprocessing, class imbalance handling, and multiple model architectures including MLP, XGBoost, and a hybrid MLP+XGBoost model.

---

## Project Overview

Missed medical appointments cause inefficiencies and increased costs in healthcare systems. This project aims to develop accurate models to predict no-shows, enabling targeted interventions such as reminders and rescheduling. Using a real-world clinical dataset with over 110,000 records, we build, tune, and evaluate multiple models for this classification task.

---

## Dataset

- Source: [Kaggle Medical Appointment No-Show Dataset](https://www.kaggle.com/datasets/joniarroba/noshowappointments)  
- Size: 110,527 records  
- Target: `No-show` (0 = Showed up, 1 = Missed)  
- Characteristics: Imbalanced classes (~20% no-shows)  
- **Note:** The dataset is **not included** in this repository due to licensing. Please download it from Kaggle and place it accordingly before running the code.

---

## Feature Engineering

Key features engineered from the raw dataset include:

- **Age** (cleaned and validated)  
- **Gender** (encoded)  
- **ScheduledDay** and **AppointmentDay** converted to datetime, from which:  
  - `DaysBetween` — Number of days between scheduling and appointment  
  - `ScheduledWeekday` — Day of week appointment was scheduled (0=Mon, ..., 6=Sun)
  - `IsWeekendAppointment` — Boolean flag for weekend appointments
  - `AppointmentWeekday` - Day of week appointment occurs
- **Neighbourhood** (removed)  
- Additional behavioral and temporal features derived to improve model predictive power

---

## Modeling Pipeline

The project follows a structured pipeline:

1. **Project Definition and Scope**  
2. **Data Collection**  
3. **Exploratory Data Analysis (EDA) – Before Feature Engineering**  
4. **Feature Engineering**  
5. **Exploratory Data Analysis (EDA) – After Feature Engineering**  
6. **Data Preprocessing** (handling missing data, encoding, normalization, train-test split, and SMOTE oversampling)  
7. **MLP Development** (model design, training, hyperparameter tuning, evaluation)  
8. **XGBoost Development** (baseline and tuned models, class imbalance strategies, evaluation)  
9. **Hybrid Model Development** (MLP feature extractor + XGBoost classifier)  
10. **Conclusion and Recommendations**

---

## Results

- Performance metrics and evaluation results are saved as CSV files included in this repository.  
- Models were assessed primarily on accuracy, precision, recall, and F1-score, with recall prioritized due to the nature of the problem.

---

## Visualizations

Various visualizations such as class distributions, confusion matrices, feature importance plots, and training curves are included throughout the project to support analysis and interpretation.

---

## How to Run

1. Clone this repository.  
2. Download the dataset from Kaggle and place it in the `/data` directory.  
3. Install dependencies
4. Run the preprocessing scripts or notebooks to prepare the data.
5. Execute the modeling scripts/notebooks for MLP, XGBoost, and Hybrid models.
6. Review results in the generated CSV files and visualizations.

---

## License

This project is licensed under the MIT License. This license is recommended for open source projects as it provides permissive reuse with minimal restrictions, allowing others to freely use, modify, and distribute the code while protecting your rights.

---

## Contact / Questions

Feel free to open an issue or contact me for questions or collaboration opportunities.
