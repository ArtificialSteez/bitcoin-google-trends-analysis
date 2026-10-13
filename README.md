# Bitcoin Market Activity and Google Search Attention

**An econometric and machine-learning investigation of whether online search attention leads or follows Bitcoin market activity.**

## Overview

This project examines whether Google Trends search interest contains useful information about Bitcoin returns, trading volume and volatility. It analyses weekly Bitcoin market observations from **1 January to 31 December 2025**, alongside search interest in terms such as *Bitcoin*, *BTC Price*, *Crypto Crash* and *Buy Bitcoin*.

**Research question:** Does internet attention lead or lag Bitcoin market activity, and can it improve forecasting beyond information already contained in the market data?

## Approach

1. Obtain Bitcoin price and volume data via Yahoo Finance (`yfinance`) and Google Trends data via `pytrends`.
2. Clean, aggregate and align the market and search series at weekly frequency.
3. Explore trends and stationarity using ADF/KPSS tests, differencing, STL decomposition and ACF/PACF plots.
4. Examine lead-lag relationships using cross-correlations and bidirectional Granger-causality tests.
5. Compare market-only and attention-enhanced Random Forest models and investigate volatility using GARCH-based analysis.

## Main findings

- Search attention showed stronger lead-lag and predictive relationships with **trading volume** than with Bitcoin returns.
- Some short-run relationships were statistically detectable, but they did **not** translate into consistent out-of-sample improvements in return or volatility forecasting.
- Google Trends is better treated as a **supplementary indicator of market participation**, not a stand-alone Bitcoin trading signal.

These are results for this sample and research design; Granger causality does not establish economic causation.

## Repository contents

- `Lwazi Nhlapo.ipynb` — analysis and modelling notebook.
- `Reatile Seekoei & Lwazi Nhlapo .pdf` — executive report and interpretation.
- `Lwazi Nhlapo & Reatile Seekoei.pptx` — project presentation.

## Tools

Python, pandas, NumPy, Matplotlib, `yfinance`, `pytrends`, statsmodels, scikit-learn, SciPy and `arch`.

## Running the project

1. Open the notebook in JupyterLab or Google Colab.
2. Install the required Python libraries if they are not already available:
   ```bash
   pip install numpy pandas matplotlib scipy yfinance pytrends statsmodels scikit-learn arch
   ```
3. Run the notebook in order. External data retrieval depends on the availability of Yahoo Finance and Google Trends; their responses may change over time.
4. Review the figures and evaluation tables alongside the accompanying report.

## Limitations

The sample covers only one year and the analysis uses weekly data. Google search intensity measures attention, not sentiment or investor positions. Statistical associations are not evidence that searches cause Bitcoin price movements.

## Contributors

**Lwazi Nhlapo** and **Reatile Seekoei** — collaborative academic project.
