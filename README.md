# Executive Summary - Insurance Loss Predictive Modeling
Accurately setting premiums is a core challenge for insurers. Premiums must reflect each policyholder’s expected loss to remain competitive. Overcharging low-risk customers or undercharging high-risk ones creates adverse selection—profitable customers leave, and the insurer retains disproportionately high-risk policyholders, leading to financial loss.

This project addresses that challenge by predicting claim losses to support fair and profitable pricing. Claim loss data are difficult to model because claim sizes are highly skewed and many records show zero losses. This requires careful handling of zero claims and non-normal distributions.

To tackle this, we developed a two-step, chained predictive modeling approach combining classification and regression techniques with resampling to address class imbalance. The approach first predicts whether a loss occurs, then estimates the size of the loss and the historically adjusted loss cost for non-zero cases, and finally predicts claim likelihood. This structure reduces bias from the heavy zero-loss class, improves accuracy on non-zero losses, and avoids data leakage between dependent variables.

We will evaluate candidate models and select the most accurate approach, measuring out-of-sample performance with Mean Squared Error (for LC and HALC) and ROC-AUC (for claim status). The resulting framework enables insurers to better forecast claim costs, price policies more fairly, and reduce the risk of adverse selection.
