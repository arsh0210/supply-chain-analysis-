# Supply Chain Delivery Performance Analysis & Predictive Insight

📌 **Project Overview**

This project features a comprehensive analysis of end-to-end order fulfillment operations for a global e-commerce company. The analysis processes 172,765 orders to pinpoint the root causes of chronic late deliveries and establishes a data-driven framework leveraging Machine Learning to predict and prevent future delays.

🎯 **Objectives & KPIs**

*   **Analyze Performance:** Evaluate delivery metrics across regions, shipping modes, and customer segments.
*   **Quantify Impact:** Assess the financial drain of delayed shipments, which currently put **$2.1M** in profit at constant risk.
*   **Track Baseline Metrics:** Monitor the overall late delivery rate (**54.71%**) against the on-time delivery rate (**45.29%**).
*   **Identify Bottlenecks:** Isolate critical failure points, such as First Class shipping, which suffers from a highly problematic 100% delay rate.

⚙️ **Technical Implementation & ML Model**

*   **Data Processing:** Cleaned the raw data by dropping redundant features, formatting datetime variables, and engineering target metrics like `Order Processing Time` and `Delay`.
*   **Class Imbalance Handling:** Applied Synthetic Minority Over-sampling Technique (SMOTE) to the training set, increasing the minority class to 79,182 records to ensure unbiased model training.
*   **Predictive Modeling:** Engineered a robust Random Forest Classifier to predict the `Late_delivery_risk` of individual orders.
*   **Model Performance:** The classification model achieved an overall accuracy of **74%**, with a precision of **78%** and recall of **75%** specifically for classifying late orders.

💡 **Strategic Recommendations**

*   **Audit Shipping SLAs:** Immediately audit premium shipping modes (First and Second Class) and consider defaulting eligible orders to Standard Class until performance improves.
*   **Deploy Alert System:** Integrate the Random Forest predictive model into the order management pipeline to flag high-risk transactions at the point of confirmation.
*   **Optimize Processing:** Introduce automated escalations for orders stalled in `PAYMENT_REVIEW` or `PENDING_PAYMENT` statuses, as these significantly elevate delay rates.
*   **Capacity Planning:** Build targeted pre-season logistics capacity for known peak delay months like August, September, and December.
