
# Photometric Redshift Estimation of SDSS Galaxies Using Supervised Learning

<img width="2723" height="800" alt="Pic5-NASA-MWA-Star-Clusters" src="https://github.com/user-attachments/assets/88a3f7df-8f98-417e-b093-b382724b01ed" />

A benchmark of five regressors (linear regression, kNN, random forest, XGBoost and an MLP) for photometric redshift (photo-z) estimation on 57,241 SDSS DR17 galaxies (0.001 ≤ z ≤ 1), using the five optical magnitudes u, g, r, i, z and four adjacent colors as features. Includes a head-to-head comparison with Henghes et al. (2021), who ran the same setup on 28× more data, and a magnitudes-vs-colors feature ablation.


Results

Tuned models on the held-out test set (11,449 galaxies), all nine features:

| Model             |        MAE |        MSE |       Bias |     σ_NMAD | Outliers (%) |
|:------------------|-----------:|-----------:|-----------:|-----------:|-------------:|
| Linear regression |     0.0712 |     0.0118 |     0.0054 |     0.0499 |         5.34 |
| kNN               |     0.0477 |     0.0075 |     0.0027 |     0.0274 |         2.91 |
| Random forest     | **0.0460** | **0.0071** | **0.0023** | **0.0259** |         2.84 |
| XGBoost           |     0.0462 |     0.0072 |     0.0024 |     0.0264 |         2.81 |
| MLP               |     0.0472 |     0.0073 |     0.0036 |     0.0275 |     **2.80** |


The four non-linear models sit within 0.0004 MSE of each other. With 28× less data than Henghes et al. we match or slightly beat their σ<sub>NMAD</sub> for every non-linear model; they win on the tail-sensitive MAE and MSE. Non-linear models get nearly the same performance from magnitudes alone or colors alone.

---------------

## Paper
full write up

<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0001" src="https://github.com/user-attachments/assets/c8264e1f-e2fc-4a5c-a36b-e208eb3541b4" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0002" src="https://github.com/user-attachments/assets/f49866e0-5813-444d-a398-3c43f2043dcc" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0003" src="https://github.com/user-attachments/assets/2abf517c-27d6-4eef-88a7-f3294810ed12" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0004" src="https://github.com/user-attachments/assets/080b790d-8157-421c-b36e-946284b79d0a" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0005" src="https://github.com/user-attachments/assets/d6814c2a-ba3d-4a09-8736-2c6a449b2a2e" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0006" src="https://github.com/user-attachments/assets/bdee5105-f9eb-41b6-9d22-8f6715cce957" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0007" src="https://github.com/user-attachments/assets/f9e5a611-fa9c-42c0-b1c9-2d9f12395ee6" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0008" src="https://github.com/user-attachments/assets/71a78955-09f2-42d4-9d51-dacb01a73fb0" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0009" src="https://github.com/user-attachments/assets/ac06d485-dc9a-403c-86d3-2c9a223ccf8d" />
<img width="1275" height="1650" alt="Photometric Redshift Estimation of SDSS Galaxies-1-1-1_page-0010" src="https://github.com/user-attachments/assets/f6ce6249-7ab5-4549-9473-4fa8f3e8e673" />


