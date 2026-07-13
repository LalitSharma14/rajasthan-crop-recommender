# Rajasthan Crop Recommender

An interview-ready machine learning project that will combine Rajasthan crop-production history, weather, and anonymized soil-test measurements.

## Phase 1

While the Soil Health Card request is pending, we will:

1. learn how Jupyter notebooks execute Python;
2. collect and audit official crop-production data;
3. define units and validation rules;
4. explore Rajasthan crops by district and season;
5. prepare a weather-data join;
6. build a leakage-safe baseline model.

## Start in VS Code

1. Open this folder in VS Code.
2. Open a terminal in this folder.
3. Create and activate `.venv`.
4. Install `requirements.txt`.
5. Open `notebooks/00_setup_and_first_steps.ipynb`.
6. Select the `.venv` Python kernel.
7. Run cells from top to bottom.

Commands for PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

In the notebook, click **Select Kernel**, choose **Python Environments**, and select `.venv\Scripts\python.exe`.

## Data policy

- `data/raw/`: unchanged source files.
- `data/interim/`: partially cleaned files.
- `data/processed/`: model-ready files.
- Never commit farmer names, phone numbers, survey numbers, full addresses, or exact personal land identifiers.
- Never overwrite a raw source file; cleaning must create a new file.
