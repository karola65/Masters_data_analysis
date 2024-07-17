# Quantitive assessment for UK power networks

This Jupyter Notebook provides an analysis of electricity consumption data provided by UK Power Networks, with carbon data.
This is a result of the Master Thesis work.

## Prerequisites

Before you can run this notebook, you need to have the following installed:
- Python 3.x
- Jupyter Notebook or JupyterLab
- Pandas: `pip install pandas`
- NumPy: `pip install numpy`
- Matplotlib: `pip install matplotlib`
- Seaborn: `pip install seaborn`

## Getting Started

1. **Clone or download this notebook** to your local machine.
2. **Install the necessary libraries** mentioned in the Prerequisites section. If you are using Anaconda, most of these libraries might already be installed.

## Data Linking

To perform the analysis, you will need to establish a link to your own dataset. You can request access to the dataset from UK Power Networks at the following URL:

[UK Power Networks - Smart Meter Consumption Data](https://ukpowernetworks.opendatasoft.com/explore/dataset/ukpn-smart-meter-consumption-lv-feeder/information/)

### Steps to Access Data:
1. Visit the above link.
2. Register or log in to access the data.
3. Once registered, you can download the data in various formats (CSV, JSON, etc.).
4. Load the data into this notebook using Pandas. For example:

```python
import pandas as pd

# Replace 'path_to_file' with the path to the CSV file you downloaded
data = pd.read_csv('path_to_file.csv')
```
## Accessing Carbon Intensity Data

This analysis can be enriched by incorporating carbon intensity data, which indicates the amount of CO2 emitted per unit of electricity consumed. This data can be accessed through the Carbon Intensity API provided by the UK government.

### Steps to Access Carbon Intensity Data:
1. Visit the Carbon Intensity API website: [Carbon Intensity API](https://api.carbonintensity.org.uk/)
2. The API is public and does not require authentication, allowing you to make requests directly.
3. You can retrieve data directly using HTTP requests. Below is an example of how to use Python to make these requests and handle the response.

```python
import requests

# Make a GET request to fetch the current carbon intensity
response = requests.get('https://api.carbonintensity.org.uk/intensity')
data = response.json()

print(data)
```
