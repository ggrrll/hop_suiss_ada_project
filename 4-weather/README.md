# Weather

This directory contains Python scripts used to fetch weather data for the dates
contained in the full dataset, and store them as CSV data.

The file [`weather.py`](weather.py) is the core module that performs the
requests to [the API](https://developer.worldweatheronline.com), and is used in
the wrapper script [`weather_utils.py`](weather_utils.py) that can be launched from command line.
