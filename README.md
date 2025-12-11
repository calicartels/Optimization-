# Milk Bank Collection Optimization

This project optimizes milk collection routes for the Oklahoma Mothers' Milk Bank (OMMB). It analyzes donation data to prioritize pickups and solves a Traveling Salesman Problem (TSP) to minimize travel time for the bank's driver.

## Business Report

[View the Business Report](https://docs.google.com/document/d/13bn-2qQkkbQ64d277w0MfLUxbD0VZrCPLaTarOvW4VU/edit?tab=t.0#heading=h.i9dnovd114ss)

## Problem Description

The OMMB operates a network of 36 depots. A single driver collects frozen breast milk with the following constraints:
- Freezer capacity is approximately 1,000 oz.
- Maximum daily driving limit is 12 hours.
- Objective is to minimize total travel time while ensuring necessary depots are visited.

## Methodology

The solution involves:
1. **Data Analysis**: Cleaning and analyzing 2023-2024 deposit transactions to determine per-depot daily fill rates.
2. **Route Optimization**: Formulating the collection routes as a TSP. Two primary routes are optimized:
   - **Local Route**: OKC Metro area (HQ + 8 depots).
   - **Tulsa Route**: Tulsa area (HQ + 6 depots).
   - The remaining 22 depots are serviced via courier shipping.
3. **Mathematical Model**: Uses integer programming with Miller-Tucker-Zemlin subtour elimination constraints to guarantee valid routes.

## Project Structure

- `case_study_final.ipynb`: Main Jupyter notebook containing data cleaning, exploratory analysis, depot prioritization, and the routing heuristic implementation.
- `latex/`: Directory containing project documentation:
  - `formulization.tex`: LaTeX source detailing the mathematical formulation of the optimization model.
  - `Optimization___Final_Project_Template.pdf`: Final project documentation file.
- `data/`: Directory containing input datasets:
  - `Deposits Transactions 2023 2024.xlsx`: Historical donation records.
  - `Depot Information.xlsx`: Metadata for each depot.
  - `Optional - Driving Distance and Time.xlsx`: Distance matrix between locations.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn

## Usage

1. Ensure the data files are located in the `data/` directory.
2. Open `case_study_final.ipynb` in a Jupyter environment.
3. Run all cells to execute the analysis and generate routing recommendations.

## Author

Sansa & Vishnu
