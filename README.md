# Bellabeat Smart Device Wellness Case Study
A data analytics case study examining smart device usage patterns (activity, sleep and heart rate) to guide Bellabeat's product and marketing strategy. Built with spreadsheet.  
links: [explore the cleaned datasets and pivot tables in the /data folder](data/)  
links: [view all exported chart graphics in the /visuals folder](visuals/)
## 1. Executive Summary & Business Task
Bellabeat, a high-tech manufacturer of health-focused smart products for women, wants to unlock new growth opportunities. 
**Goal:** Analyze smart device usage data to identify trends in daily activity, sleep, and heart rate, and apply those insights to guide Bellabeat's marketing strategy.

---

## 2. Data Sources & Limitations
* **Dataset:** FitBit Fitness Tracker Data (CC0: Public Domain, via Mobius on Kaggle).
* **Scope:** 33 consenting users over a 31-day period, covering daily activity, minute-by-minute sleep logs, and 5-second interval heart rate records.
* ### Tables analyzed:
* Daily activity merged data
* Heart rate summary data
* Minute sleep_merged
* Sleep Day_merged 
* **Key Limitations:**
* Heart rate data is only available for a subset of **14 out of 33 users**.
* Demographic data (age, location) is omitted, requiring careful framing when applying findings to Bellabeat's female-focused customer base.

---

## 3. Tools
* **Spreadsheets (Google Sheets):** Data cleaning, deduplication, timestamp formatting, and pivot table aggregations and visualization.

---
## 4. Data Preparation  
* **DATA CLEANING:** Checked for duplicate rows, Fixed data types, Checked for missing data.
* **ANALYSIS: Calculated columns and Pivots**
* <ins>Daily activity merged - Calculated</ins>
* ***Total active minutes*** addition of very, fairly and lightly active minutes
* ***Ratio of active to sedentary minutes*** total active minutes divided by sedentary minutes
* ***Pivot 1*** summarized the table by Sum of Total steps and Sum of Calories burned of each user.
* ***Pivot 2*** summarized again by the Average of Total active and Sedentary minutes of each user.

* <ins>Heart rate summary data - Calculated</ins>
* ***Hour*** hour of the day each heartrate was measured, extracted from the date column
* ***Pivot 1*** summarized the table by the average, max and min value of the heartrate for each user 
* ***Pivot 2*** summarized by the average heartrate for each hour of the day for each user

* <ins>Minutes Sleep_merged - Calculated</ins>
* ***Pivot*** summarized by the percentage of sleep state for each user (1=asleep, 2=restless, 3=awake)

* <ins>Sleep Day_merged - Calculated</ins> (2 variants, one with complete data, other with outlier removed)
* ***Total Sleep Latency*** which is total time awake in bed. (Total time in bed - Total Minutes Asleep)
* ***Sleep Efficiency*** (Total time asleep divided by the Total time in bed multiplied by 100)
* ***Pivot 1*** summarized by the average sleep latency and average sleep efficiency for each user
* ***Pivot 3*** summarized by the average of sleep latency and average sleep against Total sleep record (1,2 and 3 fragments of sleep) 

---
                               
* ## 5. Key Findings
* ![Average_Sleep_Latency_(minutes)_vs._Average_Sleep_Efficiency_by_user_Id](Visuals/Average_Sleep_Latency_(minutes)_vs._Average_Sleep_Efficiency_by_user_Id.png)
* Lesser ***Sleep latency***, which is time spent awake in bed could be seen to cause a higher ***Sleep Efficiency*** and users with high sleep latency had a drop in their sleep efficiency.
* Last 2 user IDs had a very large sleep latency so they were treated as outliers.
* ![Average_of_sleep_latency_vs._Average_of_sleep_efficiency](Visuals/Average_of_sleep_latency_vs._Average_of_sleep_efficiency.png)
* The same chart with ***outliers*** removed, it could be seen that users with slightly elevated sleep latency still got a decent sleep with sleep efficiency above ***85%***
* ![Impact_of_Total_Sleep_record_on_Sleep_Latency_and_Efficiency](Visuals/Impact_of_Total_Sleep_record_on_Sleep_Latency_and_Efficiency.png)
* ***Total sleep record*** of ***2*** had the highest sleep latency and the lowest ***Sleep efficiency***. Total sleep record of 3 had almost the same sleep latency as 1 but it has the highest sleep efficiency.
* ![Impact_of_Total_Sleep_record_on_Sleep_Latency_and_efficiency_1](Visuals/Impact_of_Total_Sleep_record_on_Sleep_Latency_and_efficiency_1.png)
* With the ***outliers*** removed ***Total sleep record*** of ***3*** had the highest sleep latency and also the highest sleep efficiency.

  ---
  
* ![Average_Daily_Sedentary_vs._Active_Minutes_by_User_Id](Visuals/Average_Daily_Sedentary_vs._Active_Minutes_by_User_Id.png)
* **Sedentary Dominance:** Users spend the vast majority of their tracked time sedentary, directly correlating with lower sleep efficiency and longer sleep latency.
* ![Total_steps_vs._Total_Calories_Burned](Visuals/Total_steps_vs._Total_Calories_Burned.png)
* There appears to be a positive relationship between the ***total steps*** and the ***calories burned*** 
---  
![Sleep_State_Distribution_by_User_Id](Visuals/Sleep_State_Distribution_by_User_Id.png)  
* Higher percentage of the ***sleep state*** of the users shows they were asleep rather than awake or restless.

* ---
![Heart_rate_range_by_user](Visuals/Heart_rate_range_by_user.png)  
* Users had the same baseline or resting heartrate but with varied peak heartrates

## 5. Strategic Recommendations
1. **Smart Inactivity Nudges:** Introduce gentle, timed movement prompts in the Bellabeat app during prolonged sedentary blocks—especially in the late afternoon and evening—to support cardiovascular recovery.
2. **Guided Wind-Down & Sleep Routines:** Pair sleep latency tracking with personalized evening wind-down reminders to improve overall sleep efficiency.
3. **Targeted Marketing Campaigns:** Position Bellabeat products (like the Ivy health tracker or Time watch) not just as step counters, but as holistic stress and recovery companions for busy professionals.

---

## 6. Repository Structure
* `/data` — Cleaned datasets and summary tables.
* `/scripts` — SQL queries and Python scripts used for analysis.
* `/visuals` — Exported charts (Sleep Latency vs. Efficiency, Hourly Heart Rate Trends).
