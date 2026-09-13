# Data Files

This folder contains the datasets used in the FPPpy lab notebooks.

## Source / Copyright Notice

All datasets are sourced from or derived from:

> **Forecasting: Principles and Practice (Python Edition)**  
> Rob J Hyndman, George Athanasopoulos, et al.  
> Online textbook: <https://otexts.com/fpppy/>

The data are distributed here solely for educational use in the
**Graduate Forecasting Course** at Chung-Ang University.
Please refer to the original textbook for authoritative descriptions
of each dataset.

## Loading Data in Google Colab

### Option A — read directly from GitHub (recommended)

```python
import pandas as pd

BASE = "https://raw.githubusercontent.com/bcseong2/fpppy-labs/main/data/"

# Examples
pbs      = pd.read_csv(BASE + "pbs.csv",      parse_dates=["Month"])
aus_prod = pd.read_csv(BASE + "aus_production.csv")
```

### Option B — download the zip and extract

```python
import zipfile, io, requests, pandas as pd

url = "https://raw.githubusercontent.com/bcseong2/fpppy-labs/main/data/fpppy_data.zip"
r = requests.get(url)
with zipfile.ZipFile(io.BytesIO(r.content)) as z:
    z.extractall("data")

pbs = pd.read_csv("data/pbs.csv", parse_dates=["Month"])
```

## Files

| File | Description |
|------|-------------|
| `AirPassengers.csv` | Monthly airline passengers 1949–1960 |
| `EPF_FR_BE.csv` | Electricity price forecasting (France & Belgium) |
| `EPF_FR_BE_futr.csv` | Future covariates for EPF dataset |
| `EPF_FR_BE_static.csv` | Static features for EPF dataset |
| `PBS_unparsed.csv` | PBS (raw dates as strings) |
| `USAccDeaths.csv` | US accidental deaths 1973–1978 |
| `US_change.csv` | US macroeconomic quarterly changes |
| `algeria_exports.csv` | Algeria exports |
| `anscombe.csv` | Anscombe's quartet |
| `ansett.csv` | Ansett Airlines weekly economy passengers |
| `aus_accomodation.csv` | Australian accommodation data |
| `aus_airpassengers.csv` | Australian air passengers |
| `aus_arrivals.csv` | International arrivals to Australia |
| `aus_economy.csv` | Australian economic indicators |
| `aus_livestock.csv` | Australian livestock counts |
| `aus_production.csv` | Australian quarterly production |
| `aus_retail.csv` | Australian retail trade |
| `aus_tourism.csv` | Australian tourism |
| `austa.csv` | Total international visitors to Australia |
| `bank_calls.csv` | Bank call centre half-hourly data |
| `boston_marathon.csv` | Boston Marathon winning times |
| `canadian_gas.csv` | Canadian gas production |
| `chinese_gdp.csv` | China annual GDP |
| `cowtemp.csv` | Cow body temperature |
| `eggs.csv` | Annual egg prices |
| `electricity_future_vars.csv` | Electricity future variables |
| `electricity_short.csv` | Short electricity dataset |
| `fpppy_data.zip` | **All files bundled** (download once) |
| `gafa_stock.csv` | GAFA (Google/Apple/Facebook/Amazon) stock prices |
| `global_economy.csv` | Global economic indicators |
| `guinea_rice.csv` | Guinea rice production |
| `hsales.csv` | US monthly housing sales |
| `insurance.csv` | Insurance quotes and TV ads |
| `labour.csv` | Australian labour force |
| `lake_huron.csv` | Level of Lake Huron |
| `mink.csv` | Mink population |
| `olympic_running_unparsed.csv` | Olympic running times |
| `pbs.csv` | Pharmaceutical Benefits Scheme (Australia) |
| `pedestrian.csv` | Melbourne pedestrian sensor counts |
| `pelt.csv` | Pelt trading records (Hudson Bay) |
| `prison.csv` | Australian prison population |
| `prison_population.csv` | Prison population (extended) |
| `strikes.csv` | US strikes |
| `total_cost_df.csv` | Total cost data |
| `tourism.csv` | Australian tourism (long format) |
| `tourism.xlsx` | Australian tourism (Excel format) |
| `tute1.csv` | Tutorial dataset 1 |
| `us_employment.csv` | US employment by sector |
| `us_gasoline.csv` | US gasoline prices |
| `us_total.csv` | US total employment |
| `ustreas.csv` | US treasury bill rates |
| `vic_elec.csv` | Victoria electricity demand |
| `www_usage.csv` | Internet usage per minute |
