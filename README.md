# Laptop Price Predictor 

![Laptop Price Predictor Banner](https://example.com/banner.png)  <!-- Replace with an actual banner image -->

A machine learning-powered web application to predict laptop prices based on their specifications. This project demonstrates an end-to-end machine learning workflow, from data exploration and feature engineering to model training and deployment as an interactive web app using Streamlit.

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Live Demo](#live-demo)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Training](#model-training)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

The Laptop Price Predictor is designed to provide users with an estimated price for a laptop given its hardware and software configuration. The prediction is made by a machine learning model trained on a dataset of laptop specifications and prices. The project includes a Jupyter notebook that details the data cleaning, exploratory data analysis (EDA), feature engineering, and model selection process. The final model is deployed as a user-friendly web application using Streamlit.

## Key Features

- **Data Preprocessing:** Comprehensive data cleaning and feature engineering, including:
    - Calculation of screen PPI (Pixels Per Inch).
    - Extraction of touchscreen and IPS display features.
    - Parsing and categorization of storage, CPU, GPU, and operating systems.
- **Model Experimentation:** Evaluation of various regression models, including:
    - Linear Regression, Ridge, and Lasso.
    - Ensemble methods like Random Forest and Gradient Boosting.
    - Advanced models like XGBoost.
    - Stacking and Voting regressors for improved performance.
- **Interactive Web App:** A Streamlit application that allows users to:
    - Select different laptop specifications (Company, Type, RAM, Weight, etc.).
    - Get an instant price prediction.
- **Reproducibility:** The repository includes the dataset, the trained model pipeline (`pipe.pkl`), and a snapshot of the processed data (`df.pkl`) for easy replication of the results.

## Live Demo

A live demo of the application is hosted on Streamlit Cloud. You can access it here: [Streamlit App Link](https://laptop-predictor-2txzje29nczusqikzy4o4d.streamlit.app/)

## Getting Started

Follow these instructions to set up and run the project locally.

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/LAPTOP-PREDICTOR-main.git
    cd LAPTOP-PREDICTOR-main
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

To start the Streamlit web application, run the following command in your terminal:

```bash
streamlit run app.py
```

This will open a new tab in your web browser with the application running locally at `http://localhost:8501`.

## Project Structure

Here is an overview of the key files in this project:

-   `app.py`: The main Python script for the Streamlit web application.
-   `laptop price prediction.ipynb`: Jupyter notebook containing the complete data analysis, model training, and evaluation process.
-   `pipe.pkl`: The serialized machine learning pipeline (model).
-   `df.pkl`: A pickled pandas DataFrame used by the Streamlit app.
-   `laptop_data.csv`: The raw dataset used for training the model.
-   `requirements.txt`: A list of all Python libraries required to run the project.
-   `README.md`: This file, providing an overview of the project.

## Model Training

The `laptop price prediction.ipynb` notebook contains all the steps for data preprocessing and model training. If you want to retrain the model or experiment with different techniques:

1.  Launch the Jupyter notebook:
    ```bash
    jupyter notebook "laptop price prediction.ipynb"
    ```
2.  Run the cells sequentially to perform data cleaning, feature engineering, and model training.
3.  The notebook will export the trained pipeline as `pipe.pkl` and the processed DataFrame as `df.pkl`.

After retraining and exporting the new files, restart the Streamlit application to use the updated model.

## Contributing

Contributions are welcome! If you have any suggestions, find a bug, or want to add a new feature, please follow these steps:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature-name`).
3.  Make your changes and commit them (`git commit -m 'Add some feature'`).
4.  Push to the branch (`git push origin feature/your-feature-name`).
5.  Open a Pull Request.

Please make sure to update the tests as appropriate.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact

If you have any questions or want to get in touch, please open an issue on this repository.