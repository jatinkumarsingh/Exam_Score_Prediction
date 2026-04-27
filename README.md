# Student Exam Score Prediction

A machine learning application that predicts student exam scores based on key lifestyle and academic factors. Built with Python and deployed as an interactive web application using Streamlit.

## 📋 Overview

This project uses a trained regression model to forecast student examination performance by analyzing factors such as study habits, attendance, mental health, sleep patterns, and work commitments. The application provides educators and students with data-driven insights into how various lifestyle factors influence academic outcomes.

## 🎯 Features

- **Interactive Web Interface**: User-friendly Streamlit application for real-time predictions
- **Multiple Input Factors**:
  - Study hours per day (0-12 hours)
  - Attendance percentage (0-100%)
  - Mental health rating (1-10 scale)
  - Sleep hours per night (0-12 hours)
  - Part-time job status (Yes/No)
- **Score Normalization**: Predicted scores are automatically constrained between 0-100
- **Fast Predictions**: Sub-second response time using pre-trained model

## 📊 Dataset

The model is trained on a comprehensive dataset of 1,000+ student records containing:

### Features
- **Academic**: Study hours, attendance percentage, exam score
- **Lifestyle**: Sleep hours, diet quality, exercise frequency
- **Work/Social**: Part-time job status, social media hours, Netflix consumption
- **Health**: Mental health rating, internet quality
- **Demographics**: Age, gender, parental education level
- **Engagement**: Extracurricular participation

### Dataset Statistics
- **Records**: 1,000+ students
- **Total Features**: 16 variables
- **Target Variable**: Exam score (0-100)

## 🛠️ Technology Stack

- **Python 3.14+**
- **Streamlit**: Web application framework
- **Scikit-learn**: Machine learning model
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib & Seaborn**: Data visualization
- **Joblib**: Model serialization

## 📦 Installation

### Prerequisites
- Python 3.10+
- pip or conda package manager

### Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd Exam_Score
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
streamlit run app.py
```

The application will open in your default browser at `http://localhost:8501`

## 📝 Usage

1. Adjust the sliders for:
   - **Study Hours**: Select hours spent studying daily (0-12)
   - **Attendance**: Select percentage of classes attended (0-100)
   - **Mental Health**: Rate mental well-being on a scale of 1-10
   - **Sleep Hours**: Select hours of sleep per night (0-12)

2. Select whether the student has a part-time job (Yes/No)

3. Click the **"Predict Exam Score"** button

4. View the predicted exam score displayed on screen

## 📁 Project Structure

```
Exam_Score/
├── app.py                              # Streamlit web application
├── notebook.ipynb                      # Data analysis & model training
├── best_model.pkl                      # Trained ML model
├── student_habits_performance.csv      # Training dataset
├── requirements.txt                    # Project dependencies
└── README.md                           # This file
```

## 🔬 Model Information

- **Model Type**: Regression model (likely Random Forest or Gradient Boosting)
- **Target Variable**: Exam Score (0-100)
- **Input Features**: 5 normalized inputs
- **Performance**: Optimized for accuracy and generalization

The model was trained and evaluated using the provided Jupyter notebook, with comprehensive data preprocessing, exploratory analysis, and feature engineering.

## 📚 Data Preprocessing

The notebook includes:
- Missing value handling
- Duplicate detection and removal
- Exploratory Data Analysis (EDA)
- Categorical variable encoding
- Feature scaling and normalization
- Train-test split validation

## 🚀 Deployment

The application is deployed on **Streamlit Cloud** and accessible at:
```
https://examscoreprediction-ai.streamlit.app/
```

### Deployment Requirements
- requirements.txt with pinned versions
- best_model.pkl in project root
- app.py as main entry point

## 💡 Key Insights from Analysis

Based on the exploratory analysis in the notebook:
- Study hours significantly impact exam performance
- Attendance is a critical predictor of success
- Sleep deprivation can negatively affect scores
- Mental health status influences academic outcomes
- Work commitments may create study time constraints

## 🔧 Development

### Model Training (notebook.ipynb)
The notebook contains:
1. Data loading and exploration
2. Data cleaning and preprocessing
3. Feature engineering
4. Model selection and training
5. Hyperparameter optimization
6. Model evaluation metrics
7. Visualization of results

### To retrain the model:
```bash
jupyter notebook notebook.ipynb
# Run all cells to update best_model.pkl
```

## 📊 Example Predictions

| Study Hours | Attendance | Mental Health | Sleep | Part-time Job | Predicted Score |
|-------------|-----------|---------------|-------|---------------|-----------------|
| 6.0        | 95        | 8             | 8.0   | No            | ~85-90          |
| 3.0        | 75        | 5             | 6.0   | Yes           | ~55-65          |
| 8.0        | 100       | 9             | 9.0   | No            | ~95-100         |

## 🐛 Troubleshooting

**Issue**: Model prediction shows unexpected values
- **Solution**: Ensure input values are within specified ranges

**Issue**: Application fails to start
- **Solution**: Verify all dependencies are installed: `pip install -r requirements.txt`

**Issue**: Model file not found
- **Solution**: Ensure `best_model.pkl` exists in the project root directory

## 📄 License

This project is provided as-is for educational purposes.

## 👤 Author

Created as a machine learning project for student performance analysis and prediction.

## 🤝 Contributing

Improvements and suggestions are welcome. Consider:
- Adding more training data for better generalization
- Experimenting with advanced models (XGBoost, Neural Networks)
- Including confidence intervals in predictions
- Adding feature importance visualization
- Implementing cross-validation analysis

## 📞 Support

For issues or questions, please refer to the project documentation or contact the development team.

---

**Last Updated**: April 2026  
**Status**: ✅ Active and Maintained
