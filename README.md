# EDA on the Titanic Disaster

![Image of the Titanic](cover.png)

*The Titanic* by Ken Marschall

This project explores the infamous Titanic disaster through statistical analysis, uncovering the hidden patterns behind who survived and who perished on that fateful night of April 15, 1912.

## Key Findings

- **Ticket Class**: First-class passengers had dramatically higher survival odds (p-value < $10^{-12}$).
- **The Women and Children**: Being a woman or a child nearly tripled the chances of survival. Chivalry wasn't dead.
- **Boarding Location**: showed a statistically significant association with survival rates.
- **Age**: Among adults, being younger didn't help you survive, although being a child definitely did.

## Methods Used

- **Chi-Squared Tests**: Used to determine if categorical variables (gender, boarding location) were independent of survival rates
- **Logistic Regression**: Applied to model the relationship between continuous variables (age, fare) and survival probability
- **Statistical Hypothesis Testing**: Employed to establish significance with p-values
- **Data Visualization**: Leveraged histograms, scatter plots with logistic curves, and comparative distributions to reveal patterns

## Summary Results

| Variable | Method | Statistic | p-value | Significant (α=0.05) |
|----------|--------|-----------|---------|----------------------|
| Embarked | Chi-Squared | 26.47 | 2.68×10^-7 | Yes |
| Gender (Adults) | Chi-Squared | 202.99 | 4.64×10^-46 | Yes |
| Age (Adults) | Logistic (coef = 0.0023) | — | 7.41×10^-1 | No |
| Fare | Logistic (coef = 0.0152) | — | 9.86×10^-12 | Yes |

## Quick Start

```sh
git clone <your-repo-url>
cd EDA-Titanic
# Make sure dependencies are installed (see below)
jupyter lab analysis.ipynb # Or open in a code editor that supports Jupyter Notebooks
```

## Python Version

Tested with Python 3.10 (recommended).

## Data Source

The analysis uses the extended Titanic dataset from [Kaggle](https://www.kaggle.com/datasets/pavlofesenko/titanic-extended).

## Installing Dependencies

### Using Conda

1. Open a terminal and navigate to this project directory.
2. Run:

    ```sh
    conda env create -f requirements.yml
    conda activate eda-titanic
    ```

### Using Pip

1. Open a terminal and navigate to this project directory.
2. (Optional) Create and activate a virtual environment:

    ```md
    python -m venv venv
    ```

    ```powershell
    # On Windows:
    venv\Scripts\activate
    ```

    ```sh
    # On macOS/Linux:
    source venv/bin/activate
    ```

3. Install dependencies:

    ```sh
    pip install -r requirements.txt
    ```

## Running the Analysis

Open `analysis.ipynb` in Jupyter Notebook or JupyterLab:

```sh
jupyter lab analysis.ipynb
```

Or in a code editor (like VSCode), simply open the notebook and select the kernel corresponding to your environment.
