# Live Weather ETL Pipeline with Airflow & Aiven Cloud Postgres

An end-to-end data engineering pipeline that orchestrates live weather data extraction, transformation, and storage.

## 🛠️ Architecture & Tech Stack
* **Orchestrator**: Apache Airflow (managed locally via Astro CLI)
* **Containerization**: Docker Desktop
* **Cloud Database**: Aiven PostgreSQL Free Plan Tier
* **Data Origin**: Open-Meteo REST API

## 🔄 Core Pipeline Workflow (TaskFlow API)
1. **`extract_weather_data`**: Pulls live geographical climate metrics using the Python `requests` library.
2. **`transform_weather_data`**: Cleans and normalizes raw JSON payloads.
3. **`load_weather_data`**: Builds a target schema and loads records over a secure SSL handshake into cloud storage.
