# 🚖 Uber ML Analytics Project

A **Next.js-based ride-hailing application** integrated with **machine learning models** for fare and ETA prediction.  
This project combines a modern React frontend with Python ML services to deliver **intelligent ride estimation, surge pricing, and destination recommendations**.

---

## ✨ Features
- ML-powered **Fare Prediction** using Random Forest  
- Real-time **ETA Estimation** with confidence scoring  
- **Dynamic Surge Pricing** by zone and demand  
- Multiple ride categories: **Economy, Premium, Motorbike, Riksha, Auto Riksha**  
- **Feature Impact Analysis** for transparent predictions  
- Smart **Destination Recommendations**  

---

## 🏗️ Architecture

### Frontend
- Next.js 15+ with App Router  
- React + TypeScript  
- Tailwind CSS (light/dark mode)  

### Backend ML Services
- Linear predictor for basic fare & ETA  
- Random Forest models for advanced ML  
- Haversine formula for distance calculation  

---

## 🛠️ Tech Stack
| Component  | Technology |
|------------|------------|
| Frontend   | Next.js, React, TypeScript |
| Styling    | Tailwind CSS |
| ML Backend | Python, scikit-learn, pandas |
| Models     | Random Forest Regressor |
| Distance   | Haversine Formula |

---

## 📊 ML Model Details

### Ride Categories

| Category    | Base Fare | Cost/km | ETA Multiplier | Max Distance |
|-------------|-----------|---------|----------------|--------------|
| Economy     | 50 BDT    | 25 BDT  | 1.0x           | 30 km |
| Premium     | 100 BDT   | 40 BDT  | 0.8x           | 50 km |
| Motorbike   | 30 BDT    | 15 BDT  | 0.7x           | 40 km |
| Riksha      | 20 BDT    | 10 BDT  | 1.5x           | 10 km |
| Auto Riksha | 35 BDT    | 18 BDT  | 1.2x           | 20 km |

### Surge Zones (Dhaka)

| Zone                | Coordinates      | Multiplier |
|---------------------|------------------|------------|
| Gulshan / Banani    | (23.78, 90.41)   | 1.5x |
| Dhanmondi           | (23.75, 90.38)   | 1.3x |
| Old Dhaka / Motijheel| (23.72, 90.40)  | 1.8x |

---

## 🚦 Getting Started

### Prerequisites
- Node.js 18+  
- Python 3.8+  
- npm or yarn

## ML Pipeline

- Synthetic data generation for realistic ride patterns

- Random Forest models for fare & ETA prediction

- Feature engineering: time, weather, and location-based features

- Confidence scoring for reliability

### Factors reducing confidence:

- Distance > 30km

- Rush hour (7–9 AM, 5–7 PM)

- Rainy weather

- Riksha / Auto Riksha (route variability)

### Installation
```bash
# Clone repo
git clone https://github.com/Aruuu62/Uber-ML-Analytics-Project.git
cd Uber-ML-Analytics-Project

# Install frontend dependencies
npm install

# Install Python dependencies
pip install pandas scikit-learn

# Run development server
npm run dev

# Test ML prediction scripts
python scripts/predict_ride_details.py
python scripts/advanced_ride_predictor.py

