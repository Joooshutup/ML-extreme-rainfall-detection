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
