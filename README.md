# Space missions

Every rocket launch since 1957, poked at with pandas, seaborn and plotly. Yes, I know, a space-flavored EDA is a rite of passage for anyone learning data analysis. This is mine.

## Why it exists

A practice project from my data-analysis learning days. The goal was to run the full beginner loop on one dataset: look, clean, plot, repeat.

## Where the data comes from

The notebook reads the Kaggle dataset **All Space Missions from 1957** (`Space_Corrected.csv`). The CSV is **not** in this repo, so grab it from Kaggle first. The notebook can also be opened directly on Kaggle through the badge at the top of the notebook, where the data is already mounted.

## How to run it

```bash
pip install -r requirements.txt
jupyter lab space-misions.ipynb
```

Then change `file_path` in the first data cell to wherever you saved the CSV (it currently points at the Kaggle path `/kaggle/input/...`).

## What is in here

- `space-misions.ipynb`: the whole analysis (yes, "misions" has a typo in the file name; I kept it so old links don't break)
- `requirements.txt`: the libraries the notebook imports

## What the notebook does

1. Loads 4,324 launches and checks the basics (types, nulls, duplicates).
2. Cleans up: strips stray whitespace from column names, drops two junk index columns, turns the odd "Rocket" column into a numeric `Mission Cost`, and splits the date, time and time zone out of the messy `Datum` column.
3. Plots missions per company, once with seaborn and once with an interactive plotly chart.
4. Ends with a note about a small Power BI dashboard I built on the same data (the dashboard itself is not part of this repo).

## A small insight

The Soviet-era `RVSN USSR` has by far the most launches in the dataset: 1,777, versus 279 for Arianespace in second place. The Cold War was busy.

## What I learned

Real-world data is never as tidy as the tutorial version: stray spaces in column names, dates crammed into one text column and a cost column that is mostly empty (3,360 of 4,324 values are missing). Cleaning takes more time than plotting, and that is normal.

## Heads-up

- No license file yet, so by default all rights are reserved. If you want to reuse something, open an issue.
- I have not re-run the notebook after tidying the repo.
