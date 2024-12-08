## Mobile Gaming A/B Testing Analysis

**Cookie Cats** is a mobile puzzle game developed by Tactile Entertainment. It's a "connect three" style puzzle game where players need to connect tiles of the same color to clear the board and win the level.<br>


[![YouTube](https://img.shields.io/badge/YouTube-Click_to_watch-red?logo=youtube)](https://www.youtube.com/embed/GaP5f0jVTWE?si=YNYwm3SSV6Z57LhD)

Cookie Cats has **a monetization strategy- progression gates.** These gates, strategically placed in certain levels, gets the player to either wait or make an in-app purchase- in order to keep playing the game and move-up in the game levels.<br>
This mechanic not only drives revenue but also aims to enhance the player’s enjoyment by preventing burnout.

In the **current settings**, the first gate is located at level 30.<br>
<h4>A question rises- can we increase the retention if we put the gate in another location?</h4>


This repository contains an analysis of an A/B test conducted on a mobile game to evaluate the impact of two game versions (`control` and `test`) on player retention. The analysis focuses on 1-day and 7-day retention metrics to determine whether the observed differences between the two groups are statistically significant.

---

## **Repository Structure**

### **Files**
1. **`AB test analysis- mobile game.ipynb`**:
   - A Jupyter Notebook containing the complete A/B testing analysis.
   - Includes data preprocessing, statistical tests, and visualizations.
   - Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`.

2. **`cookie_cats1.xlsx`**:
   - A cleaned dataset with user retention data for analysis.
   - Includes data preprocessing, statistical tests, and visualizations.

---

## **Project Objectives**
1. Assess the effect of game version changes on player retention.
2. Use statistical methods (Z-Test for proportions and Bootstrapping) to evaluate differences in retention rates.
3. Present findings using clear and actionable visualizations.

---

## **Dataset Description**
The dataset contains the following columns:
- **`userid`**: A unique identifier for each player.
- **`version`**: Game version (`control` = gate at level 30, `test` = gate at level 40).
- **`sum_gamerounds`**: Total game rounds played during the first week after installation.
- **`retention_1`**: Whether the player returned to the game 1 day after installation (`TRUE`/`FALSE`).
- **`retention_7`**: Whether the player returned to the game 7 days after installation (`TRUE`/`FALSE`).

---

## **Key Findings**

### **1-Day Retention**
- **Retention Rates**:
  - Control: 44.78%
  - Test: 44.18%
- **Statistical Results**:
  - Z-Statistic: 1.823
  - P-Value: 0.068 (not significant at $\alpha$ = 0.05).
- **Conclusion**:
  - No statistically significant difference in 1-day retention between groups.

### **7-Day Retention**
- **Retention Rates**:
  - Control: 19.0%
  - Test: 18.2%
- **Statistical Results**:
  - Z-Statistic: 3.135
  - P-Value: 0.002 (significant at $\alpha$ = 0.05).
- **Conclusion**:
  - The test group shows a statistically significant drop in 7-day retention, indicating reduced long-term player engagement.
