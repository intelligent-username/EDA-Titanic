# Exploratory Data Analysis on the Titanic Dataset

![Image of the Titanic](cover.png)

*The Titanic* by Ken Marschall

This project explores the infamous Titanic disaster through statistical analysis, uncovering the hidden patterns behind who survived and who perished on that fateful night of April 15, 1912.

## Key Findings

- **Ticket Class** had the strongest influence on survival, with first-class passengers having significantly higher survival rates (p-value < 10^-12)
- **Gender** played a crucial role, with women having a much higher chance of survival than men
- **Boarding Location** showed a statistically significant association with survival rates
- **Age** among adults was not a significant predictor of survival, though children had higher survival rates overall

## Methods Used

- **Chi-Squared Tests**: Used to determine if categorical variables (gender, boarding location) were independent of survival rates
- **Logistic Regression**: Applied to model the relationship between continuous variables (age, fare) and survival probability
- **Statistical Hypothesis Testing**: Employed to establish significance with p-values
- **Data Visualization**: Leveraged histograms, scatter plots with logistic curves, and comparative distributions to reveal patterns

## Data Source

The analysis uses the extended Titanic dataset from [Kaggle](https://www.kaggle.com/datasets/pavlofesenko/titanic-extended).

## Prerequisites

- Python 3.10

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
