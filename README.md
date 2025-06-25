# Seismic Data Analysis & Regression Model Comparison

## 🌐 Mars Quake Visualizer (3D Web App - Local Use Only)

> ⚠️ This project is currently **not hosted online**. To view the 3D Mars quake visualization, follow the local setup instructions below.

### 📁 Project Directory Structure

```
project-root/
│
├── index.html
├── main.js
├── vite.config.js
├── package.json
├── assets/
│   ├── mars.jpg
│   ├── stars_px.png
│   ├── stars_nx.png
│   ├── stars_py.png
│   ├── stars_ny.png
│   ├── stars_pz.png
│   ├── stars_nz.png
│   └── data.json
```

### 🧰 Prerequisites

Ensure you have **Node.js** and **npm** installed. Then install Vite (if not already):

```bash
npm install -g vite
```

### 🚀 How to Run Locally

```bash
# Step 1: Clone the repo
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

# Step 2: Install dependencies
npm install

# Step 3: Start the dev server
npm run dev
```

Then open your browser and navigate to:
```
http://localhost:5173
```

> Make sure the textures in `/assets` are not missing. If you see missing images or 404s, double-check the image paths and filenames.

---

## 📊 Data Simulation and Classification

### Overview
This project processes and classifies shadow and non-shadow regions from simulated seismic data. The dataset is obtained from the [IRIS Syngine Data Simulation](https://ds.iris.edu/ds/products/syngine/).

### Data Preparation
The dataset consists of the following columns:

```
['Time', 'displacement1', 'displacement2', 'displacement3',
 'Class', 'dom_freq1', 'dom_freq2', 'dom_freq3', 'rms1', 'rms2', 'rms3',
 'max1', 'min1', 'range1', 'mean1', 'max2', 'min2', 'range2', 'mean2',
 'max3', 'min3', 'range3', 'mean3']
```

Scalers applied:
- `MinMaxScaler`
- `StandardScaler`
- `MaxAbsScaler`
- `RobustScaler`
- `QuantileTransformer`

### Installation
Install Python libraries:

```sh
pip install numpy pandas scikit-learn
```

### Usage
Run the classification script:

```sh
python classify_shadow.py
```

### Expected Output
The script classifies seismic shadow vs non-shadow zones based on derived statistical features.

---

## 🧪 Regression Model: Core Radius Prediction

### Dataset Columns:

| Column | Description |
|--------|-------------|
| 1 | Core Radius (km) *(Target)* |
| 2 | P-wave Velocity (km/s) |
| 3 | S-wave Velocity (km/s) |
| 4 | Density (g/cm³) |

### Model Details
The target variable (*Core Radius*) is predicted using features (*P-wave, S-wave, Density*). Models used:
- Linear Regression (best)
- Support Vector Regression
- Decision Tree Regression
- Polynomial Regression (degree 3)

Preprocessing: StandardScaler for normalization (mean 0, std 1)

### Performance
- Low MSE
- High R² score (~1)

---

## 🧩 Run Jupyter Notebook

```bash
pip install numpy pandas scikit-learn jupyter
jupyter notebook Module_7.ipynb
```

---

## 🗂️ Input Format

- Input: a ZIP containing `.SAC` files (Seismic Analysis Code)
- Types supported: `MXE`, `MXN`

---

## 📉 Output

- A plot showing anomalies
- Core radius regression results
- Shadow classification accuracy

---

*Note: For best results, keep libraries updated and ensure proper file paths are set in the scripts.*
