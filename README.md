# 🚀 Hypothesis Testing; TikTok Verified vs Unverified: 

**Statistical Proof of Engagement Bias on TikTok — Google Advanced Data Analytics**

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![SciPy](https://img.shields.io/badge/SciPy-1.12+-8C8C8C?style=flat-square&logo=scipy&logoColor=white)](https://scipy.org)
[![Google Advanced Data Analytics](https://img.shields.io/badge/Google%20Advanced%20Data%20Analytics-Certified-4285F4?style=flat-square)](https://www.coursera.org/professional-certificates/google-advanced-data-analytics)

**Status**: Completed | **Portfolio Highlight** | **From EDA to Statistical Rigor**

---

### 📌 Executive Summary

**Unverified accounts dramatically outperform verified ones in reach.**

A two-sample t-test on 19,084 TikTok videos shows a **statistically significant difference** in mean video view counts:

- **Unverified accounts**: **265,664** average views  
- **Verified accounts**: **91,439** average views  

**t-statistic = 25.50** | **p-value = 2.61 × 10⁻¹²⁰** (<< 0.05)

We **reject the null hypothesis** with overwhelming confidence.

This is not sampling error — unverified creators achieve **~2.9× higher engagement**. The finding provides TikTok’s Data Science and Trust & Safety teams with rigorous statistical evidence that verification status is a strong behavioral signal.

---

### 🎯 Business Problem & Impact

TikTok needed definitive statistical validation:  
**Do videos from verified and unverified accounts have significantly different average view counts?**

This hypothesis test delivers:
- Quantified proof of engagement disparity
- Clear p-value for executive reporting
- Strong foundation for claim-detection modeling

**Strategic value**: Enables data-driven decisions on content moderation, algorithmic fairness, and platform integrity.

---

### 📊 Dataset

- **Source**: TikTok video claims dataset (Google Advanced Data Analytics)
- **Original size**: 19,382 videos
- **Cleaned size**: 19,084 videos (298 rows dropped due to missing values)
- **Key Variables**:
  - `verified_status` (verified / not verified)
  - `video_view_count` (primary metric)
  - Supporting: `claim_status`, `author_ban_status`, engagement metrics

---

### 🛠️ Tools & Technologies

- **Data Manipulation**: pandas, NumPy
- **Statistical Testing**: SciPy (`ttest_ind`)
- **Framework**: PACE (Plan → Analyze → Construct → Execute)
- **Environment**: Jupyter Notebook

---

### 🧭 Methodology (PACE Framework)

**Plan**  
Research Question: Do videos from verified and unverified accounts have significantly different average view counts?

**Analyze**  
- Computed descriptive statistics  
- Handled missing values  
- Calculated group means

**Construct**  
- Two-sample independent t-test (Welch’s t-test, unequal variances)  
- Significance level α = 0.05

**Execute**  
- p-value = 2.6088823687177823e-120  
- **Decision**: Reject null hypothesis

---

### 📈 Key Statistical Results

| Metric                  | Unverified       | Verified       | Difference      |
|-------------------------|------------------|----------------|-----------------|
| Mean video views        | 265,664          | 91,439         | **+174,225**    |
| Sample size             | 17,800+          | 1,284          | —               |
| t-statistic             | 25.50            | —              | —               |
| p-value                 | **2.61 × 10⁻¹²⁰** | —             | **Highly significant** |

---

### 🔥 Key Insights

1. **Statistical slam-dunk** — One of the smallest p-values in social media analytics. Verification status is a powerful predictor of engagement behavior.
2. **Engagement inequality** — Unverified accounts drive nearly 3× the views, raising important questions about algorithmic amplification and content quality.
3. **Early moderation signal** — High-view unverified videos align with elevated claim and ban risk.
4. **Production-ready inference** — Clean, reproducible hypothesis test ready for integration into TikTok’s modeling pipeline.

---

### 📌 Conclusion & Strategic Recommendations

**Key takeaway**: There is a real, statistically significant difference in average view counts between verified and unverified accounts on TikTok (p << 0.001). Unverified creators consistently achieve far greater reach.

**Recommendations**:
- Add `verified_status` as a high-weight feature in the upcoming claim-classification model
- Investigate root causes (clickbait, spam, or organic virality) through further segmentation
- Proceed with logistic regression to predict claim risk using verified status and engagement metrics
- Consider platform experiments to test the impact of verified-content promotion on trust metrics
