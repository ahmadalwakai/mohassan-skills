---
name: تعلم الآلة والذكاء الاصطناعي
description: تعلم الآلة والذكاء الاصطناعي: تدريب النماذج، التصنيف، التنبؤ، الشبكات العصبية، الإفراط في التعلم overfitting، تقييم النماذج، scikit-learn، PyTorch، النماذج اللغوية. machine learning ml ai model models training train classification classifier neural network networks deep overfitting evaluation sklearn pytorch tensorflow llm الآلة الذكاء الاصطناعي نموذج نماذج تدريب أدرب ادرب العصبية
version: 1.0.0
category: analytics
---
Use this for machine learning projects, model training and evaluation.
1. Frame the problem: the decision the model supports, the target to predict, the task type (classification, regression, ranking, clustering, forecasting), a metric tied to business value, and a simple baseline to beat (rules, averages, last value).
2. Data first: enough labelled examples that represent real use; check for leakage (features containing the answer or coming from the future), duplicates, class imbalance and label quality. Split into train, validation and test sets, by time for time series.
3. Start simple: linear or logistic regression and gradient-boosted trees (XGBoost, LightGBM) are strong on tabular data; deep learning suits images, audio, text or very large data.
4. Overfitting (strong on training data, weak on new data): more data or augmentation, simpler models, regularization (L1/L2, dropout, weight decay), early stopping on validation loss, cross-validation, removal of leaky or noisy features.
5. Evaluate with the right metric: precision, recall, F1 and PR-AUC for imbalanced classes; MAE or RMSE for regression; calibration when probabilities drive decisions. Inspect errors by segment, not only the average.
6. Report honestly: test-set results once, several seeds or confidence intervals, comparison with the baseline; never tune on the test set.
7. Production: monitor input drift and accuracy over time, retrain on a schedule or trigger, version data and models, keep a human check on high-stakes decisions.
8. Language models: try prompting and retrieval before fine-tuning, evaluate on fixed real examples, watch cost, latency and privacy.
Answer shape: the approach step by step, a code skeleton (scikit-learn or PyTorch) when useful, and how to judge whether it works.
