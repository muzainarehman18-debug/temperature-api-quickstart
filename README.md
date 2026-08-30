# 🌡️ Urban Heat Island (UHI) Vulnerability & Climate Planner

Built for the **FortyGuard Hackathon 2026** — *Track 1: Resilient Cities & Infrastructure*.

An automated municipal decision-support system and pedestrian microclimate explorer powered by **FortyGuard Large Temperature Model (LTM) API** layers.

---

## 📌 Problem & Overview
Extreme urban heat events create severe, localized microclimate variations across city blocks. Unshaded streets, exposed asphalt corridors, and vulnerable transit infrastructure frequently experience surface temperatures **5°C to 10°C hotter** than surrounding areas. 

Cities lack granular, spatial tools to prioritize heat mitigation funding, while pedestrians lack route-level thermal intelligence to navigate safely. This project solves both challenges by:
1. **Auditing & Ranking Heat Vulnerability:** Calculating a localized Heat Vulnerability Index (HVI) across municipal zones.
2. **Automating Intervention Dispatch:** Mapping recommended mitigations (cooling buses, misting shelters, cool pavement coatings) based on budget tiers.
3. **Guiding Pedestrians:** Identifying shaded street corridors, misting plazas, and public cooling waypoints.

---

## 🚀 Key Features

* **Interactive Microclimate Heatmap:** Dynamic spatial heatmap displaying peak surface temperature anomalies at 2m resolution.
* **Cool Street Corridors & Waypoints:** Highlights pedestrian pathways with verified tree canopies and active misting hubs.
* **Heat Vulnerability Index (HVI) Engine:** Quantifies exposure risk using the formula:
  $$\text{HVI} = \left(0.5 \times \text{Normalized Temp} + 0.3 \times \text{Canopy Deficit} + 0.2 \times \text{Pedestrian Density}\right) \times 100$$
* **Municipal Dispatch Table:** Real-time prioritization of top high-risk zones with assigned interventions and projected cooling ROI.
* **Dynamic Simulation Filters:** Real-time threshold adjustment for heat alerts and municipal budget allocation.

---

## 🛠️ Tech Stack & Dependencies

* **Frontend / UI:** [Streamlit](https://streamlit.io/)
* **Geospatial Mapping:** [Folium](https://python-visualization.github.io/folium/) & [streamlit-folium](https://github.com/randyzwitch/streamlit-folium)
* **Data Processing:** Pandas, NumPy
* **API Integration:** Requests, Python `os`
* **Data Source:** FortyGuard Hyperlocal Thermal API (~2m resolution LTM grid)

---

## 📦 Project Structure

```text
├── app.py                  # Main Streamlit web application & spatial analytics
├── requirements.txt        # Python package dependencies
├── README.md               # Project documentation
└── .env.example            # Environment variable template for API keys
