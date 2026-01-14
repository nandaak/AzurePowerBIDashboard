# Enterprise Quality & Test Management Dashboard
**Azure DevOps Integration via Power BI Fabric**

## Overview
This enterprise-level reporting solution provides end-to-end visibility into test management, execution, and quality metrics. By integrating **Azure DevOps Analytics (OData)** and **REST APIs**, it serves as a central "source of truth" across all IT business areas, including Corporate Systems, Marketing, and POS/Pharmacy.

> This central “source of truth” now provides visibility across all IT areas such as including Corporate Systems, Marketing,  POS/Pharmacy and any Areas defined in DevOps Organization.


## Business Value
- **Transparency:** Real-time QA transparency for both leadership and delivery teams.
- **Efficiency:** 100% elimination of manual spreadsheet-based status tracking and reporting effort.
- **Risk Mitigation:** Faster identification of coverage gaps, quality trends, and execution bottlenecks.
- **Standardization:** Unified QA metrics across diverse IT business units.

## Technical Architecture
- **Data Integration:** Combines Azure DevOps OData queries, REST APIs, SQL Server tables, and Excel datasets.
- **Semantic Modeling:** Scalable model consolidating Test Plans, Suites, Runs, and Points alongside User Stories, Bugs, and Requirements.
- **Automated Distribution:** Local PowerShell scripts extract high-priority metrics from the semantic model to send automated status emails to stakeholders twice daily.

# Dashboard Capabilities

### Executive Dashboard - QA Overview
- Organization-wide visibility across all active IT test plans.
- Real-time tracking of execution phases (Planning vs. Execution).
- Critical metrics: Execution %, duration, last activity, and ownership.
- **Deep-Dive Navigation:** Interactive drill-down from summary views to detailed execution analytics for individual test plans.

![Dashboard](images/DashBoard.jpg)
*High-level visibility across Corporate, Marketing, and POS/Pharmacy and other IT/Business areas.*

### QA Timeline
- Current time of QA testing across IT Areas

![Dashboard](images/Timeline.jpg)
*QA Testing timeline across all IT/Business areas.*

### QA Team OrgChart
- Current QA Team org chart for visibility and information

![Dashboard](images/QAOrg.jpg)
*QA Testing team org chart*

# Test Plan Report - Capabilities
### 1. Test Execution & Quality Analytics
- **Live Status Tracking:** Real-time visibility into Passed, Failed, Blocked, NA, and Pending statuses.
- **Build Quality Indicators:** Automated pass/fail ratios to identify execution gaps instantly.
- **Trend Analysis:** 14-day execution trends using stacked area charts to visualize velocity and stability.

![Daily Execution Report](images/1_Execution_Report.jpg)
*Real-time metrics showing 74% execution and 96.5% build quality.*

### 2. End-to-End Traceability
- **Requirement-to-Defect Mapping:** Full visibility from User Stories to Test Cases to Bugs.
- Coverage percentage by feature and requirement
- **Compliance Monitoring:** Automated visualization of requirement coverage (Pass/Fail/Pending).
- Ensures strict adherence to Azure DevOps requirement-based test suite standards.

![Requirements Traceability](images/2_Test_Plan_Requirements.jpg)
*Requirement coverage heatmap ensuring 100% traceability for all user stories.*

### 3. Failed Test Case Triage
- Designed for triage, this view focuses exclusively on what is not working.
- **Execution Trend (14 Days):** A stacked area chart visualizes the volume of passed, failed, and blocked tests over the last two weeks, helping identify if failures are increasing or stabilizing.
- **Failure Details:** Lists specific Test IDs, titles, the assigned tester, and the priority of the failing case.
- **Resource Allocation:** Includes an “Executed By” table to track individual tester output.

![Failed Test Report](images/4_Failed_Tests.jpg)
*Detailed failure analysis, including 14-day execution trends and assigned testers.*

### 4. Defect & Blocker Management
- **Bug Lifecycle Tracking:** Metrics by severity (High/Medium/Low) and state (Active/Closed/Remediation).
- **Bug metrics by:**
  1. Severity (High, Medium, Low)
  1. State (Active, Closed)
- **Traceability of bugs to:**
  1. Test Cases
  1. User Stories (per Azure DevOps best practices)
- **Visibility into:**
  1. New bugs found
  1. Active vs closed defects
  1. Fixed, tested, and closed lifecycle states
- **Issues and impediments tracking linked to test plans**


![Active Bugs Report](images/3_Active_Bugs.jpg)
*Tracking defect severity, aging, and direct links to user stories.*

### 5. Issues & Environment Status
The final dashboard tracks impediments that are not necessarily software bugs but block testing progress.
-	**Blocker Tracking:** Lists states, severity, and titles for impediments like environment outages or data setup issues.
-	**Mitigation Planning:** Includes columns for “Impact” and “Mitigation” to document how the team is working around current blockers.
-	**Service Status:** Features a “Service Status” indicator light to provide an at-a-glance view of the testing environment’s health.

![Issues and Impediments Report](images/5_Issues.jpg)
*Real-time tracking of environment blockers and service status indicators.*

