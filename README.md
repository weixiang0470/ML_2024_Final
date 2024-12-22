# ML_2024_Final
- A final project of Machine Learning course in NTHU

## **Members**
- 黃偉祥 資工四
- p2
- p3
- p4
- p5

## **Introduction**
- We use 2 different kind of dataset and 3 machine learning algorithms on both and see which method is better on predicting exoplanet. 
- Our experiment seperate into 2 groups, **KOI-table** and **Light-curve group**.
- We choose **Random-forest**, **XGBoost**, and **Neural Network** to compare different algorithms' performances.
- We use **F1-score**, **Accuracy**, **Precision** and **Recall** to evaluate our models.

## **How to use**
1. First install the requirements libraries.
    - `pip install -r requirements.txt`
2. Use `tsfresh.ipynb` to extract features from light curve, we provide extracted features as `tsfresh_features.csv` in **Light_curve_dataset**.
3. Follow instruction in `Method_model.ipynb` and get your result.(in Models folder)

## **Dataset**
- [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/index.html)
    - [KOI-table source](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=q1_q17_dr25_sup_koi)
    - [Light curve source](https://exoplanetarchive.ipac.caltech.edu/docs/Kepler_KOI_docs.html)
        - [Document](https://exoplanetarchive.ipac.caltech.edu/docs/KSCI-19113-001.pdf)
    


# **Warnings & Errors**
1. Warning message showed below:
    - Happen on macOS(Macbook air 2020)
    - Cause by `tsfresh.extract_features`
```
python(70769) MallocStackLogging: can't turn off malloc stack logging because it was not enabled.
python(70770) MallocStackLogging: can't turn off malloc stack logging because it was not enabled.
python(70771) MallocStackLogging: can't turn off malloc stack logging because it was not enabled.
python(70772) MallocStackLogging: can't turn off malloc stack logging because it was not enabled.
```
- Solution:
    - Restart kernel and execute the code below first
    - `os.environ["MallocStackLogging"] = "0"`

2. Memory out of usages
    - Happen when extracting features using **tsfresh**
    - Because light curve information need too much memory space to store and calculate the informations
- Solution:
    - Use **TPU** at Colab platform
    - Limited every day usage by free version