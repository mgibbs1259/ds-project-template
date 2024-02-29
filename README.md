# DS Project Template

# Docker Development Environment

This repository provides a Docker-based development environment for your project. Follow the steps below to set up and start developing inside a Docker container using VSCode.

## Prerequisites

Make sure you have the following installed on your machine:

-    Docker
-    Visual Studio Code
-    VSCode Dev Containers extension

## Getting Started

1. Clone this repository to your local machine.
2. Open the project in VSCode.
3. VSCode will detect the presence of a .devcontainer folder and suggest to reopen the project in a container. Click "Reopen in Container" when prompted.
4. Wait for VSCode to build the Docker image and start the container. This might take a few minutes on the first run.
5. Once the container is running, you are now inside the development environment. You can see the terminal is now running inside the container.

## Customization

If you need to customize the Docker development environment, modify the .devcontainer/devcontainer.json, the Dockerfile.dev, or the requirements.txt. After making changes, restart the container to apply the modifications.

# Structure

```
├── .devcontainer <- Folder for storing development container configuration files.
│
├── data
│ ├── interim <- Intermediate data that has been transformed.
│ ├── processed <- The final, canonical data sets for modeling.
│ └── raw <- The original, immutable data dump.
│
├── models <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks <- Jupyter notebooks. Naming convention is a number (for ordering),
│   the creator's initials, and a short `-` delimited description, e.g.
│   `1.0-mg-initial-data-exploration`.
│
├── src <- Source code for use in this project.
│ ├── **init**.py <- Makes src a Python module
│ │
│ ├── data <- Scripts to download or clean data
│ │ └── generate_dataset.py
│ │
│ ├── features <- Scripts to turn data into features for modeling
│ │ └── generate_features.py
│ │
│ ├── models <- Scripts to train and evaluate models
│ │ ├── train_models.py
│ │ └── evaluate_models.py
│ │
│ └── visualization <- Scripts to create exploratory and results oriented visualizations
│ │ └── generate_visualizations.py
│
├── tests <- Tests for the source code used in this project.
│   Run using: pytest.
│
├── .example-env <- Example environment file for setting up your project environment.
│   Create a .env file based on this and fill out appropriate variables.
│
├── .gitignore <- File to specify intentionally untracked files to ignore.
│
├── Dockerfile.dev <- The Dockerfile for reproducing the analysis environment.
│
├── main.py <- The main file for running a Python API using FastAPI.
│   Run using: uvicorn main:app --host 0.0.0.0 --port 5000 --reload.
│
├── README.md <- The top-level README for developers using this project.
│
├── requirements.txt <- The requirements file for reproducing the analysis environment.
│
├── run_pipelines.py <- The main file for running data, feature, and model pipelines.
```
