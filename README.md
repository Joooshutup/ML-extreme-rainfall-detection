# 🌦️ Taiwan Extreme Weather Anomaly Detection (2025)
## 📘 Overview
This project applies unsupervised machine learning (Anomaly Detection) to detect extreme rainfall events in Taiwan using daily precipitation data from the Central Weather Administration (CWA) Open Data Platform.
The analysis identifies rainfall outliers by station and date, highlighting regional and temporal patterns of extreme weather during 2025.

## 🖥️ Development Environment

This project was developed and tested under the following hardware and software environment:  
| Component | Specification |
|----------|---------------|
| **OS** | Windows 11 |
| **CPU** | Intel Core i5-8400 @ 2.80GHz |
| **RAM** | 16 GB |
| **Python** | 3.10.19 |
| **pandas** | 2.3.3 |
| **numpy** | 2.x |
| **scikit-learn** | 1.7.2 |
| **matplotlib** | 3.10.7 |
| **requests** | 2.32.5 |

> This project does not require GPU acceleration.  
> All data processing steps and anomaly detection models  
> (including Z-score and Isolation Forest) run smoothly on a standard CPU environment.

## 🧠 Objectives
Detect and visualize extreme rainfall anomalies across Taiwan. 
Compare the frequency and timing of anomalies among different regions. 
Demonstrate how AI models (e.g., Z-score, Isolation Forest) can reveal hidden climate patterns.

## 📂 Project Structure
```
rain-anomaly-2025/
├─ README.md
├─ DATA_SOURCES.md
├─ data/
│  ├─ raw/          # Original JSON files from CWA
│  ├─ processed/    # Converted and cleaned CSV/Parquet files
├─ notebooks/
│  ├─ 01_feature_eng.ipynb      # JSON parsing, cleaning, and feature extraction
│  └─ 02_anomaly_detection.ipynb# Z-score / IsolationForest anomaly detection
├─ src/
│  ├─ data_download/
│  │  └─ convert_json_to_csv.py # Script for JSON → CSV conversion
│  └─ viz.py                    # Visualization utilities (heatmap, line plots)
├─ reports/
│  └─ figures/                  # Output visualizations (heatmaps, maps, plots)
└─ requirements.txt
```
## 📊 Data Description
#### Source
- **Provider:** [Central Weather Administration (CWA), Taiwan](https://www.cwa.gov.tw/)  
- **Platform:** [CWA Open Data Platform](https://opendata.cwa.gov.tw/)  
- **Dataset:** [Daily Precipitation – Ground Weather Station Daily Rainfall Data /每日雨量-地面測站每日雨量資料](https://opendata.cwa.gov.tw/dataset/climate/C-B0025-001)  
- **Format:** JSON (downloaded and converted manually to CSV)  
- **Access Date:** 2025-11-11  
- **License:** [Government Open Data License, Version 1.0 (Taiwan)](https://data.gov.tw/license)

#### Variables (after preprocessing) 
| Variable | Description | Example |
| -------- | ------------| --------|
| `station_id` | Weather station ID | 466881 |
| `station_name` | Station name (Chinese) | 新北 |
| `station_name_en` | Station name (English) | New Taipei |
| `date` | Observation date (YYYY-MM-DD) | 2025-01-01 |
| `precip_mm` | Daily precipitation (mm) | 8.0 |

## Processing Summary
### 🧩 Data Processing Steps
- Raw JSON downloaded via CWA Open Data API (Dataset ID: S0001).  
- Parsed and normalized using `convert_json_to_csv.py`.  
- Extracted fields: `station_id`, `station_name`, `station_name_en`, `date`, `precip_mm`.  
- Missing or invalid values (e.g., `-99.0`) replaced with `NaN`.  
- Exported as `data/processed/daily_precip_2025.csv`.
