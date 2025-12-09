# Seattle Traffic Congestion Study

## Project Description

The main question of this project is:

Can we forecast one-hour-ahead traffic volume along Interstate 5 within Seattle using traffic sensor data, temporal patterns, weather conditions, and collision records?

Short-term traffic forecasting supports several transportation objectives:

* Proactive traffic management, including adaptive ramp metering and variable speed limits
* Improved traveler information and rerouting guidance
* Better emergency response and resource allocation
* Reduced congestion-related delay and secondary incidents

Seattle experiences recurring congestion on I-5, making short-term forecasting valuable for transportation agencies and planners.

## Project Overview

This project integrates multiple real-world data sources into a continuous hourly time series and evaluates three forecasting models:

1. Lagged linear regression
2. XGBoost regressor
3. Prophet time-series model with seasonal structure and external regressors

The models are evaluated on a chronologically held-out test period using MAE and RMSE.

XGBoost provides the best predictive accuracy, the linear regression model serves as a useful benchmark, and Prophet offers insight into seasonal patterns.


## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Python Dependencies
└── README.md             # Project documentation
```


## Data
Traffic volume
https://wsdot.wa.gov/about/transportation-data/travel-data/traffic-count-data

Weather data
https://www.ncei.noaa.gov/

Collision data
https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::sdot-collisions-all-years/explore

## Analysis

### Phase I — Data Engineering and EDA

* Standardize timestamps, including resolving 24:00 formatting
* Build a continuous hourly index
* Merge traffic, weather, and collision datasets
* Produce exploratory plots for daily and weekly patterns, weather effects, and collision frequency

### Phase II — Predictive Modeling

Three models are implemented:

Lagged linear regression
A simple and interpretable benchmark using previous-hour volumes and engineered features.

XGBoost regressor
A nonlinear model that captures interactions among lagged volume, weather variables, and temporal structure.
Produces the lowest MAE and RMSE of all models.

Prophet model
Configured with daily and weekly seasonality and external regressors.
Useful for structural interpretation but less accurate for short-term fluctuation.

### Phase III — Results

* XGBoost performs best for operational short-term forecasting
* Linear regression provides a solid baseline
* Prophet offers meaningful seasonal structure but higher error
* Visualizations illustrate actual versus predicted traffic and the influence of weather and collisions


## Results

The accompanying Jupyter notebook includes:

* Comparative error metrics
* Actual versus predicted volume plots
* Multi-axis time-series overlays
* Prophet trend and seasonality decomposition
* XGBoost feature importance analysis

---

## Authors

- Hannah Belville - [@belvilleh](https://github.com/belvilleh)
- Cong Ho - [TheCong07](https://github.com/TheCong07)
- Paul Skentzos - [@gpskentzos](https://github.com/gpskentzos)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Data sets: 

	- https://wsdot.wa.gov/about/transportation-data/travel-data/traffic-count-data
	- https://www.ncei.noaa.gov/
	- https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::sdot-collisions-all-years/explore

- Tutorials or papers referenced
	- https://www.youtube.com/watch?v=sTwwiuIKEeg
	- https://www.microsoft.com/en-us/research/project/predictive-analytics-for-traffic/

- Inspiration or collaborators
	- Seattle University DATA 5100 Course
