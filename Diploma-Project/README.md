# Adaptive Multi-Signal Systematic Trading Strategies  
MSc FinTech Diploma Project  
Author: Yifan  
Report: 2025-AP-FinTech  
Institution: Imperial College London  

---

## Overview

This repository contains the full implementation of the MSc FinTech Diploma Project titled **Adaptive Multi-Signal Systematic Trading Strategies**.  
The project integrates:

- Price-based technical indicators  
- Macroeconomic variables  
- FinBERT-based text embeddings  
- Machine learning models (LASSO, XGBoost)  
- Deep learning models (VSN, LSTM)  
- Meta-model regime filtering  
- Risk-managed portfolio construction  

Evaluation includes **Fama-MacBeth cross-sectional IC**, **long–short factor portfolios**, and **backtests from 2010–2022**.

---

## Project Structure

```text
Quantitative-Trading-Strategies/
│
├── VSN_LSTM/
│   ├── VSN+LSTM_with_metamodel.ipynb
│   ├── attention_weights_2017.csv
│   ├── attention_weights_2018.csv
│   ├── attention_weights_2019.csv
│   ├── attention_weights_2020.csv
│   ├── merged_macro_data.csv
│   ├── merged_stock_with_text_features.csv
│   ├── lstm_vsn_best_config_results.csv
│   ├── lstm_vsn_train_predictions.csv
│   ├── lstm_vsn_test_predictions.csv
│   ├── lstm_vsn_train_test_predictions.csv
│   ├── vsn_lstm_meta_prediction.csv
│   ├── best_model_2017.pt
│   ├── best_model_2018.pt
│   ├── best_model_2019.pt
│   ├── best_model_2020.pt
│
├── Feature_Engineering/
│   ├── Feature_Engineering.ipynb
│   ├── final_cleaned_stock_data.csv
│   ├── filtered_pxlast_2010_2022.csv
│   ├── rf.xlsx
│   ├── final_stock_data_with_signal.csv
│
├── Stock_Data_Preprocessing/
│   ├── stock_data_preprocess.ipynb
│   ├── equity.csv
│   ├── equity_long_format.csv
│   ├── final_cleaned_stock_data.csv
│   ├── filtered_pxlast_2010_2022.csv
│
├── Text_Preprocessing/
│   ├── news_preprocess.ipynb
│   ├── filtered_nasdaq_data2.csv
│   ├── finbert_cls_embedding.csv
│   ├── finbert_sentiment_score.csv
│   ├── finbert_pca_embedding.csv
│   ├── finbert_weighted_pca.csv
│
├── Lasso&XGboost/
│   ├── Lasso_XGBoost.ipynb
│   ├── merged_macro_data.csv
│   ├── merged_stock_with_text_features.csv
│   ├── finbert_weighted_pca.csv
│   ├── final_stock_data_with_signal.csv
│   ├── lasso_results.csv
│   ├── model_roll_results.csv
│   ├── df_with_lasso_predict.csv
│   ├── common_model_meta_prediction.csv
│
├── Diploma-Project/
│   ├── 2025-AP-FinTech.pdf
│   ├── README.md
│
└── README.md
