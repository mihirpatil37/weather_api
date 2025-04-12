# 🌦️ Weather Data API

A Flask-based REST API for accessing historical weather station data. Provides temperature records by station, date, and year.

## Features ✨

- **Multiple Endpoints**: Query by date, station, or year
- **JSON Responses**: Easy-to-consume data format
- **Station Catalog**: Browse available weather stations
- **Simple Integration**: RESTful interface

## API Endpoints 📡

| Endpoint | Description | Example |
|----------|-------------|---------|
| `/` | Homepage with station list | [Home](http://127.0.0.1:5000) |
| `/api/v1/<station>/<date>` | Temperature for specific station/date | [/api/v1/10/1988-10-25](http://127.0.0.1:5000/api/v1/10/1988-10-25) |
| `/api/v1/<station>` | All data for a station | [/api/v1/10](http://127.0.0.1:5000/api/v1/10) |
| `/api/v1/yearly/<station>/<year>` | All data for station/year | [/api/v1/yearly/10/1988](http://127.0.0.1:5000/api/v1/yearly/10/1988) |

## Installation 🛠️

1. Clone repository:
   ```
   git clone https:https://github.com/mihirpatil37/app_6_your_weather_api.git
   ```
2. Install dependencies:
    ```
   pip install flask pandas
   ```
3. Run the API:
    ```
   run app.py
   ```
## Data Structure 📂
    data_small/
    ├── stations.txt          # Station metadata
    └── TG_STAIDxxxxxx.txt    # Temperature data files (one per station)

## Example Response 🌡️
```text
    {
      "station": "10",
      "date": "1988-10-25",
      "temperature": 11.2
    }
```
## Development 🧑‍💻
- Built with Flask and Pandas
- Data files should be placed in data_small/
- Station IDs must be 6-digit padded (e.g., 10 → 000010)

## License 📄
- MIT License - Free for personal and commercial use