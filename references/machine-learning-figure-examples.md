# Machine Learning Figure Examples for MSSP-Style Papers

These examples are synthetic templates for machine-learning-assisted mechanical nonlinear dynamics papers.

## Common Figure Types

| Figure type | Typical manuscript question | Template file |
|---|---|---|
| Radar chart | How do models compare across normalized metrics such as accuracy, robustness, speed, and stability? | `demo_ml_radar_chart.py` |
| Confusion matrix | Which dynamic states or fault classes are misclassified? | `demo_ml_confusion_matrix.py` |
| Prediction versus truth | Is the regression model unbiased and close to the ideal 1:1 line? | `demo_ml_prediction_truth.py` |
| Residual trend + KDE | Are residuals centered, narrow, and independent of frequency or amplitude? | `demo_ml_residual_kde.py` |
| Feature importance | Which physical or signal features dominate the learned model? | `demo_ml_feature_importance.py` |
| Hyperparameter heatmap | Where is the validation error minimized in the tuning space? | `demo_ml_hyperparameter_heatmap.py` |

## Style Notes

- Use radar charts only for summary views; use bar charts or boxplots for precise numeric comparison.
- For confusion matrices, annotate cells with percentages and keep class labels short.
- For prediction-versus-truth plots, always include the 1:1 reference line and a residual panel when space permits.
- For residual-density plots, show both residual trend and distribution so bias and spread are visible.
- For feature importance, prefer horizontal bars when feature names are longer than three characters.
- For heatmaps, show a colorbar with units and mark the selected hyperparameter setting.
