# A/B Testing Analysis: Marketing Campaign Effectiveness

## Business Problem

A company wants to determine whether showing **advertisements (Ads)** leads to a higher **conversion rate** compared to showing **Public Service Announcements (PSA)**.

This analysis evaluates the effectiveness of both strategies using **statistical hypothesis testing** and exploratory data analysis.

The goal is to determine whether the advertisement strategy produces a **statistically significant increase in conversions**.

---

## Experimental Design

The dataset represents a randomized marketing experiment with two groups:

| Group | Description |
|------|------|
| Ad | Users exposed to advertisements |
| PSA | Users exposed to public service announcements (control group) |

The main metric used to evaluate performance is the **conversion rate**.

Conversion Rate = Conversions / Total Users

---

## Exploratory Data Analysis

### Conversion Rate by Experimental Group

The analysis shows that users exposed to **advertisements convert at a higher rate** than users exposed to PSA messages.

Observed conversion rates:

| Group | Conversion Rate |
|------|------|
| Ads | ~2.56% |
| PSA | ~1.79% |

This suggests that advertisement exposure increases the probability of conversion.

---

### Ads Exposure vs Conversion

![ads seen vs conv](https://github.com/user-attachments/assets/c88ad90a-6581-478f-858f-13bb9bdb1349)

Users who converted were typically exposed to **a higher number of advertisements** compared to users who did not convert.

This suggests that ad exposure may influence user behavior. However, extremely high exposure values appear as **outliers**, which is common in marketing datasets.

---

### Conversion Rate by Day

![conv day](https://github.com/user-attachments/assets/004606c2-ce86-4f52-8fd2-e3b32be89ac8)

Conversion rates vary depending on the day of exposure.

Key observations:

- **Monday shows the highest conversion rate**
- **Tuesday also performs well**
- **Weekend days tend to have slightly lower conversion rates**

This indicates that the **timing of campaigns may impact marketing performance**.

---

### Conversion Rate by Hour

![conv hour](https://github.com/user-attachments/assets/5fbd5b7b-dddd-4afd-be90-babed8be0bbe)

Conversion rates also vary depending on the hour of exposure.

Observations:

- Conversion rates increase throughout the day.
- The **highest conversion rates occur during afternoon and evening hours**.
- Early morning hours show the lowest conversion rates.

This suggests that **ad scheduling could be optimized to target peak conversion hours**.

---

## Statistical Hypothesis Testing

A **Two-Proportion Z-Test** was conducted to determine whether the difference in conversion rates between both groups is statistically significant.

### Hypotheses

**Null Hypothesis (H0)**  
The advertisement strategy does not change the conversion rate.

H0: p_ad = p_psa

**Alternative Hypothesis (H1)**  
The advertisement strategy increases the conversion rate.

H1: p_ad > p_psa

Significance level:

α = 0.05

---

## Z-Test Results

![ztest](https://github.com/user-attachments/assets/3617be2e-c181-4d08-aaea-bb2ca438aeb8)

Since the p-value is **far below the significance threshold of 0.05**, we reject the null hypothesis.

This indicates that the difference in conversion rates between the two groups is **statistically significant**.

---

## Confidence Interval

![Confidence interval](https://github.com/user-attachments/assets/5a736e91-5984-47f4-9eb9-9a5f3cf2768a)

A **95% confidence interval** was calculated for the difference in conversion rates between both groups.

95% Confidence Interval:

(0.00595 , 0.00943)

Interpretation:

We are 95% confident that the advertisement strategy increases the conversion rate by **between 0.6% and 0.94%** compared to the PSA strategy.

---

## Business Impact

The results suggest that the **advertisement strategy significantly improves conversion rates**.

From a business perspective:

- Advertisement exposure increases user engagement.
- The improvement in conversion rate is statistically significant.
- Optimizing ad timing (day and hour) could further improve campaign performance.

---

## Final Conclusion

This A/B test provides strong statistical evidence that **advertisements outperform public service announcements in driving conversions**.

Therefore, the company should consider implementing the **advertisement-based marketing strategy** as the primary marketing approach.

Additionally, further improvements could be achieved by focusing advertising efforts on **high-performing days and hours identified in the analysis**.
