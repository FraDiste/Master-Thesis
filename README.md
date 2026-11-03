# Machine Learning and Empirical Asset Pricing in Eurozone Equity Markets

Code for the MSc thesis *Machine Learning and Empirical Asset Pricing in Eurozone Equity Markets: A Predictive and Interpretability Analysis*, University of Siena (MSc in Finance, academic year 2025–2026).

Author: Francesco Distefano. Supervisor: Prof. Claudio Pacati. Co-supervisor: Prof. Piero Mazzarisi.

## Contents

The code consists of 11 Jupyter notebooks, to be run in order.

| Notebook | Content | Thesis section |
|---|---|---|
| `01_Stocks_List_Aggregation` | Security universe from the Datastream Navigator lists; download blocks | 3.2 |
| `02_Data_Reading` | Parsing of the Datastream and Worldscope files into long-format tables | 3.4.1 |
| `03_Padding_Removal` | Removal of post-delisting padding | 3.4.2 |
| `04_Deduplication` | Deduplication of multiple listings | 3.4.3 |
| `05_Characteristics` | Monthly panel, returns and screens, market benchmark, the 22 characteristics | 3.3, 3.4.4, 3.4.5 |
| `06_Estimation_Sample` | Size filter, complete-case and imputed samples, winsorisation, ranks | 3.4.6, 3.5 |
| `07_Linear_Models` | OLS benchmarks and penalised regressions | 3.6.1 |
| `08_Tree_Models` | Random forest and gradient boosted trees | 3.6.2, 3.6.3 |
| `09_Neural_Networks` | Neural networks NN1–NN5 | 3.6.4 |
| `10_Results` | Tables and figures of Chapter 4 and Appendix A | 3.7, 4 |
| `11_Interpretability` | SHAP values and regime analysis (Chapter 5) | 5 |

## Data

The data were retrieved from LSEG Datastream and Worldscope through the Excel add-in and are subject to a licence, so they are not included in this repository. The notebooks expect the retrieved files in a Google Drive folder (`/content/drive/MyDrive/Thesis/data`): the four country lists exported from Datastream Navigator, the market (`MKT_*.xlsx`), risk-free rate (`RF_*.xlsx`) and index (`IDX_*.xlsx`) files. The retrieval is described in Sections 3.2 and 3.4.1 of the thesis.

## Running the code

- The notebooks were developed and run in Google Colab, in order from 01 to 11. Each notebook reads the outputs of the previous ones from the data folder.
- Notebook 09 requires a GPU (around four hours on a T4).
- Random seeds are fixed, so the results are reproducible.

## Requirements

Python 3 with the packages listed in `requirements.txt` (pandas, NumPy, openpyxl, scikit-learn, LightGBM, PyTorch, matplotlib), all available by default in Google Colab.

## Citation

Distefano, F. (2026). *Machine Learning and Empirical Asset Pricing in Eurozone Equity Markets: A Predictive and Interpretability Analysis*. MSc thesis, University of Siena.
