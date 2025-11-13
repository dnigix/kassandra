# Polymarket Signal Transfer Entropy Analysis

This project analyzes the flow of information (using Transfer Entropy) from daily social media signals to the market returns of Polymarket contracts for "Trump" and "Biden".

The main script (`polymarket_transfer_entropy.ipynb`) loads signal and price data, calculates the transfer entropy across a range of bin counts and time lags, and performs surrogate data testing to determine statistical significance.

## Key Features

* Loads daily signal and price data.
* Discretizes return data using equal-frequency binning.
* Calculates Transfer Entropy for multiple time lags (1 to 5 days).
* Performs 1000-run surrogate data testing (p-value calculation) for statistical significance.
* Generates heatmaps that visualize *only* the statistically significant TE values, making it easy to see real information flow.

## How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR-USERNAME/Polymarket-TE-Analysis.git](https://github.com/YOUR-USERNAME/Polymarket-TE-Analysis.git)
    cd Polymarket-TE-Analysis
    ```

2.  **Install dependencies:**
    Make sure you have Python 3 installed. Then, install the required packages.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Add Your Data:**
    This repository does *not* include the data. You must provide it.
    * Create a folder named `data` in the main project directory.
    * Place your data files inside it with the *exact* names:
        * `data/daily_signal.csv`
        * `data/prices_with_returns.csv`

4.  **Run the analysis:**
    Open and run the `polymarket_transfer_entropy.ipynb` notebook using Jupyter Lab or Google Colab.

    The notebook will:
    * Save the final results table to `results/transfer_entropy_results.csv`.
    * Save the output heatmaps to the `plots/` folder.
