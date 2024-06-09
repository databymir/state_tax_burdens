# State Tax Burden Analysis
**This project performs a data analysis of state tax burden data for 2022 in the United States. This includes questions such as:**
1. Are there insights to be drawn by evaluating the in-state and out-of-state portions of total tax burden?
2. Does living in a particular area of the United States affect the total tax burden per capita?
3. Does the partisan lean of a state affect the total tax burden experienced by its citizens?
4. Does individual income per capita affect total tax burden?
5. Does living in a state without an individual income tax affect total tax burden? 

**Highlighted Skills:**
* Leveraged Python for data manipulation and analysis.
* Imported from multiple sources with different file types.
* Utilized NumPy and Pandas to prepare and clean data; including to null value removal, cleaning inconsistent values, and merging multiple DataFrames.
* Computed and analyzed descriptive statistics in Python
* Utilized Matplotlib and Seaborn to create visualizations to complement statistical analysis

## Table of Contents
* [Authors](#authors)
* [Installation](#installation)
* [Data](#data)
* [Code](#code)
* [Results](#results)
* [References](#references)
* [License](#license)

## Authors 
[@databymir] (https://github.com/databymir)

## Installation
### Codes and Resources Used
Python Version: 3.12.3
Jupyter Notebook Version: 7.0.6

### Python Packages Used
#### Data Manipulation
NumPy Version: 1.26.2
Pandas Version: 2.1.4
Functools (as part of standard Python)

#### Data Visualization
Matplotlib Version: 3.8.2
Seaborn Version: 0.13.2

## Data
### Source Data
The dataset is composed of information about state taxes, geographical areas, and partisan lean. The data was provided by the following:
1. Income and income tax data from The United States Census Bureau (via tax data compiled by The Tax Foundation)
2. Tax burden data from The Tax Foundation
2. Geographical data from The United States Census Bureau (via Chris Halpert's GitHub repository)
3. Partisan lean data from FiveThirtyEight's "partisan_lean" GitHub repository

### Data Acquisition
Part of the tax data was acquired by downloading the .xlsx file from The Tax Foundation's website at https://taxfoundation.org/data/all/state/2024-state-tax-data/.
The second part of the tax data was acquired by downloading and converting the .pdf file from The Tax Foundation's website at https://taxfoundation.org/data/all/state/tax-burden-by-state-2022/.
The geographical data was acquired by downloading the .csv file from Chris Halpert's GitHub repository at https://github.com/cphalpert/census-regions.
The partisan lean data was acquired by downloading the .csv file from FiveThirtyEight's GitHub repository at https://github.com/fivethirtyeight/data/tree/master/partisan-lean.

### Data Preprocessing
First, a number of empty rows import with the various datasets, which need to be removed.
Second, there are a number of differing naming schemes used amongst the datasets for the "state" values, which need to be cleaned and converted to a uniform set of values before merging the DataFrames.
Third, upon merging the DataFrames, there will still be some string values that need to be converted to a numeric data type.

## Code
├── Facts-Figures-2024-State-Tax-Data-Tax-Foundation.xlsx

├── fivethirtyeight_partisan_lean_STATES.csv

├── table_2_salt_burdens_by_state_2022.csv

├── table_2_salt_burdens_by_state_2022.pdf

├── us census bureau regions and divisions.csv

├── state_tax_burden.ipynb

├── LICENSE

├── README.md

└── .gitignore

## Results
Based on the analysis of The Tax Foundation data, the US Census regions and divisions, and the FiveThirtyEight partisan lean metric, the following key insights were obtained:
1. The in-state tax burden is significantly more correlated with total tax burden, when compared to its out-of-state counterpart.
2. The distributions of total tax burden by region and division indicate that geographical areas do impact the range of potential tax burdens that a resident might face.
3. The partisan lean is strongly correlated with in-state and total tax burden, indicating that political leanings affect tax policy and that policy does have an impact on the economic tax burden of constituents.
4. Individual income per capita is highly correlated with total tax burden, implying that people who live in states with higher income shoulder a higher tax burden. Moreover, individual income is more strongly correlated with out-of-state tax burden than in-state tax burden, implying that a state can control the in-state tax burden through policy but cannot avoid out-of-state tax burdens from scaling with per capita income.
5. Living in a state with no individual income tax does not provide free passage to paying little or no tax overall. The states that do not impose an individual income tax have a wide range of total tax burdens.

## References
Tax Foundation. (2024, April 3). *Facts & Figures 2024: How Does Your State Compare?* https://taxfoundation.org/data/all/state/2024-state-tax-data/

Tax Foundation. (2022, April 7). *State and Local Tax Burdens, Calendar Year 2022*. https://taxfoundation.org/data/all/state/tax-burden-by-state-2022/

Halpert, Chris. (2014, June 23). *census-regions*. GitHub. https://github.com/cphalpert/census-regions

FiveThirtyEight. (2022, September 9). *partisan-lean*. GitHub. https://github.com/fivethirtyeight/data/tree/master/partisan-lean

## License
For this github repository, the License used is [MIT License](https://opensource.org/license/mit/).
