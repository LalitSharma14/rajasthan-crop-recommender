# Rajasthan Crop Recommendation System

A machine learning project that aims to recommend suitable crops for a location in Rajasthan using soil nutrients, soil properties, weather, district, and growing season.

> **Current status:** Project environment and folder structure are ready. Data collection and model development have not started yet. Access to detailed Rajasthan Soil Health Card data has been requested from the relevant government authority.

## Problem statement

Farmers need to choose crops that suit their local soil and climate. The final system will accept values such as nitrogen, phosphorus, potassium, pH, rainfall, temperature, district, and season, then return suitable crop recommendations.

This will be a decision-support and learning project, not a replacement for advice from agricultural experts.

## Why Rajasthan?

The first version is limited to one state so that district names, seasons, weather records, crops, and soil measurements can be validated consistently. A Rajasthan-specific model is also more realistic than claiming that one small dataset represents all of India.

## Planned data

| Data | Example fields | Why it is needed |
|---|---|---|
| Soil Health Card data | Nitrogen (N), phosphorus (P), potassium (K), pH, EC, organic carbon | Describes soil fertility and condition |
| Crop-production data | District, year, season, crop, area, production | Shows which crops have historically been grown successfully |
| Weather data | Rainfall and temperature | Represents the climate conditions required by different crops |

Only official or clearly documented sources will be used. Personal farmer information and exact land identifiers will not be stored in this public repository.

## Planned machine learning workflow

1. Collect and document the data sources.
2. Inspect columns, units, missing values, and duplicate records.
3. Clean district, crop, and season names without changing raw files.
4. Join soil, crop-production, and weather records at compatible geographic and time levels.
5. Explore crop patterns across Rajasthan districts and seasons.
6. Build a simple baseline before testing more advanced models.
7. Evaluate the model using leakage-safe train and test splits.
8. Explain predictions and document the model's limitations.
9. Build a small user interface after the model is reliable.

## Repository structure

```text
rajasthan-crop-recommender/
|-- data/
|   |-- raw/          # Original source files (not committed)
|   |-- interim/      # Partially cleaned data (not committed)
|   `-- processed/    # Model-ready data (not committed)
|-- models/           # Saved trained models (not committed)
|-- notebooks/
|   `-- 00_setup_and_first_steps.ipynb
|-- .gitignore
|-- README.md
`-- requirements.txt
```

## Local setup in VS Code (Command Prompt)

Open this project folder in VS Code and run the following commands in its terminal:

```cmd
python -m venv .venv
.venv\Scripts\activate.bat
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Then open `notebooks/00_setup_and_first_steps.ipynb`, click **Select Kernel**, choose **Python Environments**, and select the Python interpreter inside `.venv`.

To confirm that the environment's Python is active:

```cmd
python -c "import sys; print(sys.executable)"
```

## Tools and why they are used

- **Python:** implements data processing and machine learning.
- **Jupyter Notebook:** supports learning, experiments, explanations, and visible outputs.
- **pandas and NumPy:** load, clean, transform, and analyse tabular data.
- **Matplotlib and Seaborn:** create exploratory charts.
- **scikit-learn:** build preprocessing pipelines, baseline models, and evaluations.
- **Git and GitHub:** preserve the development history and publicly present the project.

## Data safety and reproducibility

- Raw source files are never overwritten.
- Large or sensitive datasets are excluded from GitHub.
- Every source will record its URL, access date, licence, units, and limitations.
- Farmer names, phone numbers, addresses, survey numbers, and exact personal land identifiers will not be committed.
- Model results will not be reported until the evaluation method and test data are documented.

## Next milestone

The next milestone is to obtain and audit an official Rajasthan crop-production dataset while waiting for a response to the Soil Health Card data request.
