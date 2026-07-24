# Student Habits & Performance Prediction

An end-to-end Machine Learning data analysis and predictive modeling project that investigates how various daily habits—such as study hours, sleep, social media usage, and mental health—impact university students' academic performance (exam scores).

---

## 📌 Project Overview

Understanding the key drivers of student academic success allows educators and students to optimize habits for better outcomes. This project uses exploratory data analysis (EDA) and a Multiple Linear Regression model to predict a student's final exam score based on lifestyle choices, routine habits, and behavioral factors.

---

## 📁 Dataset Summary

The dataset `student_habits_performance.csv` contains 1,000 student records with 16 features covering demographic info, daily habits, and academic output.

| Feature Name | Type | Description |
| :--- | :--- | :--- |
| `student_id` | Identifier | Unique student ID |
| `age` | Integer | Student age (years) |
| `gender` | Categorical | Female / Male |
| `study_hours_per_day` | Numeric | Daily average study hours |
| `social_media_hours` | Numeric | Daily hours spent on social media |
| `netflix_hours` | Numeric | Daily hours spent watching streaming content |
| `attendance_percentage` | Numeric | Percentage of class attendance |
| `sleep_hours` | Numeric | Average night sleep duration |
| `mental_health_rating` | Integer | Self-reported mental health (1–10 scale) |
| `exercise_frequency` | Integer | Days exercised per week |
| `exam_score` | Numeric | **Target Variable** (0 – 100) |

---

## ⚙️ Methodology & Pipeline

1. **Data Cleaning & Preprocessing:**
   * Handled missing values in parental education level.
   * Extracted numerical features for regression baseline.
   * Split data into **80% Training** and **20% Testing** sets (`random_state=42`).

2. **Model Selection:**
   * **Multiple Linear Regression** was selected to evaluate the linear relationship between lifestyle habits and academic scores, offering high interpretability.

3. **Evaluation Metrics:**
   * Mean Absolute Error (**MAE**)
   * Root Mean Squared Error (**RMSE**)
   * Coefficient of Determination (**$R^2$ Score**)

---

## 📊 Model Performance & Results

The model performs exceptionally well in capturing performance trends:

* **$R^2$ Score:** `0.8989` (Explains **~89.9%** of variance in exam performance)
* **Mean Absolute Error (MAE):** `4.13` points
* **Root Mean Squared Error (RMSE):** `5.09` points

### Feature Coefficient Breakdown

| Feature | Coefficient | Impact on Exam Score |
| :--- | :---: | :--- |
| **`study_hours_per_day`** | **+9.53** | Strongest positive predictor (+9.5 points/hr) |
| **`sleep_hours`** | **+1.99** | Positive impact (+2.0 points/hr of sleep) |
| **`mental_health_rating`**| **+1.95** | Higher rating increases score (+1.95 points/level) |
| **`exercise_frequency`** | **+1.32** | Regular exercise boosts performance |
| **`attendance_percentage`**| **+0.15** | Steady attendance shows consistent positive gain |
| **`netflix_hours`** | **-2.32** | Detrimental impact (-2.3 points/hr) |
| **`social_media_hours`** | **-2.70** | Strongest negative habit (-2.7 points/hr) |

---

## 🔑 Key Insights

* **Study Time Rules Success:** Every extra daily hour dedicated to studying increases the final predicted score by nearly **10 percentage points**.
* **Distractions Penalty:** Daily social media and streaming video usage negatively correlate with performance, cutting exam outcomes by **2.3 to 2.7 points per hour**.
* **Wellness Matters:** Adequate sleep and solid mental health together account for significant cumulative score increases.

---

## 🛠️ Setup & Execution

### Requirements
* Python 3.8+
* `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

### Installation & Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/student-performance-prediction.git](https://github.com/your-username/student-performance-prediction.git)
   cd student-performance-prediction
