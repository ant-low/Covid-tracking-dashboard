[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ant-low/Covid-tracking-dashboard/HEAD?urlpath=%2Fdoc%2Ftree%2FCovid%2520Tracking%2520Dashboard.ipynb)

## Overview
This interactive dashboard tracks and visualizes COVID-19 case metrics across three major UK regions (North West, North East, and London). Built entirely in Python, it integrates live data from the UK Health Security Agency (UKHSA) API with static JSON fallbacks, allowing users to analyze daily case trends and monthly rolling averages dynamically.

<!-- If you took a screenshot, remove this comment and add it here: ![COVID-19 Dashboard](dashboard_screenshot.png) -->

## Key Data Analytics Features
* **Automated Data Pipelines:** Engineered a custom `APIwrapper` class to query the UKHSA REST API, featuring pagination handling, rate limiting, and dynamic URL parameter structuring.
* **Data Wrangling (Pandas):** 
  * Parsed and mapped nested JSON data into structured Pandas DataFrames.
  * Reindexed time-series data to fill missing date gaps (`.fillna()`).
  * Grouped rolling average data by month and calculated regional proportional shares using matrix division.
* **Interactive Visualization:** Designed a user interface using `ipywidgets` (dropdowns, radio buttons, callbacks) seamlessly integrated with `matplotlib` to toggle between linear/logarithmic scales and specific regions without reloading the application.

## Local Installation
To run this dashboard on your local machine:

1. Clone the repository:
   ```bash
   git clone [https://github.com/ant-low/covid-tracking-dashboard.git](https://github.com/ant-low/covid-tracking-dashboard.git)
   ```
2. Navigate to the directory and install the required dependencies:
   ```bash
   cd covid-tracking-dashboard
   pip install -r requirements.txt
   ```
3. Open the notebook in VS Code or Jupyter and run all cells.

## Project Structure
* `Hackathon Dashboard.ipynb`: The core application containing the API logic, data wrangling functions, and visual frontend.
* `requirements.txt`: The list of Python library dependencies.
* `*.json`: Six cached data files serving as immediate fallbacks, allowing the dashboard to render instantly before querying the live UKHSA API for updates.
