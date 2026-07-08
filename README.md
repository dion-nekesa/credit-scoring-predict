
 # The German Credit Customer Segmentation
### This project entails the concept of Unsupervised Machine Learning via K-Means Clustering

This repository contains an end-to-end data science pipeline that transforms raw, unorganized credit applicant data into distinct behavioral customer personas. By shifting from standard individual metrics to multi-dimensional geometric clustering, this project uncovers hidden market segments to help financial institutions optimize underwriting limits and risk-adjusted product marketing.

---

## 🚀 The Data & Engineering Pipeline
To ensure strict mathematical integrity before running distance-based algorithms, a robust data hygiene pipeline was built:
* **Data Hygiene:** Preserved 183 latent missing values in savings accounts by mapping them to an 'unknown' category, reflecting real-world applicants without active secondary depository relationships.
* **Feature Standardization:** Utilized `StandardScaler` to normalize high-magnitude metrics (Credit Amount) and low-magnitude metrics (Age) into a unified Gaussian normal space, forcing the algorithm to weigh all vectors equally.
* **Clustering Optimization:** Executed K-Means Clustering ($K=3$) to partition 1,000 historical applicant records based on age, loan volume, and credit duration.

---

## 👥 Discovered Financial Personas

The algorithm isolated three highly distinct customer archetypes within the consumer pipeline:

### 🏢 1. Heavy Long-Term Borrowers (High Exposure)
* **Profile:** Average age ~35 | High credit amounts (Avg \$7,609) | Long repayment periods (Avg ~39 months).
* **Business Insight:** This is the highest-risk group. Their capital utilization is structural—likely for business ventures or major assets. Requires aggressive underwriting safeguards.

### 🌅 2. Mature Low-Risk Borrowers (Highly Stable)
* **Profile:** Average age ~52 | Modest credit amounts (Avg \$2,398) | Short repayment windows (Avg ~16 months).
* **Business Insight:** The ultimate "safe bet." These established individuals seek short-term liquidity rather than existential funding. Ideal candidates for premier pricing tiers.

### 🚀 3. Young Entry-Level Borrowers (High Volume)
* **Profile:** Average age ~30 | Low credit amounts (Avg \$2,207) | Short-term loans (Avg ~17 months).
* **Business Insight:** The structural bedrock of volume (58.7% of all applicants). These individuals borrow for immediate consumer lifestyle needs. They represent prime targets for long-term customer lifetime value conversion.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (`StandardScaler`, `KMeans`)
* **Visualization:** Seaborn, Matplotlib

---

## 📈 Key Visual Output
*The cluster analysis cleanly separates younger, short-term borrowers from high-exposure risk groups across explicit age and credit boundaries:*

![Customer Segmentation Plot](data/image_82f28e.png) 
*(Note: Replace this image path if you save your plot image directly inside your repository!)*
