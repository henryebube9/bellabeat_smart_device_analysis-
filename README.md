# Bellabeat Smart Device Wellness Case Study
A data analytics case study examining smart device usage patterns (activity, sleep and heart rate) to guide Bellabeat's product and marketing strategy. Built with spreadsheet. 

## 1. Executive Summary & Business Task
Bellabeat, a high-tech manufacturer of health-focused smart products for women, wants to unlock new growth opportunities. **Goal:** Analyze smart device usage data to identify trends in daily activity, sleep, and heart rate, and apply those insights to guide Bellabeat's marketing strategy.

---

## 2. Data Sources & Limitations
* **Dataset:** FitBit Fitness Tracker Data (CC0: Public Domain, via Mobius on Kaggle).
* **Scope:** 33 consenting users over a 31-day period, covering daily activity, minute-by-minute sleep logs, and 5-second interval heart rate records.
* **Key Limitations:**
* Heart rate data is only available for a subset of **14 out of 33 users**.
* Demographic data (age, gender, location) is omitted, requiring careful framing when applying findings to Bellabeat's female-focused customer base.

---

## 3. Tools & Methodology
* **Spreadsheets (Google Sheets):** Data cleaning, deduplication, timestamp formatting, and pivot table aggregations and visualization.

---

## 4. Key Findings
* **Sedentary Dominance:** Users spend the vast majority of their tracked time sedentary, directly correlating with lower sleep efficiency and longer sleep latency.
* **Cardiovascular Strain:** Among the 14 users with heart rate data, individuals with higher sedentary minutes exhibit elevated evening heart rate patterns, signaling suboptimal daily recovery.
* **Weekend vs. Weekday Shifts:** Activity levels and sleep consistency fluctuate noticeably between workdays and weekends, indicating a need for adaptive user engagement.

---

## 5. Strategic Recommendations
1. **Smart Inactivity Nudges:** Introduce gentle, timed movement prompts in the Bellabeat app during prolonged sedentary blocks—especially in the late afternoon and evening—to support cardiovascular recovery.
2. **Guided Wind-Down & Sleep Routines:** Pair sleep latency tracking with personalized evening wind-down reminders to improve overall sleep efficiency.
3. **Targeted Marketing Campaigns:** Position Bellabeat products (like the Ivy health tracker or Time watch) not just as step counters, but as holistic stress and recovery companions for busy professionals.

---

## 6. Repository Structure
* `/data` — Cleaned datasets and summary tables.
* `/scripts` — SQL queries and Python scripts used for analysis.
* `/visuals` — Exported charts (Sleep Latency vs. Efficiency, Hourly Heart Rate Trends).
