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
| **numpy** | 2.2.5 |
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
│  ├─ rain.csv/          # dataset
├─ src/
│  ├─ json2csv.ipynb      # Converted JSON file from CWA to CSV
│  └─ main.ipynb         # Z-score / IsolationForest anomaly detection
```
## Processing Summary
