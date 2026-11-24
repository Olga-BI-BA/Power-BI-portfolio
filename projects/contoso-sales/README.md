# Contoso Sales Performance Report 📊

An enterprise-grade Power BI report designed to monitor key performance indicators (KPIs), product and regional efficiency.

> **Project Status:** Completed 🚀  
> **Tech Stack:** Power BI Desktop, SQL, Power Query (M Language), DAX, Figma, Git LFS.

**Note on the data:** Contoso is a synthetic dataset. It is well suited for demonstrating modelling, DAX and dashboard design, but it may not reflect realistic business patterns. The findings below illustrate the analytical approach.

## 📑 Contents

- [Business Question](#-business-question-new)
- [Report Screenshots & Insights](#-report-screenshots)
  - [1. Global Sales Overview](#1-main-page-global-sales-overview)
  - [2. Regional Trends](#2-regional-trends-page)
  - [3. Products. What Sells](#3-products-what-sells)
  - [4. Scenario Analysis](#4-scenario-analysis-page)
  - [5. Daily Cockpit](#5-daily-cockpit-page)
- [Interactivity](#-interactivity-new)
- [Data Model and DAX](#-data-model-and-dax-new)
- [Data Limitations](#-data-limitations)
- [Files](#-files)


  
## 🎯 Business Question 

**Role:** BI analyst preparing a performance review for the CEO, CFO, Commercial Director and regional managers.

**Scenario:** global net revenue is falling. Leadership needs to know *what* is shrinking, *where*, and *what to do about it*. The report is built around four decisions:

1. **Where is revenue lost?** Which regions, channels and categories drive the 2025 decline.
2. **Where is the money still being made?** Which countries and products grow, and whether they are big enough to matter.
3. **What to do with the product range?** Which subcategories to protect, harvest, grow or phase out.
4. **Is a new discount policy worth it?** Under which demand and cost assumptions it adds profit.

A fifth page, the **Daily Cockpit**, supports day-to-day management: is the month on track against its forecast?

## 📷 Report Screenshots and Insights

### 1. Main Page: Global Sales Overview
This page serves as the summary of short-term trends for executive management, offering a high-level performance overview across all global markets, sales channels, and product categories.

>Technical Features: Field Parameters, DAX, Conditional Formatting, Cross Filtering, Bookmarks & Buttons, Visuals, Dynamic RLS (by user email)

<img width="1504" height="843" alt="Animation" src="https://github.com/user-attachments/assets/ebe2197b-f3b8-467c-b6c6-5bc12348b65f" />


**📌 Executive Summary**  
Overall revenue decline hits most markets and channels. Strong growth in small categories hasn't offset revenue lost from large categories shrinking, resulting in an overall global revenue drop of **`-9.05%`**.

**Macro Regions**  
 **Asia** is the only region showing growth (`+8.81%`), heavily driven by **China** (the second-largest market, up `+6%`) and **Japan** (`+16.77%`), with explosive spikes in Thailand (`+64%`), South Korea (`+61%`), and Bhutan (`+55%`). **United States**, the primary and largest market, crashed by `-15.85%`, suffering a significant loss in global revenue share, which dropped from **56.7% down to 52.5%** in 2025. All markets across **Europe** continue to experience stagnation, resulting in an overall decline of `-9.22%`.

**Distribution Channels**  
**Online** is the only growing channel globally (`+1.46%`), primarily because it serves as the main distribution channel in China and maintained stable growth over the 2024–2025 period. **Store** revenue fell the sharpest (`-13.35%`), which was directly caused by the overall sales decline in the US market, where brick-and-mortar stores typically generate **58%** of total revenue.

**Product Categories**  
 **Home Appliances**, **Computers**, and **Cameras & Camcorders** (core drivers)form the financial backbone of the business, accounting for **75.7%** of total global revenue.
 Critically, two of these core backbone categories (**Home Appliances** and **Cameras & Camcorders**) became the top losers in 2025, with both shrinking by approximately `-22%`. Strong growing categories like **Games & Toys** (`+56.54%`) and **Audio** (`+30.69%`) (growth outliers) showed strong momentum but contribute barely **\$0.1bn** combined. This minor volume was completely insufficient to offset the heavy losses from the shrinking core segments, so overall revenue is still down 9.05%


---
### 2. Regional Trends Page

The **Regional Trends** page is built to provide regional managers and stakeholders with deep visibility into geographical performance. It effectively answers the following critical business questions:

*   **Which markets are driving the company's global revenue, and which are shrinking?**
*   **What is the exact financial impact in revenue and profit across different countries?**
*   **How does seasonal sales performance vary across major continents and countries throughout the year?**
*   **What are the operational footprints within specific countries?**
*   **How do these regional trends shift when filtering by specific years or distribution channels?**


  >Technical Features: Bookmarks, Buttons, Filtering, Visual Interactions, DAX, Visual Calculations, Conditional Formatting, Dynamic Images by URL

<img width="1511" height="848" alt="Page Regional Trends 2" src="https://github.com/user-attachments/assets/0f5dd5b5-7c94-43bb-abd7-6e1464be5377" />

---
### 3. Products. What Sells
This page provides a comprehensive analysis of product performance, sales distribution, and profitability. It is designed to help product managers, inventory planners, and executives identify where to invest or divest cash (BCG framework) and how to optimize cash flow and warehouse stock (ABC-XYZ matrix). It achieves this by highlighting top-revenue product segments, evaluating growth trajectories, assessing demand predictability, and analyzing the overall product mix.

>Technical Features: Bookmarks, Buttons, Top N/ Bottom N Filtering, Visual Interactions, DAX, Visual Calculations, Conditional Formatting, Dynamic Titles, Visuals
>
<img width="1525" height="859" alt="Page Products 3" src="https://github.com/user-attachments/assets/1c7dc7ca-a552-4e61-96ae-69942ff30ef3" />


**📌 Global BCG Matrix Insights & Recommendations**

**Stars (Business Drivers)**
* **Key Subcategory:**  Laptops are single-handedly keeping the company afloat during this market downturn.
* **Strategic Recommendation: Protect and Maximize**  
  Ensure flawless supply chain continuity, secure adequate inventory levels, and prioritize cash allocation for this segment. Shift any underutilized marketing budgets from stagnant categories directly into Laptops to sustain growth.

**Cash Cows (Protective Assets in Decline)**
* **Key Subcategories:** **Camcorders** (`-35.70%`),**Projectors & Screens** (`-14.83%`), **Home Theater Systems** (`-15.50%`),**Washers & Dryers** (`-54.21%`),**Digital SLR Cameras** (`-15.86%`)
* **Strategic Recommendation: Harvest and Optimize**  
  Implement strict inventory controls and reduce safety stocks for rapidly declining segments (like washers and video cameras) to prevent cash from being frozen in slow-moving warehouse stock.

**Question Marks (Future Growth Pockets)**
* **Key Subcategories:**  **Cell Phones Accessories** (`+153.87%`),**Download Games** (`+120.82%`),**Cameras & Camcorders Accessories** (`+105.30%`),**Fans** (`+65.56%`),**Computers Accessories** (`+35.23%`), **Televisions** (`+20.44%`),**Monitors** (`+11.29%`).
  These categories are successfully capturing current consumer trends. Mobile and PC accessories are expanding rapidly, but because they currently account for a very low share of sales (**under 2%**), they do not yet impact the total bottom line.
* **Strategic Recommendation: Selective Scaling via Cross-Selling**  
  Focus heavily on high-margin co-products like **Cell Phones Accessories** and **Computers Accessories** to expand their market share.

**Dogs (Inventory Ballast)**
* **Key Subcategories:**  
  * **Desktops** (`-46.60%`),   **Water Heaters** (`-33.80%`),  **Movie DVDs** (`-29.79%`), **Air Conditioners** (`-21.17%`), **Lamps** (`-18.34%`).
  * These products provide neither growth nor volume, actively burning working capital and occupying valuable warehouse space. Stationary Desktops are completely losing the battle to mobile laptops, and Movie DVDs represent an obsolete market.
* **Strategic Recommendation: Aggressive Rationalization / Divestment**  
  **Completely discontinue Movie DVDs.** Execute aggressive promotional clearances or flash sales for **Desktops** and **Water Heaters** to quickly liquidate remaining stock and free up warehouse capacity.


---

### 4. Scenario Analysis Page
The Scenario Analysis is a financial simulation model to evaluate KPIs for the following business goal: increase of global market share via implementation of a new discount policy.  

**Data methodology note**:
*Because this portfolio project utilizes a synthetic dataset, it lacks the behavioral patterns and granular transaction history required to statistically calculate a true price elasticity coefficient (the exact relationship between discount depth and demand growth). Consequently, the dashboard is designed as a deterministic simulation tool. It allows stakeholders to manually input their own strategic assumptions or market expectations regarding demand elasticity to instantly visualize the potential financial outcomes.*


>Technical Features: What-If Parameters, DAX, Conditional Formatting, Charts 

<img width="1521" height="853" alt="Page Regional Trends 2" src="https://github.com/user-attachments/assets/4767cdd8-5b79-465d-a188-2cfa5dd959db" />


**📌Scenario Evaluation: impact analysis of 4% Discount and 9% Demand Growth Assumptions**

The core insight reveals that implementing **a new discount policy resulting in a 4% discount depth** (increased from the baseline of 1.68%), which is projected to expand sales volume and **increase demand by 9%** (stakeholders' assumption), will result in a net profit increase only if the company successfully keeps cost-push inflation or **supplier price growth under 2-2.5%**.

As shown in the simulated scenario, allowing cost inflation to escalate to 3.00% triggers a 12.27% jump in COGS (+$196M), completely outpacing the 5.08% expansion in Net Revenue (+$188M) and **resulting in a 0.40% drop in Gross Profit**.

---
### 5. Daily Cockpit Page
The Daily Cockpit serves as an operational executive command center designed for CEOs, CFOs, and Commercial Directors to monitor daily performance against long-term strategic forecasts. It allows leadership to instantly see if the business is on track to meet monthly commitments or if immediate corrective action is needed to fix performance gaps.

>Technical Features: Field Parameters, DAX, Conditional Formatting, Cross Filtering, Charts, Dynamic Titles 

<img width="1526" height="854" alt="Page Daily CockPit 5" src="https://github.com/user-attachments/assets/36c281a1-6402-430d-8aba-6f63f49e8691" />

---

## 🕹️ Interactivity 

- Cross-filtering between visuals on every page.
- Field-parameter switches for metric (net revenue, gross profit, active SKUs, YoY growth), view (channel or macro region) and level (category or country).
- Year buttons and bookmark-driven toggles (Growing / Declining, Trends / Details, Category / Global ABC-XYZ).
- Dynamic titles and insight text that follow the current selection.
- What-if sliders on the Scenarios page (discount, demand increase, unit cost).
- Country cards with dynamic flags loaded by URL.

---

## 🧱 Data Model and DAX 

- **Data preparation (SQL):** the data was prepared with SQL queries before it was loaded into Power BI.
- **Dynamic row-level security (RLS):** access is restricted by region and store, based on the signed-in user's email (`Security_Region_RLS`, `Security_Store_RLS`).
- **Star schema** with a sales fact and a sales-territory (region and country) dimension at its core.
- **Facts:** `fact Sales`, `fact Inventory`.
- **Dimensions:** `dim Calendar`, `dim Product`, `dim Store`, `dim SalesTerritory`, `dim Promotion`, `dim Channel`, `dim Currency`, `dim Geo`.
- **Classification tables:** `XYZ Classification` and `ABC XYZ Classification`; ABC and ABC-XYZ labels are also stored on `dim Product`.
- **Field parameters and what-if tables:** metric selection, date group, category / country and product level; scenario tables for discount, demand, price and unit cost.
- **Measures** sit in one `_Measures` table, grouped by purpose:
  - core metrics (net revenue, gross profit, gross margin, discount depth, units sold, active SKUs);
  - prior-year and YoY measures (value, %, gain/loss);
  - shares of revenue and profit, and subcategory share;
  - monthly forecast and forecast versus prior year;
  - scenario measures (net revenue, COGS, gross profit, versus fact 2025);
  - conditional-formatting (`CF …`) and icon (`viz …`) measures;
  - dynamic titles and insight text.
- **Techniques:** time intelligence, ABC-XYZ classification, Pareto (cumulative share) analysis, what-if simulation, forecast to month end, visual calculations.

---

## ⚠️ Data Limitations 

- The dataset is **synthetic**. It does not contain the behaviour needed to estimate a real price elasticity, so the Scenarios page is a deterministic simulation (see the methodology note above).
- Findings describe 2025 against 2024 unless a page says otherwise. Screenshots with another year selected show different percentages.

---

## 🗂️ Files 

| Path | Content |
|---|---|
| `powerbi/contoso-sales.pbix` | The full report (stored with Git LFS) |
| `screenshots/` | One animated preview per page |
