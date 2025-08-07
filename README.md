# Maji-Ndogo-Data-Transparency

This repository contains two integrated Power BI dashboard that offer in-depth insights into the Maji Ndogo Water Service Project. Designed to support both strategic decision makers and the general public, the dashboard promote data driven transparency by highlighting Project progress, financial allocations, and improvement in water access across multiple regions.

# Dashboards Included
This project features two distinct Power BI dashboards designed to support both strategic leadership and public transparency:

# 1. Maji Ndogo Stakeholders Dashboard (For Decision-Makers)
<img width="604" height="338" alt="Image" src="https://github.com/user-attachments/assets/392ac5b2-d44e-4194-938e-5fdc304e8dd9" />

This dashboard is tailored for key decision-makers including President Aziza Naledi and provincial leaders by delivering critical insights into the state of water access, infrastructure needs, and financial performance. It supports informed decision-making through actionable data and dynamic visualizations.

**Purpose:**
To equip national and provincial leadership with accurate, timely, and actionable data on:

1..Water access challenges

2..Infrastructure upgrade requirements

3..Budget allocations and expenditures

This enables evidence-based strategic planning and effective resource deployment.

**Primary Data Source:**
**_Md_water_services_data.xlsx_**  
Contains detailed data on water sources, project visits, infrastructure costs, and implementation progress.

# Key Features & Visuals:
**Overall Water Access Status:**
High-level summaries of population access to water, segmented by province and by rural vs. urban areas.

**Water Access Challenges:**
Visualization of affected populations and water source issues, with optional de-emphasis of less critical sources (e.g., **_tap_in_homes_**) for strategic clarity.

**Upgrade Costs & Budget Allocations:**
Breakdown of upgrade needs and associated costs by province, area type (rural/urban), and improvement category.

**High-Impact Summary Cards:**
Quick-glance metrics showing total upgrade cost, current water access levels, and projected improvements.

**Interactive Controls:**
Province slicers and rural/urban filters to enable customized data exploration by leaders.

**Dynamic Financial Views (Bookmarks):**
Toggle between budget breakdowns by province or by improvement type using buttons and bookmarks to save space and enhance usability.

**Provincial Drill-Down Pages:**
Dedicated pages per province with local insights: town-level budgets, rural/urban expenditure splits, specific improvement needs, queue lengths, gender data, and localized crime metrics.

# Key Insights Delivered:
**Strategic Resource Allocation:**
Identifies where funding is most needed by region, population type, and improvement priority to maximize impact.

**Impact Assessment:**
Links investment to measurable outcomes in water access, supporting performance tracking.

**Targeted Interventions:**
Pinpoints specific problems (e.g., broken boreholes, contamination) and the populations affected.

**Financial Accountability:**
Transparent view of committed funds and their tangible outputs, reinforcing accountability and trust.


### 2. **Maji Ndogo Public Dashboard** *(For Public Project Monitoring)*

**Description:**

This **public-facing dashboard** offers transparent insights into the **financial performance** and **progress** of water infrastructure projects across Maji Ndogo. It is designed for **citizens**, **civil society**, **journalists**, and **external stakeholders** to monitor **budget adherence**, **project status**, and **regional distribution** of improvements.

**Purpose:**

To enhance **public accountability** by:
- Tracking **actual spending vs. allocated budgets**  
- Visualizing **project progress** and **completion rates**  
- Highlighting **geographic** and **vendor-level** trends

**Primary Data Source:**
- `Md_water_services_data(public).xlsx`, using structured tables or imported CSVs:
  - `project_progress.csv`: Core **project details**, **completion dates**, **budgeted and actual costs**, and **status**
  - `infrastructure_cost.csv`: **Standard** and **rural-adjusted** unit costs
  - `location.csv`: **Geographic data** for towns and regions
  - `vendors.csv`: Vendor participation information

**Key Features & Visuals:**

- **Cumulative Budget & Cost Line Chart**  
  Visual comparison of **total budgeted vs. actual expenditure** over time.

- **KPI Cards (At-a-Glance Metrics):**
  - **Cumulative Budget**: Total allocated budget (e.g., **$146,737,375**)  
  - **Cumulative Cost**: Total actual expenditure (e.g., **$154,493,298**)  
  - **Cost Difference**: Highlights **under- or over-spending**  
  - **Total Projects in Backlog**  
  - **Completed Projects**

- **Project Status Bar Chart**  
  Breakdown of project statuses (e.g., **Backlog** vs. **Completed**).

- **Projects by Town/Location Chart**  
  Distribution of projects across **towns and regions**.

- **Projects by Improvement Type**  
  Categories such as **“Drill Well”**, **“Install Pump”**, etc.

- **Projects by Vendor**  
  Shows the number of projects by **vendor involvement**.

- **Interactive Filters (Slicers):**
  - **Date Range Slicer**  
  - **Town Slicer**

**Key Insights Delivered:**

- **Budget vs. Actual Spend**  
  Tracks whether projects adhere to their **allocated budgets** or **overspend**.

- **Project Progress Monitoring**  
  Visibility into the **delivery pipeline** from **backlog to completion**.

- **Geographic Distribution**  
  Identifies areas with **high project activity** or **underserved needs**.

- **Resource Allocation Trends**  
  Highlights **prioritized improvements** and **active vendors**.

**Data Model Highlights:**

- **Dedicated Date Table**  
  Enables robust **time intelligence** via `date_of_completion`.

- **Calculated Columns:**
  - `**budgeted_improvement_cost**`: Computes per-project budgets with **rural adjustments**
  - `**rural_adjusted_cost**` *(in `infrastructure_cost.csv`)*: Formula — `unit_cost_USD * 1.5`
  - `**aggregated_improvements**`: Groups similar types (e.g., **“Install 1–8 taps”** → **“Install public tap(s)*”**)
  - `**average_queue_time**` *(in `water_source`)*: Assesses queue times
  - `**basic_water_access**` *(in `water_source`)*: Classifies sources as **‘Basic’** or **‘Below Basic’** based on **UN standards**

- **Custom DAX Measures:**
  - `**cumulative_budget**`, `**cumulative_cost**`  
  - `**basic_water_access_percentage**`  
  - `**project_count_backlog**`, `**project_count_completed**`  
  - `**cost_difference**`

