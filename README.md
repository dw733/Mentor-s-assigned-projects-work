# Diabetes Progression Prediction

My mentor challenged me to start with linear regression and see if I could improve it. I used scikit-learn’s diabetes dataset, which has 442 records and 10 input features, to predict a disease progression score one year after baseline.

[Open the notebook](./Linear_Regression_Baseline_Improvements.ipynb)

## What I did

I trained a linear regression baseline, then tried Ridge regression and Ridge with degree-2 polynomial features. I used five-fold cross-validation on the training data to pick the Ridge settings and saved 89 records for the final test. I kept scaling inside each scikit-learn pipeline so it learned from the training data in each fold.

## Results

| Model | Test RMSE |
| --- | ---: |
| Linear regression | 53.85 |
| Ridge regression | 53.78 |
| Polynomial Ridge | **52.67** |

Polynomial Ridge lowered test RMSE by about **2.2%** compared with my baseline. That was a small improvement on one test split. The part I learned most from was setting up a fair comparison and checking that the improvement held on data the models hadn’t seen.

## Run it yourself

I ran this notebook with Python 3.12. Install the packages and open JupyterLab from the project folder.

```bash
python -m pip install jupyterlab numpy pandas matplotlib scikit-learn==1.8.0
python -m jupyterlab
```

Open `Linear_Regression_Baseline_Improvements.ipynb` and run all cells. The dataset comes with scikit-learn, so it loads automatically.
