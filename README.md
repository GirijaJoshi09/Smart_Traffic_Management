# Smart Traffic Optimizer — Machine Learning Based Traffic Prediction System

This project is a Machine Learning–based Smart Traffic Optimization System designed to predict Signal Time, Vehicle Flow, Accident Risk, and Traffic Clusters (K-Means).
It includes accuracy evaluation, interactive dashboard graphs, and MySQL-backed prediction logging.

---

## Features

### 1. Signal Time Prediction

Predicts optimal green signal duration based on real-time traffic data.
Outputs:

* Optimal Signal Time
* Model Accuracy (%)
* Confidence Score

### 2. Vehicle Flow Prediction

Forecasts upcoming traffic volume using speed, density, and weather variables.
Outputs:

* Vehicles per hour
* Model Accuracy (%)
* Predicted Change in Traffic Flow

### 3. Accident Risk Prediction

Predicts the probability of an accident using traffic and weather features.
Outputs:

* Accident Probability
* Risk Level (High / Medium / Low)
* Confidence Score

### 4. Traffic Clustering (K-Means)

Clusters traffic conditions into:

* Low Traffic
* Medium Traffic
* High Traffic

### 5. Interactive Dashboard

The interface displays:

* Signal Time Trend Chart
* Vehicle Flow Trend Chart
* Vehicle Distribution Pie Chart
* Accident Reports Over Time
* Traffic Cluster Visualizations
* Real-time model accuracy for every prediction

---

## Machine Learning Models Used

| Module                   | Algorithm                  |
| ------------------------ | -------------------------- |
| Signal Time Prediction   | Linear Regression          |
| Vehicle Flow Prediction  | Multiple Linear Regression |
| Accident Risk Prediction | Logistic Regression        |
| Traffic Clustering       | K-Means                    |

---

## Tech Stack

**Backend:** Python, Flask, Scikit-Learn, Pandas, NumPy
**Frontend:** HTML, CSS, JavaScript
**Database:** MySQL
**Model Storage:** Joblib
**Visualization:** Custom JavaScript charts and analytical dashboard

---

## Project Structure

```
├── src/
│   ├── app.py                 # Flask application
│   ├── train.py               # Training of all ML models with metadata
│   ├── models_helper.py       # Prediction + accuracy computation
│   ├── routes/                # API endpoints
│   ├── templates/             # Frontend HTML files
│   └── static/                # CSS and JS files
│
├── models/                    # Trained models and metadata files
├── data/                      # Dataset used for training
└── README.md
```

---

## How to Run

### Step 1: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 2: Train all Machine Learning models

```bash
python src/train.py
```

### Step 3: Start the Flask server

```bash
python src/app.py
```

### Step 4: Open the dashboard

```
http://127.0.0.1:5000
```

---

## Results

* Signal Time Prediction Accuracy: 80% – 90%
* Vehicle Flow Prediction Accuracy: 70% – 85%
* Accident Risk Classification Accuracy: 85% – 90%
* K-Means clustering successfully categorizes traffic into low, medium, and high congestion levels

The dashboard visualizes trends using:

* Signal time predictions
* Flow rate variations
* Accident probability
* Traffic clusters
* Model accuracy for each output

---

## Future Enhancements

* Integration with real-time IoT traffic sensors
* Deep Learning (LSTM) models for time-series forecasting
* Real-time adaptive traffic signal control
* Multi-junction coordinated traffic optimization

---

## Contributors

* **Gauri Bankar**
* **Manasi Jog**
* **Girija Joshi**

Just tell me, Girija Darling.
