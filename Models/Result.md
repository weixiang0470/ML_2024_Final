# **KOI Table Group**
## **Random Forest**
1. Accuracy : 0.84
2. Precision : 0.79
3. Recall : 0.92
4. F1-score : 0.85
- 5 most importance features
    1. koi_impact
    2. koi_depth
    3. koi_model_snr
    4. koi_steff
    5. koi_smet
- CM
![CM](./Img/KOI_rf_cm.png)

## **XGBoost**
1. Accuracy : 0.84
2. Precision : 0.79
3. Recall : 0.93
4. F1-score : 0.85
- 5 most importance features
    1. koi_impact
    2. koi_insol
    3. koi_depth
    4. koi_model_snr
    5. koi_teq
- CM
![CM](./Img/KOI_xgb_cm.png)

## **Neural Network**
1. Accuracy : 0.82
2. Precision : 0.71
3. Recall : 0.97
4. F1-score : 0.82
- CM

![CM](./Img/KOI_nn_cm.png)