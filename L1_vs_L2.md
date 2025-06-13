L1 vs. L2 Regularization

Regularization techniques help prevent overfitting in machine learning models by adding a penalty to the loss function.

Mathematical Definitions
	•	L1 Regularization (Lasso):
\text{Penalty} = \lambda \sum_{i=1}^{n} |\beta_i|
	•	L2 Regularization (Ridge):
\text{Penalty} = \lambda \sum_{i=1}^{n} \beta_i^2

Conceptual Differences

Aspect	L1 Regularization (Lasso)	L2 Regularization (Ridge)
Sparsity	Encourages sparse solutions (coefficients become zero)	Typically shrinks coefficients towards zero without setting them exactly to zero
Geometric intuition	Diamond-shaped constraint region (sharp corners)	Circular constraint region (smooth, no corners)
Robustness to Outliers	Robust (less influenced by outliers)	Less robust (more influenced by outliers)
Statistical Interpretation	Estimates align with median of the data	Estimates align with mean of the data

Intuition
	•	L1 Regularization:
	•	Minimizing absolute errors leads to robust median-like estimates.
	•	Effectively performs feature selection due to sparsity.
	•	L2 Regularization:
	•	Minimizing squared errors leads to estimates that resemble the mean.
	•	Typically does not eliminate features entirely but reduces their impact.

Example Illustration

Given data points: [1, 2, 3, 100]:
	•	L1 (Median-based): Estimate ≈ 2.5 (not significantly influenced by the outlier 100).
	•	L2 (Mean-based): Estimate ≈ 26.5 (strongly influenced by the outlier 100).

Practical Guidelines
	•	Use L1 Regularization if your goal is feature selection and interpretability.
	•	Use L2 Regularization if you aim to handle multicollinearity, stabilize model coefficients, and reduce overfitting without completely discarding features.
