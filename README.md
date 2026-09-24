# India Air Quality Dashboard

**Question:** How do major pollutant trends compare across Indian cities in 2023–2025, and where do expected seasonal patterns break?

## Dataset attached to this project

Use the official-source, CPCB-derived dataset maintained at [Vonter/india-cpcb-aqi](https://github.com/Vonter/india-cpcb-aqi). It consolidates public Central Pollution Control Board (CPCB) Data Repository and AQI Repository records. The project provides 2023, 2024, and 2025 releases; its data dictionary documents station, city, timestamp, AQI, PM2.5, PM10, NO2, SO2, CO, and ozone fields.

Download a 2023, 2024, or 2025 release as CSV (if it is delivered as `.csv.gz`, unzip it first), then open `india-air-quality-dashboard.html`. The dashboard processes the file locally in the browser; no data is uploaded.

## Read-only profile before cleaning

Before aggregation, the dashboard reports row count, date coverage, cities, detected fields, and blank values. Its analysis then:

1. parses timestamps;
2. retains 2023–2025 records;
3. groups stations to city-month means;
4. excludes blank/non-numeric readings from each measure; and
5. keeps the source data untouched.

## Four retained views

1. **Compare:** city ranking for the selected measure.
2. **Break down:** monthly trends by city.
3. **Re-measure:** share of observations in CPCB AQI bands.
4. **Find exceptions:** city-by-month heatmap, highlighting breaks from the usual seasonal pattern.

Source and reuse terms: [CPCB-derived dataset repository](https://github.com/Vonter/india-cpcb-aqi), [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1.0/). The repository attributes the underlying data to CPCB.
