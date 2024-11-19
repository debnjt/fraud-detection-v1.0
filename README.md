# Introduction
Theft of electricity can be done in the forms of meter tampering, illegal connections, billing irregularaities, and unpaid bills, to name a few (Smith, 2004). This has resulted in loss of approximately $96 billion yearly across the globe (Northeast Group, 2022). To reduce the loss, I investigate developing a fraud detection system to spot theft of electricity and gas.

# Methodology
This project is inspired by "Enhancing Electricity Theft Detection through K-Nearest Neighbors and Logistic Regression Algorithms with Synthetic Minority Oversampling Technique: A Case Study on State Electricity Company (PLN) Customer Data" written by Yan Maraden et al. In this paper, the authors found that a proposed solution of logistic regression with SMOTE oversampling technique outperforms existing methods for the Indonesian dataset they were working on. With the addition that logistic regression is a well known classification method, I propose the use of logistic regression to develop a model for the Tunisian dataset. 

As the Tunisian dataset is imbalanced with more observations of non-fraud rather than fraud, I look into sampling methods to rectify the biasness. In my code, I explore undersampling, oversampling and Synthetic Minority Oversampling Technique. 

# Dataset
The data is from the Tunisian Company of Electricity and Gas. There are 2 datasets, client.csv and invoice.csv

## invoice.csv
The data contains the following columns
- id: Customer id
- date: Date of meter reading
- counter_type: Nominal data to indicate electricity or gas reading
- consommation_level_1: Consumption level
- consommation_level_2: Consumption level
- consommation_level_3: Consumption level

## client.csv
The data contains the following columns
- region: Location of customer
- date: Start date of customer
- id: Customer id

# Conclusion
Logistic regression alongside oversampling shows the best result (evaluated by recall and f1 score). 

# Future Works
I would like to explore other methods of classification such as K Nearest Networks and decision trees. It would be interesting to analyze whether the effect of dimensionality reduction methods like Principal Component Analysis could improve the performance of the model. 

# References
1. Maraden, Y., Wibisono, G., Nugraha, I. G. D., Sudiarto, B., Jufri, F. H., Kazutaka, & Prabuwono, A. S. (2023). Enhancing Electricity Theft Detection through K-Nearest Neighbors and Logistic Regression Algorithms with Synthetic Minority Oversampling Technique: A Case Study on State Electricity Company (PLN) Customer Data. Energies, 16(14), 5405. https://doi.org/10.3390/en16145405
2. Northeast Group, L. (2018, June 26). $96 billion is lost every year to electricity theft. PR Newswire: press release distribution, targeting, monitoring and marketing. https://www.prnewswire.com/news-releases/96-billion-is-lost-every-year-to-electricity-theft-300453411.html
3. Smith, T. B. (2004). Electricity theft: A comparative analysis. Energy Policy, 32(18), 2067–2076. https://doi.org/10.1016/s0301-4215(03)00182-4 
