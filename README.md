# Laptop Price Predictor

Laptop Price Predictor is a small machine-learning project that estimates laptop prices from hardware and configuration features. The repository includes data preprocessing and modeling in a Jupyter notebook and a Streamlit app for quick interactive price predictions.

## Key Features
- Data cleaning and feature engineering (screen PPI, touchscreen/IPS flags, storage parsing, CPU/GPU/os categories).
- Multiple model experiments (Linear, Ridge, Lasso, RandomForest, GradientBoosting, XGBoost, Stacking/Voting).
- Exported pipeline (`pipe.pkl`) and dataset snapshot (`df.pkl`) for fast prediction in a Streamlit app.
- Interactive web UI (`app.py`) for predicting laptop prices.

## Quick Start

Prerequisites
- Python 3.8+ (recommended)
- pip

Install dependencies:
```bash
pip install -r requirements.txt
```

Run the Streamlit app:
```bash
streamlit run app.py
```
Open the local URL printed by Streamlit (usually http://localhost:8501).

## Training / Notebook
The data preprocessing and model training are in `laptop price prediction.ipynb`. To retrain:
1. Open the notebook in Jupyter or VS Code.
2. Run the cells from top to bottom to preprocess, train models and export `pipe.pkl` and `df.pkl`.

After re-exporting, restart the Streamlit app to use the updated pipeline.

## Files of interest
- `laptop_data.csv` — original dataset used for training.
- `laptop price prediction.ipynb` — notebook with preprocessing, EDA and modeling.
- `app.py` — Streamlit app loading `pipe.pkl` and `df.pkl` to serve predictions.
- `pipe.pkl`, `df.pkl` — exported model pipeline and dataframe snapshot.

## Notes on Data & Model
- The app predicts the log of price internally — the displayed price is the exponentiated prediction (original scale).
- If you retrain models, ensure the exported pipeline accepts the same feature order as `app.py` input.

## Contributing
- Fix bugs or add features via PRs.
- For dataset updates, update the notebook preprocessing cells and re-export `pipe.pkl` and `df.pkl`.

## License & Credits
Use and modify as needed. Credit the original author of the dataset and any third-party libraries used.

## Contact
For questions or help, open an issue or contact the repository owner.
