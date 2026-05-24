# Project Brief: The "Last Mile" Logistics Auditor

**Candidate:** Uwayo Neeve Celia
**Client:** Veridi Logistics (Global E-Commerce Aggregator)
**Deliverable:** Public Dashboard, Code Notebook & Insight Presentation

---

### A. The Executive Summary

An audit of 96,470 delivered orders from the Olist Brazilian E-Commerce dataset reveals that 8.1% of deliveries failed to meet their estimated delivery date, directly causing a measurable drop in customer satisfaction. Orders delivered on time averaged a review score of 4.29/5, while "Super Late" orders (more than 5 days late) averaged only 1.79/5 - a 58% collapse in customer sentiment. The problem is not nationwide: northeastern states, particularly Alagoas (AL) at 23.9% late rate and Maranhão (MA) at 19.7%, are disproportionately affected, suggesting a regional logistics capacity gap rather than a systemic failure. Immediate investment in last-mile infrastructure in the northeast is recommended.

### B. Project Links

- **Link to Notebook:** https://colab.research.google.com/drive/1YWvtnbBMcxGdz3ncTvTTZRpVgGqZB2MY?usp=sharing
- **Link to Dashboard:** https://public.tableau.com/app/profile/neeve.celia.uwayo/viz/VeridiLogisticsDeliveryPerformanceAudit_17796307690420/Dashboard1#1
- **Link to Presentation:** A link to a short slide deck (PDF/PPT) AND (Optional) a 2-minute video walkthrough (YouTube) explaining your results.

### C. Technical Explanation

### Data Cleaning
- Loaded 5 CSV files from the Olist Brazilian E-Commerce dataset
- Deduplicated the reviews table on `order_id` before joining to prevent row explosion
- Converted all date columns to datetime format
- Filtered to delivered orders only (96,470 rows) and dropped rows with missing delivery dates
- Created `Days_Difference` = estimated delivery date minus actual delivery date
- Classified orders as "On Time" (>=0 days), "Late" (-5 to 0 days), or "Super Late" (< -5 days)

### Candidate's Choice — Monthly Late Rate Trend
I added a dual-axis chart showing order volume (blue area) vs. % late deliveries 
(red line) over time. This feature adds specific business value because it reveals 
whether the late delivery problem is seasonal (fixable with temporary capacity 
increases) or structural (requiring long-term infrastructure investment). 
The data shows a spike to ~21% late rate in March 2018 coinciding with peak order 
volume, indicating the logistics network cannot scale with demand surges — 
a critical finding for capacity planning.

---

## 🛑 CRITICAL: Pre-Submission Checklist

**Before you submit your form, you MUST complete this checklist.**

> ⚠️ **WARNING:** If you miss any of these items, your submission will be flagged as "Incomplete" and you will **NOT** be invited to an interview.
>
> **We do not accept "permission error" excuses. Test your links in Incognito Mode.**

### 1. Repository & Code Checks

- [ ] **My GitHub Repo is Public.** (Open the link in a Private/Incognito window to verify).
- [ ] **I have uploaded the `.ipynb` notebook file.**
- [ ] **I have ALSO uploaded an HTML or PDF export** of the notebook.
- [ ] **I have NOT uploaded the massive raw dataset.** (Use `.gitignore` or just don't commit the CSV).
- [ ] **My code uses Relative Paths.**

### 2. Deliverable Checks

- [ ] **My Dashboard link is publicly accessible.** (No login required).
- [ ] **My Presentation link is publicly accessible.** (Permissions set to "Anyone with the link can view").
- [ ] **I have updated this `README.md` file** with my Executive Summary and technical notes.

### 3. Completeness

- [ ] I have completed **User Stories 1-4**.
- [ ] I have completed the **"Candidate's Choice"** challenge and explained it in the README.

**✅ Only when you have checked every box above, proceed to the submission form.**

---
