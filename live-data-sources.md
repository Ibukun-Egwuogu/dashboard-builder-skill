# Live & Open Data Sources

Free, public data APIs and datasets for building dashboards with real, live data.
All sources listed here have free tiers or are fully open.

---

## Global Health & Public Health

### WHO Global Health Observatory (GHO)
- **URL**: https://ghoapi.azureedge.net/api/
- **What**: Health indicators for 194 countries — disease incidence, mortality, intervention
  coverage, health system metrics
- **Format**: REST JSON — no API key required
- **Use cases**: Malaria dashboard, disease trend analysis, healthcare coverage comparison
- **Sample call**: `GET https://ghoapi.azureedge.net/api/Indicator` to list all indicators
- **Good for**: Disease case trends, vaccination rates, maternal health, cause of death

### Our World in Data (GitHub mirror)
- **URL**: https://github.com/owid/owid-datasets
- **What**: Curated CSV datasets on health, energy, poverty, education, climate — all
  cleaned and ready to use
- **Format**: CSV files (direct download)
- **Use cases**: Long-term trend dashboards, cross-country comparisons, development indicators
- **Good for**: Portfolio projects needing clean, citation-quality data

---

## Economics & Finance

### World Bank Open Data
- **URL**: https://api.worldbank.org/v2/
- **What**: Economic and development data for every country — GDP, poverty, trade, education,
  infrastructure
- **Format**: REST JSON — no API key required
- **Use cases**: Economic development dashboard, poverty analysis, infrastructure comparison
- **Sample call**: `GET https://api.worldbank.org/v2/country/NG/indicator/NY.GDP.MKTP.CD?format=json`
  (Nigeria GDP over time)
- **Good for**: Finance, government policy, agriculture, education portfolios

### Frankfurter Exchange Rates
- **URL**: https://api.frankfurter.app/
- **What**: Real-time and historical currency exchange rates (ECB data)
- **Format**: REST JSON — no API key required
- **Use cases**: FX dashboard, NGN/USD/GBP trend tracker, international pricing analysis
- **Sample calls**:
  - Latest rates: `GET https://api.frankfurter.app/latest?from=USD`
  - Historical: `GET https://api.frankfurter.app/2020-01-01..2024-12-31?from=NGN&to=USD`
- **Good for**: Finance, e-commerce, logistics cost dashboards

### Alpha Vantage (Stock Market)
- **URL**: https://www.alphavantage.co/
- **What**: Real-time and historical stock prices, forex, crypto, economic indicators
- **Format**: REST JSON — free API key (500 requests/day free)
- **Use cases**: Investment portfolio dashboard, stock performance tracker, sector comparison
- **Good for**: Finance, retail investor analytics

### Open Exchange Rates
- **URL**: https://openexchangerates.org/
- **What**: 170+ currency exchange rates, historical data
- **Format**: REST JSON — free tier available
- **Good for**: International sales, supply chain cost tracking

---

## Climate & Environment

### Open-Meteo
- **URL**: https://api.open-meteo.com/
- **What**: Free weather and climate API — temperature, precipitation, wind, solar radiation
  for any location, historical back to 1940
- **Format**: REST JSON — no API key required
- **Use cases**: Agricultural weather impact, energy demand forecasting, logistics weather risk
- **Sample call**: `GET https://api.open-meteo.com/v1/forecast?latitude=6.45&longitude=3.39&hourly=temperature_2m`
  (Lagos weather forecast)
- **Good for**: Agriculture, energy, transportation, logistics

### Global Carbon Project / Our World in Data
- **URL**: https://github.com/owid/co2-data
- **What**: CO2 and greenhouse gas emissions by country, 1750–present
- **Format**: CSV — direct download
- **Good for**: Energy, government policy, ESG dashboards

---

## African & Nigeria-Specific

### NBS (National Bureau of Statistics Nigeria)
- **URL**: https://nigerianstat.gov.ng/
- **What**: Nigeria economic, demographic, trade, agricultural data
- **Format**: Excel/CSV downloads — no API, but consistent structure
- **Good for**: Nigerian economic dashboards, state-level comparisons

### CBN (Central Bank of Nigeria) Data
- **URL**: https://www.cbn.gov.ng/rates/
- **What**: Exchange rates, inflation, monetary policy rates
- **Format**: Manual download — updated regularly
- **Good for**: NGN/USD tracker, inflation dashboard, monetary policy analysis

### Africa CDC Open Data
- **URL**: https://africacdc.org/
- **What**: Disease surveillance, outbreak data, vaccination coverage across Africa
- **Format**: Reports + downloadable datasets
- **Good for**: Public health, malaria, COVID, epidemic response dashboards

---

## Demographics & Social

### UN Population Division
- **URL**: https://population.un.org/wpp/
- **What**: World population data by country, age group, urban/rural split, projections to 2100
- **Format**: Excel/CSV downloads
- **Good for**: Healthcare demand, education, infrastructure planning dashboards

### UNICEF Data
- **URL**: https://data.unicef.org/
- **What**: Child mortality, malnutrition, education, water/sanitation, protection
- **Format**: API + CSV downloads
- **Good for**: NGO dashboards, public health, social impact analysis

---

## Transport & Logistics

### NYC Open Data (good for taxi/transport portfolio projects)
- **URL**: https://data.cityofnewyork.us/
- **What**: NYC taxi trips, Citi Bike, subway usage, road incidents
- **Format**: REST API + CSV — free, no key required
- **Good for**: Transportation analytics, route analysis, demand pattern projects

### OpenSky Network (Flight data)
- **URL**: https://opensky-network.org/apidoc/
- **What**: Live and historical flight data — departure, arrival, delays, airline performance
- **Format**: REST JSON — free tier
- **Good for**: Airline/airport performance dashboards, delay analysis

---

## Retail & E-commerce

### Kaggle Open Datasets (static, but excellent quality)
- **URL**: https://www.kaggle.com/datasets
- **Notable sets**: Brazilian E-commerce (Olist), UK Online Retail, Amazon product reviews,
  Superstore Sales
- **Format**: CSV
- **Good for**: Sales, customer segmentation, RFM analysis, churn dashboards

---

## Using Live APIs in Dashboards

### Power BI
Connect via: Home → Get Data → Web → enter API URL
For JSON APIs: use Power Query to parse the response
Schedule refresh: Power BI Service → Dataset settings → Scheduled refresh

### Tableau
Connect via: Connect → Web Data Connector or JSON file
Use Tableau Prep for API transformations

### Python/SQL pipelines feeding Power BI / Tableau
```python
import requests
import pandas as pd

# Exchange rate example
r = requests.get("https://api.frankfurter.app/latest?from=USD&to=NGN,GBP,EUR")
data = r.json()
df = pd.DataFrame(data['rates'].items(), columns=['Currency', 'Rate'])
```

### Refreshing live data
- Frankfurter, Open-Meteo, WHO: safe to call daily or more frequently
- Alpha Vantage: respect rate limits (5 calls/min free tier)
- World Bank: data updated annually — daily refresh unnecessary
- Always add "Data as of [datetime]" from the API response, not from your system clock
