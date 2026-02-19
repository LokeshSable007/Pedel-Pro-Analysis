<h1 align="center">Pedel Pro Sales Analysis</h1>

> **Dataset:** Multi-table relational database &nbsp;|&nbsp; **Records:** 9 tables, 1,615 orders, 4,722 line items &nbsp;|&nbsp; **Period:** Jan 1, 2016 – Dec 28, 2018 &nbsp;|&nbsp; **Locations:** 3 Stores across USA

---

## Table of Contents

1. [Client Background](#1-client-background)
2. [Northstar Metrics](#2-northstar-metrics)
3. [Executive Summary](#3-executive-summary)
4. [Data Structure & ERD](#4-data-structure--erd)
5. [Insight Deep-Dive](#5-insight-deep-dive)
   - [5.1 Sales Trends](#51-sales-trends)
   - [5.2 Category Performance](#52-category-performance)
   - [5.3 Brand Analysis](#53-brand-analysis)
   - [5.4 Store Performance](#54-store-performance)
   - [5.5 Product Analysis](#55-product-analysis)
   - [5.6 Customer Geography](#56-customer-geography)
   - [5.7 Inventory & Stock Analysis](#57-inventory--stock-analysis)

---

<h1 align="center">1. Client Background</h1>

**BikeStores** is a regional bicycle retail chain operating three store locations across the United States: Santa Cruz Bikes (California), Baldwin Bikes (New York), and Rowlett Bikes (Texas). Established in 2016, the company specializes in selling premium bicycles and accessories across seven product categories — from children's bikes and cruisers to high-end mountain bikes, road bikes, and electric bikes.

The company's product catalog spans **321 unique bicycle models** from **9 major brands** including Trek, Electra, Surly, Heller, and others. Over the nearly three-year operational period (January 2016 through December 2018), BikeStores has built a customer base of **1,445 unique customers** and fulfilled **1,615 orders** totaling **7,078 units sold**.

BikeStores generated cumulative revenue of **$7.69M** across this period, with an average order value of **$4,761** — reflecting the premium nature of the product mix. The business operates with a **10-person staff** distributed across the three locations, supported by a centralized inventory system tracking **939 stock records** across all store locations.

Reporting to the Head of Operations, a comprehensive performance analysis was conducted to evaluate BikeStores' commercial trajectory over its first three years. This review provides critical insights that cross-functional teams in merchandising, operations, and store management will utilize to optimize product mix, improve regional performance, and strengthen profitability. The key focus areas include:

---

<h1 align="center">2. Northstar Metrics</h1>

The analysis is structured around eight core business performance areas:

- 📈 **Sales Trends** — Tracking year-over-year and quarterly revenue performance, order volume, and average order value to identify growth patterns and seasonal trends across the business lifecycle.

- 🏷️ **Category Performance** — Evaluating the seven product categories (Mountain Bikes, Road Bikes, Cruisers, Electric Bikes, Cyclocross, Comfort Bikes, Children's Bikes) to understand revenue contribution, unit economics, and margin profiles.

- 🏆 **Brand Analysis** — Assessing brand-level performance across nine bicycle manufacturers to identify top performers, revenue concentration risk, and partnership opportunities.

- 🏪 **Store Performance** — Comparing the three retail locations on revenue, customer acquisition, order volume, and average order value to surface regional best practices and underperforming markets.

- 🚲 **Product Analysis** — Identifying top-selling SKUs, price point dynamics, and product mix optimization opportunities across the 321-model catalog.

- 🌎 **Customer Geography** — Analyzing customer distribution and purchasing behavior by state to inform regional marketing, inventory positioning, and expansion strategy.

- 📦 **Inventory & Stock Analysis** — Evaluating stock levels against sales velocity to identify overstock, stockout risk, and optimal reorder points across the product portfolio.

- 👥 **Staff Productivity** — Measuring individual staff performance on revenue generation and customer service metrics to support compensation planning and training priorities.

---

<h1 align="center">3. Executive Summary</h1>

<table>
  <tr>
    <td valign="top" width="50%">

### 📊 1. Strong Growth Followed by Sharp Decline
- Revenue grew **42% YoY** from $2.43M (2016) to $3.45M (2017), driven by category expansion and increased AOV from $3,823 to $5,010.
- **2018 saw a 47% revenue collapse** to just $1.81M across only 292 orders — a red flag indicating potential operational, competitive, or market disruption.
- The business is **incomplete for 2018** (data ends Dec 28), but Q4 2018 shows only **$21,660 in revenue** from 4 orders, suggesting near-total operational shutdown.

</td>
    <td valign="top" width="50%">

### 🏪 2. Extreme Store Concentration Risk
- **Baldwin Bikes (NY) dominates** with 67.8% of total revenue ($5.22M) and 1,019 customers — nearly 7x Santa Cruz's performance.
- Santa Cruz Bikes (CA) generated $1.61M (20.9%) while Rowlett Bikes (TX) trailed at $868K (11.3%).
- Baldwin's dominance suggests either superior location/management **or** systemic underinvestment in the other two stores.

</td>
  </tr>
  <tr>
    <td valign="top" width="50%">

### 🚴 3. Trek Brand Lock-In
- **Trek accounts for 59.9% of all revenue** ($4.60M), creating dangerous single-supplier dependency.
- Electra (15.7%) and Surly (12.3%) are distant second/third, with the remaining 6 brands combining for just 12.1% share.
- Mountain Bikes (35.3% of revenue) and Road Bikes (21.7%) drive over half of sales, while Children's Bikes represent only 3.8% despite broader market appeal.

</td>
    <td valign="top" width="50%">

### 💰 4. Premium Pricing Strategy Working
- AOV increased from $3,823 (2016) to $6,214 (2018), though this coincides with declining order volume.
- Top products command $4,000–$6,000 unit prices — Trek Slash 8 27.5, Trek Conduit+ (electric), and Trek Fuel EX 8 29 lead with $556K, $389K, and $368K in cumulative revenue.
- **Electric Bikes deliver $2,910 average unit price** vs. $248 for Children's Bikes, validating premium category focus.

</td>
  </tr>
</table>

### 5. Key Recommendations

> ⚠️ **Investigate 2018 collapse** — Revenue down 47%, order volume down 58% from 2017. Root cause could be competitive disruption, operational failure, or data quality issue. **Urgent priority**.

> 🏪 **Rebalance store portfolio** — Baldwin (NY) drives 68% of revenue. Either scale Santa Cruz and Rowlett through capital investment, or consider consolidating to a single high-performing location.

> 🏷️ **Diversify brand mix** — Trek dependency (60%) creates supplier risk. Negotiate better terms or expand Electra, Surly, and emerging brands to reduce concentration.

> 📦 **Address inventory imbalances** — Several high-demand items (Trek Remedy 29 Frameset, Surly Straggler 650b) show stock-to-sales ratios below 0.5, signaling persistent stockouts and lost revenue.

---

<h1 align="center">4. Data Structure & ERD</h1>

The dataset consists of **9 relational tables** forming a normalized retail database schema. The core transactional fact table is `order_items`, which connects to dimensional tables for products, customers, stores, and staff.

### 📐 Entity Relationship Diagram

```
┌─────────────┐         ┌──────────────┐         ┌─────────────┐
│  customers  │────┐    │    orders    │────┐    │   stores    │
├─────────────┤    │    ├──────────────┤    │    ├─────────────┤
│ customer_id │◄───┼───►│ order_id     │◄───┼───►│ store_id    │
│ first_name  │    │    │ customer_id  │    │    │ store_name  │
│ last_name   │    │    │ order_status │    │    │ city        │
│ email       │    │    │ order_date   │    │    │ state       │
│ city        │    │    │ store_id     │    │    └─────────────┘
│ state       │    │    │ staff_id     │    │
└─────────────┘    │    └──────────────┘    │
                   │            │            │
                   │            ▼            │
                   │    ┌──────────────┐    │    ┌─────────────┐
                   │    │ order_items  │    └───►│   staffs    │
                   │    ├──────────────┤         ├─────────────┤
                   └───►│ order_id     │         │ staff_id    │
                        │ product_id   │◄───┐    │ first_name  │
                        │ quantity     │    │    │ store_id    │
                        │ list_price   │    │    │ manager_id  │
                        │ discount     │    │    └─────────────┘
                        └──────────────┘    │
                                            │
┌─────────────┐         ┌──────────────┐   │
│  brands     │────┐    │  products    │───┘
├─────────────┤    │    ├──────────────┤
│ brand_id    │◄───┼───►│ product_id   │
│ brand_name  │    │    │ product_name │
└─────────────┘    │    │ brand_id     │◄───┐
                   │    │ category_id  │    │
┌─────────────┐    │    │ model_year   │    │
│ categories  │────┘    │ list_price   │    │
├─────────────┤         └──────────────┘    │
│ category_id │◄────────────────────────────┘
│ category_name│
└─────────────┘

┌─────────────┐
│   stocks    │  (Inventory tracking)
├─────────────┤
│ store_id    │
│ product_id  │
│ quantity    │
└─────────────┘
```

### 📋 Data Dictionary

| Table | Rows | Description |
|-------|------|-------------|
| **orders** | 1,615 | Order header with customer, store, staff, dates, and status |
| **order_items** | 4,722 | Line-item detail: product, quantity, price, discount |
| **customers** | 1,445 | Customer master: name, email, address |
| **products** | 321 | Product catalog: SKU details, brand, category, MSRP |
| **stores** | 3 | Store locations: Santa Cruz (CA), Baldwin (NY), Rowlett (TX) |
| **staffs** | 10 | Sales staff assigned to stores with manager hierarchy |
| **brands** | 9 | Bicycle manufacturers: Trek, Electra, Surly, etc. |
| **categories** | 7 | Product categories: Mountain, Road, Cruiser, Electric, etc. |
| **stocks** | 939 | Inventory levels per product per store |

**Key Metrics Calculated:**
- **Line Revenue** = `quantity × list_price × (1 - discount)`
- **Discount Amount** = `quantity × list_price × discount`
- **AOV (Average Order Value)** = `SUM(line_revenue) / COUNT(DISTINCT order_id)`

---

<h1 align="center">5. Insight Deep-Dive</h1>

---

<h2 align="center">5.1 Sales Trends</h2>

<h3 align="left">📈 Yearly Performance</h3>

| Year | Revenue | YoY Growth | Orders | Customers | Items Sold | AOV |
|------|---------|------------|--------|-----------|------------|-----|
| 2016 | $2,427,379 | — | 635 | 625 | 2,663 | $3,823 |
| 2017 | **$3,447,208** | **+42.0%** | 688 | 684 | 3,099 | $5,010 |
| 2018 | $1,814,530 | **-47.4%** ⚠️ | 292 | 270 | 1,316 | $6,214 |

**Analysis:**
- 2017 was the peak performance year with **$3.45M in revenue**, representing a healthy 42% year-over-year growth driven by both increased order volume (+8.3%) and a rising AOV (+31%).
- 2018 experienced a **catastrophic 47% revenue decline** alongside a 58% drop in order volume. While AOV continued climbing to $6,214 (suggesting a shift toward higher-ticket items or fewer bulk buyers), the sharp reduction in customer count (270 vs. 684) signals a critical business disruption.
- The 2018 dataset is **incomplete** (ends Dec 28 vs. full-year 2016/2017 data), but even accounting for missing days, Q4 2018 shows only 4 orders totaling $21,660 — an unsustainable run rate.

<h3 align="left">📅 Quarterly Trends</h3>

| Quarter | Revenue | Orders | Items | AOV |
|---------|---------|--------|-------|-----|
| 2016 Q1 | $551,859 | 154 | 657 | $3,584 |
| 2016 Q2 | $582,976 | 139 | 599 | $4,194 |
| 2016 Q3 | $698,306 | 180 | 743 | $3,879 |
| 2016 Q4 | $594,237 | 162 | 664 | $3,668 |
| 2017 Q1 | $907,452 | 174 | 788 | $5,215 |
| 2017 Q2 | $874,390 | 177 | 785 | $4,940 |
| 2017 Q3 | $813,954 | 170 | 773 | $4,788 |
| 2017 Q4 | $851,412 | 167 | 753 | $5,098 |
| 2018 Q1 | $946,079 | 155 | 691 | $6,104 |
| 2018 Q2 | $818,111 | 126 | 581 | $6,493 |
| 2018 Q3 | $28,680 ⚠️ | 7 | 24 | $4,097 |
| 2018 Q4 | $21,660 🚨 | 4 | 20 | $5,415 |

**Key Findings:**
- **2017 showed consistent quarterly performance** in the $813K–$907K range, with Q1 2017 being the single best quarter ($907K).
- **2018 Q3 and Q4 collapse** to near-zero revenue ($29K and $22K respectively) suggests operational shutdown, data truncation, or severe business disruption.
- **Seasonal pattern (2016-2017)**: Q3 tends to be strongest (summer bike-buying season), followed by Q1 (New Year fitness resolutions).

---

<h2 align="center">5.2 Category Performance</h2>

<h3 align="left">🏷️ Revenue by Category</h3>

| Category | Revenue | Rev Share | Units Sold | Orders | Avg Unit Price |
|----------|---------|-----------|------------|--------|----------------|
| **Mountain Bikes** | **$2,715,080** | **35.3%** | 1,755 | 866 | $1,547 |
| **Road Bikes** | $1,665,098 | 21.7% | 559 | 315 | **$2,979** |
| **Cruisers Bicycles** | $995,033 | 12.9% | 2,063 | 959 | $482 |
| **Electric Bikes** | $916,685 | 11.9% | 315 | 202 | **$2,910** |
| **Cyclocross Bicycles** | $711,012 | 9.2% | 394 | 245 | $1,805 |
| **Comfort Bicycles** | $394,020 | 5.1% | 813 | 472 | $485 |
| **Children Bicycles** | $292,189 | 3.8% | 1,179 | 635 | $248 |

**Analysis:**
- **Mountain Bikes dominate** with over one-third of total revenue ($2.72M), driven by both volume (1,755 units) and premium pricing ($1,547 avg).
- **Road Bikes punch above their weight** — only 559 units sold but $1.67M in revenue due to a $2,979 average unit price, the highest outside Electric Bikes.
- **Electric Bikes show explosive premium potential** at $2,910 per unit, though still small volume (315 units total). This category likely saw growth post-2018 but represents an underexploited opportunity during the data period.
- **Children's Bikes underperform** at just 3.8% revenue share despite high unit volume (1,179 units), reflecting low $248 average pricing and thin margins.
- **Cruisers have strong volume** (2,063 units) but contribute only 12.9% of revenue — a classic high-volume, low-margin category suitable for entry-level customers.

---

<h2 align="center">5.3 Brand Analysis</h2>

<h3 align="left">🏆 Revenue by Brand</h3>

| Brand | Revenue | Rev Share | Units Sold | Orders |
|-------|---------|-----------|------------|--------|
| **Trek** | **$4,602,754** | **59.9%** 🚨 | 1,839 | 883 |
| **Electra** | $1,205,321 | 15.7% | 2,612 | 1,096 |
| **Surly** | $949,507 | 12.3% | 908 | 531 |
| **Sun Bicycles** | $341,995 | 4.4% | 731 | 393 |
| **Haro** | $185,385 | 2.4% | 331 | 196 |
| **Heller** | $171,459 | 2.2% | 138 | 97 |
| **Pure Cycles** | $149,476 | 1.9% | 376 | 232 |
| **Ritchey** | $78,899 | 1.0% | 118 | 77 |
| **Strider** | $4,320 | 0.1% | 25 | 16 |

**Critical Insights:**
- **Trek's 60% revenue concentration is a major business risk.** If Trek raises prices, changes distribution terms, or favors competing retailers, BikeStores faces existential exposure.
- **Electra (15.7%) and Surly (12.3%)** provide some diversification but are still distant second/third choices. Together with Trek, these three brands account for **87.9% of all revenue**.
- **Six "long-tail" brands** (Sun, Haro, Heller, Pure Cycles, Ritchey, Strider) combine for only 12.1% of revenue, suggesting underutilized supplier relationships or low consumer demand for these brands.
- **Strider (0.1% share)** is essentially irrelevant to the business — likely a children's balance bike niche with minimal traction.

**Recommendation:** Negotiate volume-based pricing with Trek while actively developing Electra and Surly as strategic alternatives to reduce dependency.

---

<h2 align="center">5.4 Store Performance</h2>

<h3 align="left">🏪 Revenue by Store Location</h3>

| Store | Location | Revenue | Rev Share | Orders | Customers | Units | AOV |
|-------|----------|---------|-----------|--------|-----------|-------|-----|
| **Baldwin Bikes** | Baldwin, NY | **$5,215,751** | **67.8%** | 1,093 | 1,019 | 4,779 | $4,772 |
| **Santa Cruz Bikes** | Santa Cruz, CA | $1,605,823 | 20.9% | 348 | 284 | 1,516 | $4,614 |
| **Rowlett Bikes** | Rowlett, TX | $867,542 | 11.3% | 174 | 142 | 783 | **$4,986** |

**Analysis:**
- **Baldwin Bikes (NY) is the undisputed leader**, generating nearly **7x the revenue of the Texas location** and over 3x Santa Cruz. With 1,019 customers and 1,093 orders, Baldwin drives the bulk of the business.
- **Rowlett Bikes shows the highest AOV** ($4,986) despite the lowest order count (174), suggesting a wealthier customer base or better upselling — but overall contribution remains small at 11.3% of revenue.
- **Santa Cruz Bikes underperforms** relative to its presumably affluent California market. With only 284 customers over three years, there's either a market fit issue, operational challenge, or competitive pressure.

**Store Performance Deep-Dive:**

| Metric | Baldwin | Santa Cruz | Rowlett |
|--------|---------|------------|---------|
| Customers per Year | 340 | 95 | 47 |
| Orders per Customer | 1.07 | 1.23 | 1.23 |
| Revenue per Customer | $5,119 | $5,654 | $6,109 |
| Revenue per Order | $4,772 | $4,614 | $4,986 |

- **Baldwin has the lowest repeat rate** (1.07 orders/customer) but compensates with massive volume.
- **Santa Cruz and Rowlett** show slightly better loyalty (1.23 orders/customer) but struggle with customer acquisition.

---

<h2 align="center">5.5 Product Analysis</h2>

<h3 align="left">🚲 Top 15 Products by Revenue</h3>

| Rank | Product | Brand | Category | Revenue | Units | Avg Price |
|------|---------|-------|----------|---------|-------|-----------|
| 🥇 | Trek Slash 8 27.5 - 2016 | Trek | Mountain | $555,559 | 154 | $3,608 |
| 🥈 | Trek Conduit+ - 2016 | Trek | Electric | $389,249 | 145 | $2,684 |
| 🥉 | Trek Fuel EX 8 29 - 2016 | Trek | Mountain | $368,473 | 143 | $2,577 |
| 4 | Surly Straggler 650b - 2016 | Surly | Cyclocross | $226,766 | 151 | $1,502 |
| 5 | Trek Domane SLR 6 Disc - 2017 | Trek | Road | $211,585 | 43 | **$4,921** |
| 6 | Surly Straggler - 2016 | Surly | Cyclocross | $203,508 | 147 | $1,384 |
| 7 | Trek Remedy 29 Carbon Frameset - 2016 | Trek | Mountain | $203,381 | 125 | $1,627 |
| 8 | Trek Powerfly 8 FS Plus - 2017 | Trek | Electric | $188,250 | 41 | **$4,591** |
| 9 | Trek Madone 9.2 - 2017 | Trek | Road | $175,900 | 39 | **$4,510** |
| 10 | Trek Silque SLR 8 Women's - 2017 | Trek | Road | $174,525 | 29 | **$6,018** |
| 11 | Trek Silque SLR 7 Women's - 2017 | Trek | Road | $163,080 | 30 | **$5,436** |
| 12 | Trek Fuel EX 9.8 27.5 Plus - 2017 | Trek | Mountain | $159,053 | 33 | **$4,820** |
| 13 | Heller Shagamaw Frame - 2016 | Heller | Mountain | $151,161 | 129 | $1,172 |
| 14 | Trek Fuel EX 9.8 29 - 2017 | Trek | Mountain | $147,450 | 33 | **$4,468** |
| 15 | Trek Boone 7 - 2017 | Trek | Cyclocross | $127,610 | 42 | $3,038 |

**Key Findings:**
- **Trek dominates the top 15** — 12 of 15 slots are Trek products, reinforcing the brand dependency identified earlier.
- **Trek Slash 8 27.5 is the single biggest revenue driver** at $556K across 154 units, averaging $3,608 per sale.
- **Women's road bikes command premium pricing** — Trek Silque SLR 8 Women's averages **$6,018** per unit, the highest on the list, despite only 29 units sold.
- **Electric bikes show strong unit economics** — Trek Conduit+ and Powerfly models generate $2,684–$4,591 average prices, validating the premium Electric category.

---

<h2 align="center">5.6 Customer Geography</h2>

<h3 align="left">🌎 Revenue by State</h3>

| State | Revenue | Rev Share | Customers | Orders | AOV |
|-------|---------|-----------|-----------|--------|-----|
| **New York (NY)** | **$5,215,751** | **67.8%** | 1,019 | 1,093 | $4,772 |
| **California (CA)** | $1,605,823 | 20.9% | 284 | 348 | $4,614 |
| **Texas (TX)** | $867,542 | 11.3% | 142 | 174 | $4,986 |

**Analysis:**
- The geographic concentration **mirrors store performance exactly** — all NY customers shop at Baldwin, all CA customers at Santa Cruz, all TX customers at Rowlett.
- This suggests BikeStores operates as a **local/regional retailer with no e-commerce presence** or cross-store customer mobility.
- **Texas shows the highest AOV** ($4,986) despite the smallest customer base, indicating premium buyer segments or successful upselling tactics.
- **New York's 1,019 customers** represent 70.5% of the total customer base, creating similar concentration risk to the Trek brand dependency.

---

<h2 align="center">5.7 Inventory & Stock Analysis</h2>

<h3 align="left">📦 Top 20 Low-Stock Items (Stock-to-Sales Ratio)</h3>

| Product | Brand | Stock | Units Sold | Stock/Sales |
|---------|-------|-------|------------|-------------|
| Trek Remedy 29 Carbon Frameset - 2016 | Trek | 13 | 125 | **0.104** 🚨 |
| Sun Bicycles Streamway 7 - 2017 | Sun | 11 | 37 | **0.297** |
| Electra Amsterdam Original 3i - 2015/2017 | Electra | 11 | 32 | **0.344** |
| Electra Amsterdam 3i Ladies' - 2017 | Electra | 12 | 31 | **0.387** |
| Trek Precaliber 24 (21-Speed) - Girls - 2017 | Trek | 16 | 39 | **0.410** |
| Trek Silque SLR 8 Women's - 2017 | Trek | 12 | 29 | **0.414** |
| Trek Domane SL 6 - 2017 | Trek | 16 | 37 | **0.432** |

**Critical Findings:**
- **Trek Remedy 29 Carbon Frameset** has the most severe stockout risk — only 13 units in stock after selling 125 units, a **0.104 ratio** indicating chronic undersupply.
- **Multiple high-demand products** show ratios below 0.5, meaning current stock levels would last less than half the historical sales period if demand continues.
- **Popular models are being starved of inventory**, likely resulting in lost sales and customer frustration.

**Overstocked Items:**

Several products show **stock-to-sales ratios above 5.0**, meaning inventory levels exceed 5x historical sales:
- Electra Superbolt 1 20" - 2018: 4.5x ratio
- Electra Townie Original 21D Ladies' - 2018: 5.3x ratio  
- Electra Cruiser 7D (24-Inch) Ladies' - 2018: 5.3x ratio

These likely represent **2018 model-year introductions** with poor market fit or inadequate marketing.

---

<h2 align="center">5.8 Staff Performance</h2>

<h3 align="left">👥 Top Performers</h3>

| Staff | Store | Revenue | Orders | Customers | AOV |
|-------|-------|---------|--------|-----------|-----|
| **Marcelene Boyer** | Baldwin Bikes | **$2,624,121** | 553 | 538 | $4,745 |
| **Venita Daniel** | Baldwin Bikes | $2,591,631 | 540 | 518 | $4,799 |
| **Genna Serrano** | Santa Cruz Bikes | $853,287 | 184 | 164 | $4,637 |
| **Mireya Copeland** | Santa Cruz Bikes | $752,536 | 164 | 152 | $4,589 |
| **Kali Vargas** | Rowlett Bikes | $463,918 | 88 | 75 | **$5,272** |
| **Layla Terrell** | Rowlett Bikes | $403,624 | 86 | 79 | $4,693 |

**Insights:**
- **Marcelene Boyer and Venita Daniel** at Baldwin Bikes are the top revenue generators, each handling 500+ orders and generating $2.6M+ in revenue.
- **Kali Vargas (Rowlett)** achieves the **highest AOV** ($5,272) despite lower volume, suggesting exceptional upselling skills or a premium customer segment.
- Performance differences within stores are minimal (e.g., Baldwin's two top reps are within 1.2% of each other), suggesting systematic training or similar customer pools rather than individual variance.

---

<h1 align="center">📌 Summary of Key Recommendations</h1>

<table>
  <tr>
    <th>Priority</th>
    <th>Area</th>
    <th>Action</th>
    <th>Expected Impact</th>
  </tr>
  <tr style="background-color: #ffebee;">
    <td>🔴 Critical</td>
    <td>2018 Revenue Collapse</td>
    <td>Investigate root cause of 47% YoY decline and Q3/Q4 near-shutdown</td>
    <td>Business continuity risk</td>
  </tr>
  <tr style="background-color: #ffebee;">
    <td>🔴 Critical</td>
    <td>Brand Concentration</td>
    <td>Reduce Trek dependency from 60% → 40% through Electra/Surly growth</td>
    <td>Supplier risk mitigation</td>
  </tr>
  <tr style="background-color: #fff3e0;">
    <td>🟡 High</td>
    <td>Store Performance Gap</td>
    <td>Audit Santa Cruz & Rowlett operations; consider consolidation if unfixable</td>
    <td>Operational efficiency</td>
  </tr>
  <tr style="background-color: #fff3e0;">
    <td>🟡 High</td>
    <td>Inventory Stockouts</td>
    <td>Reorder Trek Remedy, Surly Straggler, Trek Silque models to 1.5x–2.0x ratio</td>
    <td>Revenue recovery from lost sales</td>
  </tr>
  <tr style="background-color: #e8f5e9;">
    <td>🟢 Medium</td>
    <td>Electric Bike Category</td>
    <td>Expand Electric inventory and marketing — highest unit price ($2,910 avg)</td>
    <td>Premium margin growth</td>
  </tr>
  <tr style="background-color: #e8f5e9;">
    <td>🟢 Medium</td>
    <td>Children's Category</td>
    <td>Either exit (3.8% rev share, $248 avg price) or reposition as loss-leader</td>
    <td>Margin improvement</td>
  </tr>
</table>

---

*Report generated from BikeStores relational database | Analysis period: Jan 1, 2016 – Dec 28, 2018 | 9 tables, 1,615 orders, $7.69M revenue*
