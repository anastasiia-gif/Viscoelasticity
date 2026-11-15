# Viscoelasticity — Material Test Data Analysis

Python analysis of force–strain–time measurements from a **viscoelasticity practical**: cleaning raw instrument data, filtering, curve fitting and visualization of the material response.

## What it does

The raw export (`csv_data.csv`) comes straight from the test setup in European number format (semicolon-separated, decimal commas). The scripts:

1. **Parse and clean** the CSV — delimiter/decimal conversion, stripping artifacts, NaN checks
2. **Filter** the signals (Gaussian smoothing) to remove measurement noise
3. **Fit models** to the data with `scipy.optimize.curve_fit` and linear regression
4. **Plot** force, strain and the fitted curves over time

## Scripts

| Script | Purpose |
|---|---|
| `visualize_data.py` | Plot the raw measurement data |
| `visualize_filter_data.py` | Plot the data after noise filtering |
| `regression.py` | Curve fitting of the viscoelastic response |
| `linear_regression.py` | Linear regression on the (near-)linear regions |

## Running

```bash
pip install pandas numpy scipy matplotlib
python visualize_data.py
```

The `Viscoelasticity practical` document describes the experiment itself.
