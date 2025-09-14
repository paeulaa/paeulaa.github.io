# A/B Testing Case Study: Comparing Interface A vs. B  

## Introduction  
In this project, we explored how **interface design** (Interface A vs. B) and **task complexity** (easy vs. difficult) affect user performance. The dataset covered **38 participants**, segmented into four personas based on **gender** and **memory span**. We also factored in **cognitive traits** like verbal closure and flexibility of closure.  

<img src="images/A-B-testing-project/user segmentation.png?raw=true"/>  
<img src="images/A-B-testing-project/interfaceAB.png?raw=true"/>  

---

## Research Setup  
We analyzed the dataset in three phases:  

1. **Descriptive Statistics** – averages, distributions, and 95% confidence intervals.  
2. **T-tests** – testing statistical significance across conditions.  
3. **Correlation & ANOVA** – exploring relationships between fixation data, task duration, and memory span.  

Our key metrics:  
- **Task duration** (completion time in ms)  
- **Fixation count & fixation duration** (eye-tracking data)  

---

## Key Findings  

### 1. Persona-Level Insights  
Men consistently showed higher flexibility of closure than women, while participants with higher memory span tended to score slightly higher in verbal closure.  

<img src="images/A-B-testing-project/mean-sd-verbal-flexibility.png?raw=true"/>  
<img src="images/figure4-flexibility-closure.png?raw=true"/>  
<img src="images/figure5-verbal-closure.png?raw=true"/>  

---

### 2. Interface & Task Complexity  
Users achieved the **fastest completion times with Interface B on easy tasks**. Difficult tasks required more time overall, but there was no statistically significant difference between A and B under difficult conditions.  

<img src="images/figure6-mean-sd-taskduration.png?raw=true"/>  
<img src="images/figure7-histogram-taskduration.png?raw=true"/>  

---

### 3. Data Distributions Across Personas  
Performance varied across personas:  
- **Interface B (easy tasks)** → concentrated performance, narrow variance.  
- **Interface A (difficult tasks)** → wider variance, larger gaps between personas.  

<img src="images/figure8-boxplot-efforts.png?raw=true"/>  
<img src="images/figure9-scatter-verbal-flexibility.png?raw=true"/>  

---

### 4. Statistical Testing Results  
- **T-test (Easy A vs. Easy B):** Interface B significantly faster (p < .001).  
- **T-test (Difficult A vs. Difficult B):** No significant difference.  
- **T-test (Easy vs. Difficult in A):** Significant difference—difficult tasks clearly slower.  

<img src="images/figure10-confidence-interval.png?raw=true"/>  
<img src="images/figure16-mean-difference.png?raw=true"/>  

---

### 5. Eye-Tracking & Cognitive Traits  
We integrated fixation data to examine attention load. Strong correlation was observed:  
- More fixations → longer task durations (R² ≈ 0.86).  
- Log-transformed data normalized skewed distributions for statistical testing.  

<img src="images/figure18-histogram-taskduration-log.png?raw=true"/>  
<img src="images/figure20-histogram-fixationduration-log.png?raw=true"/>  
<img src="images/figure22-histogram-fixationcount-log.png?raw=true"/>  
<img src="images/figure23-scatter-fixation-taskduration.png?raw=true"/>  

---

### 6. ANOVA Results  
- **Interface** had a significant effect on both task duration and fixation duration.  
- **Memory span** alone was not a significant factor.  
- No significant interaction between interface and memory span.  

<img src="images/figure24-descriptive-taskduration.png?raw=true"/>  
<img src="images/figure25-anova-taskduration.png?raw=true"/>  
<img src="images/figure27-descriptive-fixationduration.png?raw=true"/>  
<img src="images/figure28-anova-fixationduration.png?raw=true"/>  

---

## Conclusion  
This study revealed how **interface efficiency is context-dependent**:  

- For **easy tasks**, Interface B provided significant speed advantages.  
- For **difficult tasks**, task complexity itself was the main bottleneck, regardless of interface design.  
- Cognitive traits like **flexibility of closure** influenced performance, though memory span showed limited impact.  

By combining **A/B testing with cognitive and eye-tracking analysis**, we gained a nuanced understanding of how interface design choices impact different user groups. These findings highlight that **effective design goes beyond surface-level comparisons**—it requires looking at task complexity, user traits, and attention load to truly optimize usability.  

