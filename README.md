# Vaex-Big-Data-Analytics-for-Airline-data

A Python notebook (ipynb) created in Jupyter Notebook, which utilizes the Vaex library for Big Data Analytics of an Airline dataset.

**Author**: Nikolas Petrou, MSc in Data Science

## Overview
The main part of the work focuses on the exploration a big dataset of 17 GB. Specifically, the dataset contains information on flights within the United States between 1988 and 2018. It can be directly downloaded from: [vaex.s3.us-east-2.amazonaws.com](https://vaex.s3.us-east-2.amazonaws.com/airline/us_airline_data_1988_2018.hdf5).

In addition, in this project the Out-of-Core DataFrames Python library [Vaex](https://vaex.io/docs/index.html) is employed, in order to visualize, explore acalculate statistics of this big tabular dataset.

The goal of this project is to utilize [Vaex](https://vaex.io/docs/index.html) to perform an Exploratory Data Analysis (EDA), as well as to predict the arrival delay of a flight (regression task).


## What is Vaex and why Vaex?

[Vaex](https://vaex.io/docs/index.html) is a Python library for lazy Out-of-Core DataFrames (similar to _Pandas_), to visualize and explore big tabular datasets. It can calculate statistics such as mean, sum, count, standard deviation etc, on an N-dimensional grid up to a billion (10^9) objects/rows per second. Visualization is done using histograms, density plots and 3d volume rendering, allowing interactive exploration of big data. Furthermore, _Vaex_ provides [wrappers](https://vaex.io/docs/example_ml_iris.html) to powerful libraries for predictive models (e.g. _Scikit-learn_, _xgboost_) and make them work efficiently with _Vaex_. _Vaex_ does implement a variety of standard data transformers (e.g. PCA, numerical scalers, categorical encoders) and a very efficient KMeans algorithm that take full advantage. Finally, _Vaex_ uses memory mapping, a zero memory copy policy, and lazy computations for best performance (no memory wasted).

#### Advantage of using Vaex over using Pandas with a more powerful machine 
Switching to a more powerful machine (with more RAM and/or better CPU) may solve some memory issues, but still, _Pandas_ will only use one out of the 32 cores of your fancy machine. With _Vaex_, **all operations are out of the core and executed in parallel** and lazily evaluated, allowing for crunching through a billion-row dataset effortlessly.


## Data
The dataset has a relatively big size (17 GB), and contains information on flights within the United States between 1988 and 2018. It can be directly downloaded from: [vaex.s3.us-east-2.amazonaws.com](https://vaex.s3.us-east-2.amazonaws.com/airline/us_airline_data_1988_2018.hdf5)

Each row-record of the dataset represents an individual flight. Specifically, each record contains information of the airline (UniqueCarrier), airports (origin airport, destination airport) and flight level information such as time schedule (day of week, day of month, month, year), flight distance, departure time and delay, arrival time and delay.
