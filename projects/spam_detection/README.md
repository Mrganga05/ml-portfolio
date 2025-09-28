# House Price Prediction (Regression) - Baseline

**Problem:** Predict house sale prices (continuous target).

**Dataset:** Kaggle - House Prices: Advanced Regression Techniques (train.csv). Place train.csv in `projects/house_price/data/`.

**Approach:** 
- Baseline features: OverallQual, GrLivArea, YearBuilt, TotalBsmtSF, FullBath, GarageCars, GarageArea, LotArea.
- Target transformed with log1p to reduce skew.
- Preprocessing: median imputation + standard scaling.
- Model: RandomForestRegressor (pipeline).

**How to run:**
```bash
# from repo root
pip install -r requirements.txt
# run training
python projects/house_price/train.py
# run prediction example
python projects/house_price/predict_example.py
