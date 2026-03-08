# Airbnb Market Demand & Conversion Analysis 🏠📊

## 📋 Project Overview
This project explores user search behavior and host response patterns on Airbnb. By analyzing search logs and the resulting conversion funnel, I identified a significant structural mismatch between traveler demand and available inventory. The project provides data-driven strategies to close market gaps and increase overall booking volume.

[Project Data & Description Link](https://platform.stratascratch.com/data-projects/market-analysis-dublin) 

---

## 🛠 Data Cleaning & Methodology
To ensure high data integrity, the raw dataset was refined through a two-stage pre-processing pipeline:

1.  **Session Consolidation:** Prioritized high-intent searches. For users with multiple search entries, undated observations were removed if the user eventually provided specific check-in/out dates.
2.  **Outlier Mitigation:** Calculated search frequency per user and removed the top **1%** of the distribution to eliminate noise from bots, scrapers, or non-typical power users.

---

## 🔍 Key Findings

### 1. The "Weekend Warrior" Profile
* **Duration:** **86%** of all searches are for short-term stays (1–7 nights). The most requested duration is **2 nights (22%)**.
* **Temporal Peaks:** Demand is heavily concentrated on "weekend-adjacent" stays:
    * *Friday – Sunday (2 nights)* is the single most popular window (**10.12%**).

### 2. Demographic & Pricing Sensitivity
* **Group Size:** **74%** of searches are for **1–2 guests**.
* **Budget:** 39% of users use a "Max Price" filter, with a **median cap of €130/night**. 

### 3. Acceptance Rate Bottlenecks
Despite high demand for short stays, host behavior creates a significant conversion bottleneck:
* **Duration Penalty:** 1-night stays have only a **42% acceptance rate**, compared to **50%+** for 3-night stays.
* **Lead-Time Penalty:** Acceptance rates drop from **50%** (8+ days out) to just **25%** for same-day requests.



---

## 📈 Conversion Funnel
The funnel analysis reveals that the primary drop-off occurs between the "Contact" and "Accepted" stages, particularly for last-minute and short-duration bookings.

| Stage | Users | Conversion (Step) |
| :--- | :--- | :--- |
| **Total Searchers** | 18,441 | - |
| **Contacted Host** | 2,988 | 16.20% |
| **Accepted by Host** | 2,275 | 78.42% |
| **Completed Booking** | 1,890 | 83.08% |

---

## 💡 Strategic Recommendations

* **Supply Acquisition:** Priority should be given to onboarding **City Centre** units (targeted by 81% of filtered searches) optimized for **1–2 guests**.
* **Instant Book Promotion:** To capture the last-minute market (where acceptance is as low as 25%), the platform should incentivize hosts to enable **Instant Book** for weekend windows.
* **Pricing Anchor:** Maintain a high volume of inventory around the **€130 price point** to align with the median search filter.

---

## 💻 Tech Stack
* **Python:** Data cleaning and aggregation.
* **Pandas, NumPy, Seaborn:** Core data manipulation and visualization.
* **Statistical Testing:** Used $p$-value analysis to validate the significance of lead-time impact on acceptance rates.
