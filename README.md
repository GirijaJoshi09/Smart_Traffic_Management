# Smart Traffic Optimizer — Machine Learning Based Traffic Prediction System

This project is a Machine Learning–based Smart Traffic Optimization System designed to predict Signal Time, Vehicle Flow, Accident Risk, and Traffic Clusters using real-time and historical traffic inputs.
The system integrates an Emergency Vehicle Priority mechanism, accident interval analysis, dashboard visualizations, and MySQL-backed prediction logging.

---

## Features

### 1. Signal Time Prediction (Linear Regression)

Predicts the optimal green signal duration based on:

* Traffic volume
* Vehicle distribution
* Average vehicle speed
* Hour of the day
* Weather impact

**Outputs:**

* Optimal Signal Time
* Confidence Score
* Prediction Accuracy

---

### 2. Vehicle Flow Prediction (Multiple Linear Regression)

Predicts upcoming traffic volume using:

* Average speed
* Temperature
* Humidity
* Traffic volume

**Outputs:**

* Vehicles per hour
* Confidence Score
* Variations in predicted flow

---

### 3. Accident Risk Prediction (Logistic Regression)

Estimates accident probability using:

* Speed variations
* Vehicle density
* Weather conditions
* Time of the day

**Outputs:**

* Accident Probability
* Risk Level (Low / Medium / High)
* Classification Confidence

---

### 4. Traffic Clustering (K-Means Clustering)

Groups traffic conditions into:

* Low congestion
* Medium congestion
* High congestion

This helps identify traffic patterns and peak congestion times.

---

### 5. Interactive Analytical Dashboard

The dashboard includes:

* Signal Time Trend Chart
* Vehicle Flow Trend Chart
* Accident Reports Over Time
* Vehicle Distribution Pie Chart
* Prediction Activity Chart
* Accident-Prone Interval Chart (based on weather and time)
* Real-time prediction accuracy indicators

---

## Changes Made During Final Evaluation

### 1. Accident Risk Interval Chart (Based on Historical Data + Weather)

A new accident analytics module was added that processes historical traffic records to generate:

* Accident frequency for each hourly interval (0–23)
* Weather-wise accident distribution
* A line chart displaying accident-prone intervals

This addition allows the system to highlight high-risk time periods under different weather conditions, improving predictive decision-making.

---

### 2. Emergency Vehicle Priority System

An emergency override mechanism was implemented to prioritize urgent vehicles such as ambulances, fire brigades, and police vehicles.

**Working:**

* User selects "Emergency Active" from the UI.
* The system reads the standard predicted green signal time.
* A controlled override is applied by adding additional green time (20–30 seconds).
* Minimum green-time safety checks are maintained.
* All emergency-triggered overrides are logged in MySQL with flags and metadata.

This ensures faster clearance for emergency vehicles without disrupting the prediction model.

---

## Machine Learning Models Used

| Module                   | Algorithm                  |
| ------------------------ | -------------------------- |
| Signal Time Prediction   | Linear Regression          |
| Vehicle Flow Prediction  | Multiple Linear Regression |
| Accident Risk Prediction | Logistic Regression        |
| Traffic Clustering       | K-Means Clustering         |

---

## Tech Stack

**Backend:** Python, Flask, Scikit-Learn, Pandas, NumPy
**Frontend:** HTML, CSS, JavaScript, Chart.js
**Database:** MySQL
**Model Storage:** Joblib
**Visualization:** JavaScript analytics charts

---

## Project Structure

```
├── src/
│   ├── app.py                  # Main Flask application
│   ├── train.py                # Training script for all ML models
│   ├── models_helper.py        # Prediction + confidence + accuracy logic
│   ├── priority_manager.py     # Emergency override logic
│   ├── routes/                 # API routing modules
│   ├── templates/              # Frontend HTML templates
│   └── static/                 # CSS, JS, assets
│
├── models/                     # Trained ML models and metadata
├── data/                       # Dataset used for training
└── README.md
```

---

## How to Run

### Step 1: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 2: Train all ML models

```bash
python src/train.py
```

### Step 3: Start the application

```bash
python src/app.py
```

### Step 4: Open dashboard in browser

```
http://127.0.0.1:5000/
```

---

## Results

* Signal Time Prediction Accuracy: 80% – 90%
* Vehicle Flow Prediction Accuracy: 70% – 85%
* Accident Classification Accuracy: 85% – 90%
* K-Means clustering successfully identifies congestion levels

The dashboard provides:

* Real-time prediction insights
* Historical analytics
* Emergency override detection
* Performance visualizations

---

## Future Scope

* Integration with live IoT traffic sensors
* Deep Learning (LSTM) for time-series traffic forecasting
* Multi-junction adaptive traffic control
* AI-based automatic emergency vehicle detection using GPS

---

## Contributors

* Gauri Bankar
* Manasi Jog
* Girija Joshi
