# Urban Heat Island (UHI) Vulnerability & Cooling Center Planner

An automated decision-support pipeline combining FortyGuard hyper-local thermal data with community infrastructure metrics to prioritize municipal emergency heat interventions.

---

## 📌 Problem & Impact
Dense urban environments experience extreme microclimate variability where concrete corridors reach dangerous surface temperatures exceeding 45°C. Traditional municipal responses rely on coarse city-wide weather station averages. 

This project integrates the **FortyGuard Temperature API** to calculate a localized **Heat Vulnerability Index (HVI)**, pinpointing the top 5 critical heat risk zones to deploy emergency mobile cooling units, hydration stations, and urban canopy initiatives—reducing localized pedestrian exposure by an estimated 4–7°C.

---

## ⚙️ Architecture & Methodology
1. **Thermal Ingestion:** Fetches granular surface temperature layers via FortyGuard REST endpoints.
2. **Feature Fusion:** Overlays canopy coverage deficits and transit foot-traffic exposure data.
3. **Vulnerability Indexing:** Computes normalized HVI scores (0–100) across spatial coordinates.
4. **Actionable Outputs:** Generates an interactive Folium geospatial dashboard and a prioritized municipal dispatch table.

---

## 🛠️ Tech Stack
- **Language & Runtime:** Python 3.10+, Google Colab / Jupyter
- **API & Auth:** FortyGuard Temperature API, python-dotenv, requests
- **Data Analysis:** pandas, numpy
- **Geospatial Visualization:** folium, folium.plugins.HeatMap

---

## 🚀 Quickstart & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/muzainarehman18-debug/temperature-api-quickstart.git](https://github.com/muzainarehman18-debug/temperature-api-quickstart.git)
cd temperature-api-quickstart
pip install -r requirements.txt
FORTYGUARD_API_KEY=fg_live_your_api_key_here
jupyter notebook uhi_cooling_planner.ipynb
