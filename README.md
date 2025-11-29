# 🍷 Wine Quality Prediction using MLflow and DAGsHub
### Getting started with MLFLOW Experiments
This project implements an Elastic Net regression model to predict the quality of red wine using physicochemical features, with experiment tracking and model versioning managed by MLflow on a remote DAGsHub server.

## 🚀 Getting Started

### 1. Prerequisites

Ensure you have a Conda environment and the required dependencies installed.

1.  **Create/Activate Environment (Optional, but Recommended):**
    ```bash
    conda activate <your_environment_name>
    ```

2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    # Assuming requirements.txt contains: mlflow, pandas, numpy, scikit-learn, dagshub
    ```

### 2. Authentication (Crucial Step)

To allow MLflow to write experiment data to the remote DAGsHub repository, you must set your credentials.

**You must generate a DAGsHub Access Token** from your DAGsHub user settings.

Set the following environment variables in your terminal **before running the script**:

| Variable | Value | Notes |
| :--- | :--- | :--- |
| `MLFLOW_TRACKING_USERNAME` | `ABHINAY945` | Your DAGsHub Username. |
| `MLFLOW_TRACKING_PASSWORD` | `<YOUR_DAGSHUB_TOKEN>` | **Replace with your actual token.** (e.g., `5a7cb830c6b1945f4e81b59fdd10fa1e7d35bb7d`) |

**Example Command (using Git Bash/Linux shell):**

```bash
export MLFLOW_TRACKING_USERNAME=ABHINAY945
export MLFLOW_TRACKING_PASSWORD=YOUR_DAGSHUB_TOKEN_HERE

Run the MLflow Experiment
Execute the main script (app.py). You can provide alpha and l1_ratio hyperparameters as arguments, or use the defaults (0.5 and 0.5).

Run with Defaults:
Bash
python app.py

Run with Custom Parameters (e.g., alpha=0.1, l1_ratio=0.8):
Bash
python app.py 0.1 0.8

***
📊 Results and Tracking
All experiment runs (parameters, metrics, and models) are logged to the remote MLflow Tracking Server hosted on DAGsHub:

Tracking URI: https://dagshub.com/ABHINAY945/Takein_MLFLOW.mlflow

You can view the results, compare runs, and access the registered model by navigating to your DAGsHub repository and clicking the MLflow tab.
***
