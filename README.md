# Spitcast API Documentation

Welcome to the Spitcast API. This API provides surf forecasts and ocean condition data for California surf spots. It includes data sourced from NOAA and Spitcast's proprietary forecast engine.

---

## Endpoints

### 🌊 Surf Spots

Get a (growing) list of California surf spots for which Spitcast provides forecasts.

**Endpoint:**  
`https://api.spitcast.com/api/spot`

---

### 📈 Surf Forecast

Get Spitcast's surf forecast for a specific spot and date. Forecasts include wave height and shape quality.

**Endpoint Format:**  
`https://api.spitcast.com/api/spot_forecast/{spot_id}/{year}/{month}/{day}`

**Example:**  
`https://api.spitcast.com/api/spot_forecast/1/2025/3/14`

**Shape Values:**
- `0.0` = Poor  
- `0.5` = Poor-Fair  
- `1.0` = Fair  
- `>1.0` = Good

---

### 🌊 Swell Forecast

NOAA WAVEWATCH III data, regionally parsed by county. Shows offshore swell forecasts.

**Endpoint Format:**  
`https://api.spitcast.com/api/buoy_ww3/{county_id}/{year}/{month}/{day}`

**Example:**  
`https://api.spitcast.com/api/buoy_ww3/1/2025/3/14`

[About WAVEWATCH III](https://polar.ncep.noaa.gov/waves/wavewatch/)

---

### 💨 Wind Forecast

Wind forecast data sourced from NOAA’s National Digital Forecast Database.

**Endpoint Format:**  
`https://api.spitcast.com/api/buoy_ndfd/{county_id}/{year}/{month}/{day}`

**Example:**  
`https://api.spitcast.com/api/buoy_ndfd/1/2025/3/14`

[NDFD Info](https://graphical.weather.gov/)

---

### 🌊 Tide Forecast

Tide prediction data from NOAA's Tides & Currents.

**Endpoint Format:**  
`https://api.spitcast.com/api/buoy_tide/{county_id}/{year}/{month}/{day}`

**Example:**  
`https://api.spitcast.com/api/buoy_tide/1/2025/3/14`

[NOAA Tides & Currents](https://tidesandcurrents.noaa.gov/)

---

### 🌡️ Current Water Temperature

Water temperature data from NOAA's National Data Buoy Center.

**Endpoint Format:**  
`https://api.spitcast.com/api/buoy_ndbc/{county_id}/{year}/{month}/{day}`

**Example:**  
`https://api.spitcast.com/api/buoy_ndbc/1/2025/3/14`

[NDBC Info](https://www.ndbc.noaa.gov/)

---

## Terms of Use

1. **Use at your own risk**  
   Uptime isn't guaranteed, and the API structure may change from time to time.

2. **Forecasts aren’t perfect**  
   Surf forecasting is inherently uncertain. The model is under ongoing development to improve accuracy.

3. **Please give credit**  
   If you're using Spitcast data publicly, a simple attribution is appreciated.

4. **Don't use the Spitcast name**  
   If you're building something public-facing (like an app), please don’t name it Spitcast. Use your own branding and mention it’s powered by Spitcast.

5. **Share what you build**  
   I’d love to see how you use this data. Feel free to reach out or share your projects!
