# Build an ML Pipeline for Short-Term Rental Prices in NYC
This project builds an end-to-end Machine Learning (ML) pipeline to estimate short-term rental prices
in New York City (NYC) based on similar properties. The pipeline is designed for a property management
company that rents out properties on various platforms and requires frequent model retraining.

The goal is to create a scalable and automated ML pipeline that ingests new data weekly, processes it, 
and updates the pricing model accordingly.

## Key Features
- **Automated Data Pipeline**: Handles weekly data updates and retrains the model
- **Feature Engineering & Preprocessing**: Cleans and transforms raw data
- **Model Training & Evaliuation**: Implements and tunes a Random Forest model
- **Experiment Tracking**: Utilizes MLflow and Weights & Biases for experiment logging
- **Configuarable & Modular Design**: Uses Hydra for parameter Management




### Setup

This project is compatible with the following operating systems:
- **Supported OS**:
  - **Ubuntu 22.04**
  - **macOS** - (latest versions)
- **Pyhon Version: 3.10**

## Instalation
1. Clone the Repository

```
git clone https://github.com/[your github username]/Project-Build-an-ML-Pipeline-Starter.git
```


### Create conda environment

```bash
> conda env create -f environment.yml
> conda activate nyc_airbnb_dev
```

### Log into Weights and Biases

```bash
> wandb login [your API key]
```



## Pipeline Execution
## Run Full Pipeline

```bash
>  mlflow run .
```
## Run Specific Steps
To run only selected steps (e.g. ``download`` and ``basic_cleaning``)

```bash
> mlflow run . -P steps=download,basic_cleaning
```

## Configuring Parameters
Override configuration parameters using Hydra syntax:

```bash
> mlflow run . \
  -P steps=download,basic_cleaning \
  -P hydra_options="modeling.random_forest.n_estimators=10 etl.min_price=50"
```

### Pre-existing components
This project integrates pre-implemented reusable components



## License

[License](LICENSE.txt)
