# Weather Data Processing Pipeline

Production-ready ETL pipeline for weather data analysis with real-time monitoring and SLA tracking.

## Overview

End-to-end data engineering solution that:
- Processes 20,885+ hourly weather records across 5 Italian cities
- Validates and enriches data with temperature categories and weather conditions
- Calculates aggregations at hourly and daily granularity
- Monitors SLA violations and anomalies in real-time
- Generates weather analytics for trend analysis and forecasting

**Status:** Production Ready | **Language:** Python | **Framework:** Pandas/NumPy

## Key Results

- **Data Quality:** 100% (20,885 records, 0 missing values)
- **Cities Analyzed:** 5 (Milan, Rome, Venice, Turin, Naples)
- **Processing:** 7-step ETL pipeline with monitoring
- **Features:** Temperature categories, rainfall flags, humidity levels
- **Outputs:** 3 CSV files ready for analytics

## Architecture

## Tech Stack

- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Python 3** - Core language
- **Jupyter Notebook** - Development environment

## Data Coverage

### Geographic Scope
- Cities: Milan, Rome, Venice, Turin, Naples
- Time Range: 2026-01-01 to 2026-06-24 (hourly)
- Total Records: 20,885
- Data Quality: 100%

### Metrics Tracked
- **Temperature:** Mean, min, max, standard deviation
- **Humidity:** Average levels with high-humidity flags
- **Precipitation:** Total rainfall with rainy hour counts
- **Wind Speed:** Average wind velocity
- **Pressure:** Atmospheric pressure readings

## Features Engineered

| Feature | Description | Use Case |
|---------|-------------|----------|
| `temp_category` | Freezing / Cold / Mild / Warm / Hot | Temperature classification |
| `is_rainy` | Binary flag (precipitation > 5mm) | Rainfall detection |
| `is_humid` | Binary flag (humidity > 70%) | Humidity monitoring |
| `temp_ma_24h` | 24-hour moving average | Trend smoothing |
| `hour`, `day`, `month` | Temporal features | Seasonality analysis |

## How to Run

```bash
# Prerequisites
pip install pandas numpy jupyter

# Execute
jupyter notebook weather_analytics.ipynb
```

## Output Files

- `weather_data_cleaned.csv` - Complete enriched dataset with all features
- `hourly_summary.csv` - Hourly aggregated metrics
- `daily_summary.csv` - Daily aggregated statistics

## Monitoring & SLA

### Quality Checks
- Temperature anomalies detected: 0 (> 45°C)
- High precipitation events detected: 0 (> 50mm)
- Data quality: 100.0%

### SLA Tracking
- Total records processed: 20,885
- Cities analyzed: 5
- Time range coverage: Complete (2026-01-01 to 2026-06-24)
- Missing values: 0

## Skills Demonstrated

- ✅ **Data Validation:** Type casting, range checks, duplicate detection
- ✅ **Feature Engineering:** Categorical binning, binary flags, moving averages
- ✅ **Aggregations:** GroupBy operations, multi-level aggregations
- ✅ **Monitoring:** SLA checks, anomaly detection, quality reporting
- ✅ **Temporal Analysis:** Date/time feature extraction
- ✅ **Data Persistence:** CSV export, structured output

## Real-World Applications

This pattern applies to:
- **Weather Forecasting:** Historical trend analysis, pattern recognition
- **Climate Monitoring:** Temperature and precipitation tracking
- **Agricultural Analytics:** Crop planning based on weather patterns
- **Energy Management:** Weather-based demand forecasting
- **IoT Data Processing:** Sensor data aggregation and analysis

## City Statistics Summary

Comprehensive statistics by city:
- **Temperature Range:** -10°C to 40°C (clipped for data quality)
- **Humidity Range:** 20% to 95% (validated and bounded)
- **Precipitation Range:** 0 to 100mm (realistic thresholds)

---

**Created:** June 24, 2026  
**Status:** Production Ready ✅
