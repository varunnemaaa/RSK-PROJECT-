# 📊 Statewide Safety, Protection & Wellbeing Programme Analytics Dashboard

### Power BI | Data Analytics | Assessment Intelligence | Madhya Pradesh

An interactive **Power BI analytics and monitoring dashboard** developed for the **Statewide Safety, Protection & Wellbeing Programme for KGBVs & NSCBAVs, Madhya Pradesh**.

The project transforms student and personnel assessment data into an interactive analytical solution for monitoring **programme participation, assessment completion, Pre/Post performance and learning outcomes** at state and institution levels.

---

## 📌 Project Overview

The project is designed to provide a structured view of programme performance across:

- 🗺️ State
- 📍 District
- 🏫 Institution
- 👩‍🎓 Students
- 👨‍🏫 Personnel

The solution follows a **Pre-Assessment → Learning Modules → Post-Assessment → Learning Gain** framework.

It uses **Power Query for data preparation, a star-schema data model for analytics, and DAX for KPI and learning-outcome calculations**.

---

## 🎯 Objectives

The key objectives of the project are to:

- Consolidate student and personnel assessment data.
- Monitor programme participation and coverage.
- Track assessment completion.
- Compare Pre and Post assessment performance.
- Calculate learning gain.
- Identify students and personnel showing improvement.
- Analyse performance across districts and institutions.
- Provide separate student and personnel analytics.
- Create an executive-level monitoring dashboard.
- Enable interactive drill-down from statewide to institution-level analysis.

---

## 🏫 Programme Modules

### Student Modules

| Module | Description |
|---|---|
| **M1** | My Safety, My Rights |
| **M2** | Safe & Unsafe Behaviour |

### Personnel Modules

| Module | Description |
|---|---|
| **E1** | Understanding POCSO & Child Safeguarding |
| **E2** | POSH & Safe Workplace Practices |

Each assessment framework supports **Pre and Post assessment analysis**.

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| **Microsoft Power BI** | Dashboard development & visualization |
| **Power Query** | Data cleaning & transformation |
| **DAX** | KPIs and analytical calculations |
| **Microsoft Excel** | Source assessment datasets |
| **Star Schema** | Analytical data modelling |

---

# 🔄 Project Workflow

```text
Assessment Data
       ↓
Raw / Staging Data
       ↓
Power Query Transformation
       ↓
Data Cleaning & Standardization
       ↓
Append / Merge
       ↓
Dimension & Fact Tables
       ↓
Star Schema
       ↓
DAX Measures
       ↓
Power BI Data Model
       ↓
Interactive Dashboard
       ↓
State → District → Institution Analysis
```

---

# 🧩 Data Model

The project follows a **star-schema architecture** with shared dimensions and separate student/personnel fact tables.

### Dimensions

```text
Dim_Date
Dim_District
Dim_Institution
Dim_Module
Dim_Question
Dim_Student
Dim_Employee
```

### Fact Tables

```text
Fact_Response_Student
Fact_Response_Employee
```

### Simplified Architecture

```text
                    Dim_Date
                       │
                       ▼
Dim_Student ──► Fact_Response_Student ◄── Dim_Module
                       ▲
                       │
                Dim_Question
                       ▲
                       │
                Dim_Institution
                       ▲
                       │
                 Dim_District


                    Dim_Date
                       │
                       ▼
Dim_Employee ──► Fact_Response_Employee ◄── Dim_Module
                       ▲
                       │
                Dim_Question
                       ▲
                       │
                Dim_Institution
                       ▲
                       │
                 Dim_District
```

The student and personnel fact tables remain separate while sharing common analytical dimensions.

---

# 📊 Dashboard Pages

The final Power BI dashboard contains **six main pages**.

## 1️⃣ Home — Dashboard Overview

Provides the overall programme introduction and navigation.

### Includes:

- Programme overview
- Programme snapshot
- Institutions covered
- Districts active
- Students trained
- Personnel trained
- Learning gain
- Navigation to analytical pages

---

## 2️⃣ State Executive Dashboard

Provides an executive-level view of programme performance across Madhya Pradesh.

### Key components:

- Madhya Pradesh district map
- Institutions covered
- Districts active
- Students trained
- Personnel trained
- Programme completion
- Overall learning gain
- Training participation
- District performance
- Learning gain analysis
- Executive insights

The map acts as the central visual for understanding geographic programme coverage.

---

## 3️⃣ State Student Dashboard

Focuses on student participation and learning outcomes across the state.

### Key visuals:

- Students trained
- Institutions covered
- Districts active
- Student completion
- Student learning gain
- District Participation vs Learning Gain
- Student Module Participation
- Student Responses by District
- Student Pre vs Post performance
- Students Showing Improvement

### Filters:

- District
- Institution
- Class
- Module
- Stage
- Year

---

## 4️⃣ State Personnel Dashboard

Focuses on personnel participation and assessment outcomes.

### Key visuals:

- Personnel trained
- Institutions covered
- Districts active
- Personnel completion
- Personnel learning gain
- Personnel assessment responses
- Pre vs Post performance
- Personnel showing improvement
- Key analytical breakdowns
- Decomposition Tree

### Analytical dimensions include:

- District
- Module
- Department
- Hostel Type

---

## 5️⃣ Institution Student Dashboard

Provides institution-level student analytics.

### Key visuals:

- Students trained
- Selected institution
- Classes covered
- Student completion
- Learning gain
- Student assessment activity trend
- Student Pre vs Post performance
- Student assessment responses
- Students showing improvement
- Key Influencers

### Filters:

- District
- Institution
- Class
- Module
- Stage
- Year

The Institution ID slicer allows users to move from the statewide view to an individual institution.

---

## 6️⃣ Institution Personnel Dashboard

Provides institution-level personnel analytics.

### Key visuals:

- Personnel participation
- Selected institution
- Departments covered
- Personnel completion
- Personnel learning gain
- Learning gain by module
- Personnel response activity
- Pre vs Post performance
- Personnel showing improvement by department

### Filters:

- District
- Institution
- Department
- Module
- Stage
- Year

---

# 📈 Key KPIs

The dashboard uses several analytical KPIs.

### Institutions Covered

Number of distinct participating institutions.

### Districts Active

Number of districts with programme activity.

### Students Trained

Distinct students participating in the programme.

### Personnel Trained

Distinct personnel participating in the programme.

### Programme Completion

Measures participant completion of the assessment/programme cycle based on the available assessment data.

### Pre-Assessment Score

Average/percentage performance during the Pre stage.

### Post-Assessment Score

Average/percentage performance during the Post stage.

### Learning Gain

```text
Learning Gain =
Post-Assessment Score − Pre-Assessment Score
```

The metric is interpreted as a **percentage-point difference** when displayed as a percentage.

### Participants Showing Improvement

Participants whose Post score is higher than their Pre score.

---

# 📊 Power BI Visuals Used

The dashboard combines multiple visualization types to avoid relying on a single chart style.

### Core visuals

- KPI Cards
- Bar Charts
- Column Charts
- Line Charts
- Donut Charts
- Matrix
- Geographic Map
- Key Influencers
- Decomposition Tree
- Slicers
- Navigation Buttons

---

# 🔍 Analytical Features

## Pre vs Post Analysis

Allows users to compare assessment performance before and after the learning modules.

## Learning Gain

Measures the change between Pre and Post assessment performance.

## District Analysis

Allows comparison of participation and learning outcomes across districts.

## Institution Analysis

Allows users to select and analyse individual institutions.

## Student Improvement

Identifies students whose Post assessment score is higher than their Pre assessment score.

## Personnel Improvement

Identifies personnel whose Post assessment score is higher than their Pre assessment score.

## Key Influencers

Used to explore factors associated with the selected learning-gain measure.

## Decomposition Tree

Provides interactive breakdown of learning gain across dimensions such as:

```text
Learning Gain
      ↓
District
      ↓
Module
      ↓
Department
```

---

# 🧹 Data Preparation

The project uses Power Query for:

- Data cleaning
- Data standardization
- Appending assessment datasets
- Merging reference information
- Preparing dimensions
- Preparing fact tables
- Handling Pre/Post stages
- Validating identifiers
- Preparing assessment dates
- Creating the final analytical model

Raw/staging data is kept conceptually separate from the curated analytical model.

---

# 🗂️ Repository Structure

A recommended GitHub structure is:

```text
Statewide-Safety-Wellbeing-Analytics/
│
├── README.md
│
├── data/
│   ├── student/
│   ├── personnel/
│   └── sample/
│
├── powerbi/
│   └── Programme_Analytics_Dashboard.pbix
│
├── documentation/
│   ├── Project_Report.pdf
│   ├── Data_Model.pdf
│   └── Workflow_Document.pdf
│
├── screenshots/
│   ├── home.png
│   ├── state-executive.png
│   ├── state-student.png
│   ├── state-personnel.png
│   ├── institution-student.png
│   └── institution-personnel.png
│
└── dax/
    └── measures.md
```

> **Note:** Do not upload sensitive or personally identifiable student/personnel information to a public GitHub repository. Use the synthetic/demo datasets for public demonstration.

---

# 🖥️ Dashboard Preview

### Home / Programme Overview

Add your screenshot here:

```markdown
![Home Dashboard](screenshots/home.png)
```

### State Executive

```markdown
![State Executive Dashboard](screenshots/state-executive.png)
```

### State Student

```markdown
![State Student Dashboard](screenshots/state-student.png)
```

### State Personnel

```markdown
![State Personnel Dashboard](screenshots/state-personnel.png)
```

### Institution Student

```markdown
![Institution Student Dashboard](screenshots/institution-student.png)
```

### Institution Personnel

```markdown
![Institution Personnel Dashboard](screenshots/institution-personnel.png)
```

---

# 💡 Business Value

The dashboard provides a single analytical layer for understanding programme performance.

Instead of reviewing assessment responses individually, users can quickly answer questions such as:

- How many students participated?
- How many personnel participated?
- Which districts are active?
- Which institutions are covered?
- How did Pre and Post assessment scores change?
- What is the overall learning gain?
- How many students showed improvement?
- How are personnel outcomes changing?
- How does performance vary across modules?
- How can a specific institution be investigated?

---

# ⚠️ Data Disclaimer

The publicly shared/demo version of this project may contain **synthetic or demonstration data**.

The dashboard structure, analytical model and methodology are intended to demonstrate the BI solution and should not be interpreted as representing actual statewide programme outcomes unless connected to verified production data.

No personally identifiable student or personnel information should be published in the repository.

---

# 🚀 Future Enhancements

Potential future enhancements include:

- Automated data refresh
- Production-scale data integration
- Additional programme modules
- Expanded district and institution coverage
- Automated report distribution
- Advanced predictive analytics
- Additional operational monitoring
- Intervention/action tracking
- Production deployment and governance

These are **future enhancements**, not necessarily part of the current implementation.

---

# 📚 Skills Demonstrated

This project demonstrates practical experience in:

- Business Intelligence
- Power BI
- Power Query
- DAX
- Data Cleaning
- Data Transformation
- Data Modelling
- Star Schema
- KPI Development
- Assessment Analytics
- Pre/Post Analysis
- Learning Gain Analysis
- Geographic Analytics
- Interactive Dashboard Design
- Executive Reporting
- Data Storytelling

---

# 👨‍💻 Project

**Statewide Safety, Protection & Wellbeing Programme Analytics Dashboard**

**Domain:** Education / Safety & Wellbeing / Programme Monitoring  
**Platform:** Microsoft Power BI  
**Geography:** Madhya Pradesh, India  
**Dashboard Type:** Interactive Programme Analytics & Decision Support

---

## ⭐ Key Takeaway

> **From raw assessment responses to actionable programme insights — this Power BI solution connects participation, assessment performance and learning outcomes across state, district and institution levels.**

---

### 🔗 Suggested GitHub Repository Name

```text
statewide-safety-wellbeing-powerbi-dashboard
```

or, more professional:

```text
MP-Safety-Wellbeing-Programme-Analytics
```

**I recommend the second one** for your portfolio because it is concise, domain-specific and looks professional on a resume/GitHub profile.
