# Monsoon (JJAS) Rainfall over Kerala from NASA IMERG

Analysis of the 2020 southwest monsoon season (June-September) over the Kerala region, southwest India, using NASA GPM IMERG Final Run daily precipitation.

## What the notebook does

1. Downloads daily IMERG files for June-September 2020 (only if they are not already saved locally).
2. Crops the data to the study region (72-79°E, 7-14°N) and runs basic quality checks (number of days, value range, missing data).
3. Saves the cropped data as a NetCDF file.
4. Produces three plots:
   - a map of seasonal total rainfall (where the rain fell),
   - a time series of area-mean daily rainfall (when it fell),
   - monthly totals (how the season built up and faded).

## Data

- Product: GPM IMERG Final Run, daily, version 07 (`GPM_3IMERGDF`)
- Source: NASA Earthdata (GES DISC)
- Units: mm/day for daily values, mm for totals

## How to run

1. Create a free [NASA Earthdata](https://urs.earthdata.nasa.gov/) account.
2. Install the requirements:
   ```
   pip install -r requirements.txt
   ```
3. Open `imerg_kerala_monsoon_rainfall.ipynb` in Jupyter and run all cells. The first run asks for your Earthdata login and downloads the data into `data/raw/imerg`. Later runs skip the download.

To analyse a different year, change `YEAR` in the settings cell.

## Main findings (2020)

- Rainfall is strongly controlled by geography: the highest seasonal totals occur along the Western Ghats, and totals fall steadily to the east.
- July is the wettest month and August the driest, because a long monsoon break in the second half of August outweighs the season's strongest single spell in early August.

## Files

- `imerg_kerala_monsoon_rainfall.ipynb`: the analysis notebook
- `requirements.txt`: Python packages needed
