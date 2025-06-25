# 🤖 Martian Core Quake Visualizer (ML + 3D Visualization)

This project combines **machine learning** with **3D visualization** to analyze and display seismic activity on Mars. Using real or simulated Martian quake data, it predicts characteristics of seismic events and maps them visually using Three.js on an interactive globe.

---

## 🚀 Features

- 🔍 ML-based quake classification & prediction
- 🌍 Interactive 3D Mars globe (Three.js powered)
- 📍 Quake markers colored by magnitude
- 🔁 Expanding wave animations for impact visualization
- 🧭 Smooth orbit controls, zoom, pan
- 🔄 Reset alignment button for camera
- 📊 Dropdown-based quake selector for quick exploration
- 📐 Modular codebase for ML + visualization separation

---

## 🧠 Machine Learning Component

The ML model is trained to classify and regress seismic properties such as:

- Shadow vs. non-shadow zone detection
- Core radius prediction based on:
  - P-wave & S-wave velocity
  - Density values

### 📦 Algorithms Used

- Linear Regression ✅ (best performer)
- Polynomial Regression
- SVR (Support Vector Regression)
- Decision Tree Regression

### 📈 Evaluation

- Metrics: Mean Squared Error (MSE), R² Score
- Feature scaling using StandardScaler, MinMaxScaler, etc.

---

## 💻 Local Setup

### 1. Clone the Repository
```bash
git clone https://github.com/adyasa2004/martiancoreanalysis.git
cd martiancoreanalysis
```

### 2. Install Dependencies
Make sure you have **Node.js** and **npm** installed:
```bash
npm install
```

### 3. Start the App
```bash
npm run dev
```

### 4. View in Browser
Visit the URL printed in terminal (typically `http://localhost:5173/`)

---

## 🖼️ Screenshots
<!-- Add screenshots below -->
<p align="center">
  <img src="screenshots/screenshot1.png" alt="Visualization 1" width="600"/>
</p>

<p align="center">
  <img src="screenshots/screenshot2.png" alt="Visualization 2" width="600"/>
</p>

---

## 📁 Project Structure

```
martiancoreanalysis/
├── assets/              # Mars textures & quake data
├── main.js              # Three.js & visualization logic
├── ml/                  # (Optional) ML scripts or training code
├── index.html           # HTML template
├── style.css            # Custom styling
└── vite.config.js       # Vite build config
```

---

## 📚 Data Source

Quake data is simulated or adapted from:
- NASA InSight Mission seismic records
- IRIS Syngine simulations (synthetic seismograms)

---

## 🤝 Contributions

Got an idea? Found a bug? Want to improve visualization or ML? PRs and issues welcome!

---

## 🪐 Made with ML, JS & Space Curiosity by [@adyasa2004](https://github.com/adyasa2004)
