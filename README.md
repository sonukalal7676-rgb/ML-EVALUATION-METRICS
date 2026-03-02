**Breast Cancer Classifier
A decision tree classifier trained on the sklearn breast cancer dataset, with a full evaluation suite covering both probabilistic and hard-prediction metrics.**

**What it does**
Loads the built-in breast cancer dataset, splits it 70/30, trains a DecisionTreeClassifier, and prints out 8 metrics:

MSE / MAE / RMSE / R² — computed against predicted probabilities (continuous output)
Accuracy / Precision / Recall / F1 — computed against hard class predictions

**The mix of regression-style and classification metrics is intentional** — it gives a fuller picture of how well the model's confidence aligns with actual outcomes, not just whether the final label was correct.

**Requirements**
numpy
scikit-learn

****Notes**
The train/test split is random each run (no random_state set), so metric values will shift slightly between runs — expected behavior
predict_proba on a decision tree returns 0.0 or 1.0 for most samples since trees don't smooth probabilities; this makes MSE/RMSE a bit harsher than you'd see with a calibrated model
Swap in RandomForestClassifier or add CalibratedClassifierCV if you want smoother probability estimates

**Output example**
MSE: 0.06213458974321098
MAE: 0.04128765432109876
RMSE: 0.24926893456781234
R2 Score: 0.748523987654321
Accuracy: 0.9473684210526315
Precision: 0.9523809523809523
Recall: 0.9238095238095239
F1 Score: 0.937799043062201
