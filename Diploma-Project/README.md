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
```

---

## Notes on Issues Identified After Project Completion

1. **Potential FinBERT Look-Ahead Bias**  
   Although only past news was used during modeling, FinBERT is pretrained on a broad historical corpus that includes later-period text.  
   This may introduce mild structural look-ahead effects.

2. **Factor Testing Method Not Fully Appropriate**  
   The report used pooled regressions to evaluate factor significance.  
   A more appropriate approach would be applying Fama–MacBeth IC testing and factor long–short portfolios for assessing cross-sectional predictive power.

---

## Data Access  
Full datasets and intermediate processed files can be accessed here:  
https://drive.google.com/drive/folders/1slYxjsxwI0v614aNnJi4T_h61Yyw3NKo

---

## Citation  
Yifan. (2025). *Adaptive Multi-Signal Systematic Trading Strategies*.  
MSc FinTech Diploma Project, Imperial College London.

Yifan. (2025). *Quantitative-Trading-Strategies*. GitHub Repository.  
https://github.com/Starfocker/Quantitative-Trading-Strategies

---

## BibTeX
@report{yifan2025adaptive,
  title       = {Adaptive Multi-Signal Systematic Trading Strategies},
  author      = {Yifan},
  year        = {2025},
  institution = {Imperial College London},
  note        = {MSc FinTech Diploma Project}
}

@software{yifan2025qts,
  author  = {Yifan},
  title   = {Quantitative-Trading-Strategies Codebase for Adaptive Multi-Signal Systematic Trading},
  year    = {2025},
  url     = {https://github.com/Starfocker/Quantitative-Trading-Strategies},
  version = {1.0}
}

---

## Contact  
For questions or reproduction inquiries, please open an issue on the repository.
