# Airwise

[Open the live website](https://yatish-as.github.io/airwise-weather/)

Airwise is a light, weather-first dashboard for forecasts, air quality, WeatherGPT, interactive maps, alerts, and climate analysis. It is a static HTML app with no build step.

## Open the website

Use the hosted HTTPS link above for the easiest access.

For a local copy, open the `outputs` folder and double-click `start-airwise.cmd`. It starts a local web server at `http://127.0.0.1:8765/` and opens the site in your browser. Keep the command window open while using it. Do not open `index.html` directly: a `file://` page has no web origin, so Puter cannot sign in.

## Data and maps

- Weather and forecasts: [Open-Meteo Forecast API](https://open-meteo.com/en/docs).
- Air-quality pollutants and US AQI: [Open-Meteo Air Quality API](https://open-meteo.com/en/docs/air-quality-api), including CAMS model data.
- Place lookup: [Open-Meteo Geocoding API](https://open-meteo.com/en/docs/geocoding-api).
- The interactive basemap uses MapLibre GL JS and OpenFreeMap tiles, with OpenMapTiles and OpenStreetMap attribution. It does not use Google Maps or require Google Maps billing.
- AQI and weather map shading is interpolated from model samples across the visible area.

Weather and air-quality results are model estimates, not street-level sensor readings. The global CAMS air-quality grid is about 45 km resolution (about 11 km in Europe). Use a nearby calibrated monitor for curbside conditions and official local guidance for emergencies.

## WeatherGPT and voice

WeatherGPT uses Puter.js with the lightweight GPT-5.4 Nano model and live weather context. Puter may ask visitors to sign in; its AI service may charge the account they connect. The microphone uses browser/provider speech recognition, and the speaker uses browser text-to-speech. Language and voice availability depend on the device.

## Personal progress and alerts

Progress is stored in the browser and does not sync between devices. Forecast-based alerts are informational estimates, not official warnings. Browser notifications work only after permission is granted and while the site is open.

Map tiles are provided under [OpenFreeMap's terms](https://openfreemap.org/tos/). Open-Meteo data use is subject to its [terms](https://open-meteo.com/en/terms).
