# COVID-19 SEIR Model

This repository contains a Jupyter notebook that implements a modified SEIR (Susceptible, Exposed, Infected, Recovered) epidemiological model to predict COVID-19 spread with consideration for immunity decay.

Link to [deck](https://docs.google.com/presentation/d/1yt59Hk_VmX83pHDD_Ftqbc7kNfxiRJXX1X7TCHhiWUc/edit#slide=id.g31d6bd9a6ad_0_12)


## Overview

The model consists of two main parts:

1. **Parameter Optimization**: Uses real COVID-19 data from Johns Hopkins University to optimize the parameters (beta, sigma, gamma) for the standard SEIR model
2. **Immunity Decay Model**: Extends the standard SEIR model by incorporating a time-varying tau parameter that models waning immunity over time

## Mathematical Model

The model uses a system of differential equations to simulate the dynamics of disease spread:

- **S**: Susceptible population
- **E**: Exposed (infected but not yet infectious)
- **I**: Infectious population
- **R**: Recovered/removed population

The immunity decay component allows recovered individuals to become susceptible again after some time (controlled by the tau parameter), which more accurately represents the real-world dynamics of COVID-19 immunity.

## Requirements

To run this notebook, you'll need:

- Python 3.x
- NumPy
- Pandas
- SciPy
- Matplotlib
- Jupyter Notebook or JupyterLab

## Data Source

The model uses COVID-19 data from the Johns Hopkins University CSSE repository:
- https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv

## License

[MIT License](LICENSE)

## Citation

If you use this model in your research, please cite this repository and the original Johns Hopkins COVID-19 data source.
