Adaptive Multi-Signal Systematic Trading Strategies

MSc FinTech Diploma Project
Author: Yifan
Report: 2025-AP-FinTech
Institution: Imperial College London

Overview

This repository contains the full implementation of the MSc FinTech Diploma Project titled Adaptive Multi-Signal Systematic Trading Strategies.
The research integrates price-based indicators, macroeconomic variables, and FinBERT-based text embeddings using machine learning and deep learning models including LASSO, XGBoost, VSN, and LSTM.
Evaluation methods include Fama-MacBeth cross-sectional IC, long-short factor portfolios, meta-model regime filtering, and risk-managed backtesting from 2010 to 2022.

Project Structure

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

Data Access

Due to file size limitations, complete datasets and intermediate files are available at the following link:

https://drive.google.com/drive/folders/1slYxjsxwI0v614aNnJi4T_h61Yyw3NKo

Methodological Notes
1. FinBERT Look-Ahead Consideration

FinBERT is a pretrained language model trained on historical financial news.
Although only news published up to each trading day is used for feature construction, the pretrained embedding space may encode long-horizon structural information from its corpus.
This does not constitute direct look-ahead leakage, but the possibility of minimal structural information leakage is acknowledged.

2. Statistical Validation Using Fama-MacBeth IC

Predictive validity is evaluated using a Fama-MacBeth cross-sectional regression framework.

Steps:

Compute the daily cross-sectional correlation (IC) between signals or model outputs and forward returns.

Collect the IC time series across the sample period.

Test whether the average IC is significantly different from zero using its time-series standard error.

This provides a robust measure of cross-sectional predictability independent of any specific functional form.

3. Long-Short Portfolio Evaluation

To measure economic significance:

Rank stocks cross-sectionally each day based on signal value.

Form a long portfolio using the highest-ranked quantile.

Form a short portfolio using the lowest-ranked quantile.

Compute long-short returns over time.

This directly evaluates whether signals translate into tradeable returns.

4. Meta-Model Regime Filtering

A secondary classification model is trained to identify days when the base strategy is more likely to be profitable.
Inputs include macroeconomic indicators, aggregated text features, volatility measures, and dispersion of predictions.
The meta-model suppresses exposure during unfavorable market regimes, reducing drawdown and improving stability.

5. Risk-Managed Portfolio Construction

Three weighting schemes are implemented:

Equal Weight

Volatility Parity

Risk Parity

Covariance matrices are estimated on rolling windows to construct stable and diversified portfolios.

Citation

Report Citation
Yifan. (2025). Adaptive Multi-Signal Systematic Trading Strategies. MSc FinTech Diploma Project, Imperial College London.

Code Repository Citation
Yifan. (2025). Quantitative-Trading-Strategies. GitHub Repository.
https://github.com/Starfocker/Quantitative-Trading-Strategies

BibTeX (Report)
@report{yifan2025adaptive,
  title       = {Adaptive Multi-Signal Systematic Trading Strategies},
  author      = {Yifan},
  year        = {2025},
  institution = {Imperial College London},
  note        = {MSc FinTech Diploma Project},
}

BibTeX (Code)
@software{yifan2025qts,
  author  = {Yifan},
  title   = {Quantitative-Trading-Strategies: Codebase for Adaptive Multi-Signal Systematic Trading},
  year    = {2025},
  url     = {https://github.com/你的用户名/Quantitative-Trading-Strategies},
  version = {1.0}
}

Contact

For questions or reproduction inquiries, please open an issue in the repository or contact directly.
