# SafarSuraksha – Geospatial Safety Heatmap (Folium + Leaflet)

This repository contains an interactive geospatial safety heatmap developed as part of the **SafarSuraksha** project during the Cyber AI Hackathon 2025.  
The map highlights safe vs. unsafe zones using lightweight ML logic based on incident density and anomaly detection.

The final output is a fully interactive HTML map generated using **Folium** (Python) and rendered with **Leaflet.js**.

---

## 🔍 Features
- Interactive map using Leaflet.js  
- Colour-coded safety zones  
- Risk levels derived from ML preprocessing (density + anomaly scoring)  
- One-click HTML visualization (no backend required)

---

## 🧠 ML / Data Logic Behind the Heatmap
Even though the visualization is rendered as an HTML file, the risk scoring was computed using:

- **Incident density modelling**  
- **Basic anomaly detection** for unusually high-risk points  
- **Time-of-day risk weighting**  
- Mapping of regions → categorical risk levels

These categories were then converted into colour codes by Folium’s choropleth-style function.  
The logic appears in the HTML file as the `geo_json_*_styler()` function, which assigns colours:

| Colour Code  | Meaning         |
|--------------|-----------------|
| `#d73027`    | High risk       |
| `#fc8d59`    | Medium-high     |
| `#fee08b`    | Medium          |
| `#91cf60`    | Low             |
| `#1a9850`    | Very low risk   |

---

## 🗂 Repository Structure
