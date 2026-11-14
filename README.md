<div align="center">

<!-- Animated Header Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=1,11,20,30&height=220&section=header&text=TERRATWIN%20AI&fontSize=50&fontColor=ffffff&animation=twinkling&fontAlignY=38&desc=%F0%9F%AA%90%20Planetary%20Geospatial%20AI%20%26%20Earth%20Analog%20Discovery&descFontSize=16&descAlignY=64&descAlign=50" width="100%" alt="TerraTwin AI Header"/>

<!-- Team Galactic Glitch Animated Typing -->
<br/>
<img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=700&size=24&duration=2500&pause=1000&color=00F5FF&center=true&vCenter=true&multiline=true&width=750&height=90&lines=%E2%9C%A8+BY+TEAM+GALACTIC+GLITCH+%E2%9C%A8;%F0%9F%9A%80+Mapping+Moon+%26+Mars+to+Earth+Analogs;%F0%9F%94%AC+100%25+Real+Kaggle+Observational+Remote-Sensing" alt="Team Galactic Glitch"/>
<br/>

<!-- Modern Tech Badges -->
<p align="center">
  <img src="https://img.shields.io/badge/Team-Galactic%20Glitch-7928CA?style=for-the-badge&logo=spacex&logoColor=white" alt="Team"/>
  <img src="https://img.shields.io/badge/Data-Kaggle%20Verified-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle"/>
  <img src="https://img.shields.io/badge/Backend-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Frontend-Three.js-FF5722?style=for-the-badge&logo=three.js&logoColor=white" alt="Three.js"/>
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
</p>

<!-- Animated Divider -->
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%" alt="Divider"/>

</div>

## 🌌 Overview
**TerraTwin AI** is a full-stack planetary geospatial intelligence platform engineered by **Team Galactic Glitch**. It discovers, compares, and ranks Earth analog environments for planetary regions across the **Moon** and **Mars** using **100% real observational remote-sensing datasets directly from Kaggle**.

---

## 🏗️ System Architecture

```
  ┌─────────────────────────────────┐       ┌─────────────────────────────────┐
  │   Three.js 3D Globe Client      │       │     FastAPI REST Gateway        │
  │     http://localhost:8080       │◄─────►│     http://localhost:8000       │
  └─────────────────────────────────┘       └──────────────┬──────────────────┘
                                                           │
                      ┌────────────────────────────────────┴──────────────────┐
                      ▼                                                       ▼
  ┌─────────────────────────────────┐                     ┌──────────────────────────────────┐
  │   Geospatial Processing Engine  │                     │    ML Analog Discovery Engine    │
  │ • Horn (1981) Windowed Slope    │                     │  • Multi-Metric Dynamic KNN      │
  │ • 5x5 RMS Surface Roughness     │                     │  • Transparent Missing Features  │
  │ • Geodetic Datum Alignment      │                     │  • Ranked Attribution Breakdown  │
  └─────────────────┬───────────────┘                     └──────────────────▲───────────────┘
                    │                                                        │
                    └─────────────────► [ Real GeoTIFFs ] ───────────────────┘
```

---

## 🛰️ Real Kaggle Datasets & Provenance

All datasets are verified via **SHA-256 checksums** inside `data/manifests/`:

| Planet | Kaggle Dataset Identifier | Source & Sensor | Files & Size | License |
| :---: | :--- | :--- | :---: | :---: |
| 🌕 **Moon** | `alexhhhh0938/lunar-nac-real-context` | NASA LRO LOLA 20mpp Polar Stereographic | `lunar20_nac_common.tif` (25.4 MB) | CC0 |
| 🌕 **Moon** | `encinas88/lunarsite-southpole-finetune` | NASA LRO LOLA 118m/px + Crater Rims | `southpole_finetune_118mpp.hdf5` (10.9 MB) | CC0 |
| 🌕 **Moon** | `yash92328/lunar-water-discovery` | Chandrayaan-1 M3 83-Band Spectral Cube | `Bullialdus_m3_tiff.tif` (46.3 MB) | CC0 |
| 🔴 **Mars** | `olekis/mars-terrain-ai-jezero-hazard-and-routing-data` | NASA HiRISE DTM (MOLA Datum) | Jezero DEM, Slope, Roughness (9.6 MB) | NASA Open |
| 🔴 **Mars** | `codebreaker619/mars-crater-study-dataset` | Robbins & Hynek Mars Crater Database | `Mars Crater info.csv` (16.8 MB) | USGS Open |
| 🌍 **Earth** | `dwarika/smoothed-digital-elevation-model-dem` | NASA SRTM 1 Arc-Second DEM | `dem_s_1s_clip.tif` (13.6 MB) | Public Domain |
| 🌍 **Earth** | `umutalkn/modis-lst-and-dem-marmara` | NASA MODIS Surface Temperature + DEM | `dataset_v3.csv` (4.2 MB) | CC BY 4.0 |
| 🌍 **Earth** | `erickfhernandezp/global-carnivorous-plants-with-climate-data` | WorldClim v2.1 Climate Grids + SRTM | `Riched Carnivorous Plant.csv` (34.6 MB) | CC BY 4.0 |

> [!IMPORTANT]
> **Scientific Honesty**: Missing layers (*LRO Diviner Temperature, LEND Neutron, CRaTER Radiation, LOLA PSR*) are declared `UNAVAILABLE_ON_KAGGLE` and **never fabricated or replaced with synthetic formulas**.

---

## 🔬 Core Algorithms

- **Slope (Horn 1981)**: $\text{Slope} = \arctan\left(\sqrt{(\partial z/\partial x)^2 + (\partial z/\partial y)^2}\right) \times \frac{180^\circ}{\pi}$
- **Surface Roughness (RMS)**: $\text{Roughness} = \sqrt{\overline{z^2} - (\bar{z})^2}$
- **Analog Similarity**: $d(\mathbf{x}, \mathbf{y}) = \sqrt{\sum_{k \in \text{valid}} w_k \left(\frac{x_k - y_k}{\sigma_k}\right)^2}, \quad S = \exp(-2.2 \times d) \in (0, 1]$

---

## ⚡ API Endpoints Summary

| Method | Endpoint | Description |
| :---: | :--- | :--- |
| `GET` | `/api/v1/health` | System health & validated datasets count |
| `GET` | `/api/v1/planets` | Planet catalog, radii, and connected layers |
| `POST` | `/api/v1/regions` | Select planetary coordinates & extract features |
| `POST` | `/api/v1/analogs/search` | **Core ML**: Search & rank top Earth analogs |
| `POST` | `/api/v1/analysis` | Run asynchronous background geospatial analysis |

---

## 🚀 Quick Start Guide

```bash
# 1. Install Dependencies
python -m pip install fastapi uvicorn rasterio scipy numpy pandas kagglehub h5py requests

# 2. Acquire & Verify Real Kaggle Data
python scripts/acquire_kaggle_data.py

# 3. Generate Derived Geospatial Products (Slope, Roughness)
python -m backend.geospatial.processor

# 4. Launch App (Backend :8000 + Frontend :8080)
python run_app.py
```
> Open **`http://localhost:8080`** in your browser.

---

<div align="center">

### 🛸 Engineered by Team Galactic Glitch
*Pioneering Planetary Geospatial Data & Earth Analog Discovery*

<!-- Animated Footer Wave -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=1,11,20,30&height=100&section=footer" width="100%" alt="Footer Wave"/>

</div>
