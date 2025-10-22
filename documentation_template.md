# Power BI Semantic Model & Report Documentation Template

> Fill all fields marked **Required** before promotion to Production. Fields marked **(Cert)** are required for Certification. Optional sections can be deferred but recommended.
> Use consistent naming. Keep this file versioned beside the PBIX / deployment artifacts. Generate dynamic metrics (size, refresh stats) via scripts where possible.

---
## **0. Metadata Header**  
| Field | Value | Notes |
|-------|-------|-------|
| Model Name |  | **Required** |
| Report(s) / App(s) Served |  | **Required** (list main downstream assets) |
| Version |  | **Required** (semantic model version tag e.g. v1.3) |
| Status | Draft / Production / Certified | **Required** |
| Sensitivity Classification | Internal / Confidential / Restricted | **Required** align with labels |
| Business Owner |  | **Required** |
| Technical Owner |  | **Required** |
| Data Steward |  | **Required for Certified** |
| Support Channel |  | Teams channel / email DL |
| Last Updated |  | Auto-populate in pipeline if possible |
| Jira/DevOps References |  | Link to change epics / tasks |

---
## **1. Purpose & Scope**  
**Required**  
- Business objectives:  
- Core business questions answered:  
  

---
## **2. Audience & Usage**  
**Required**  
Only capture persona and a concise note (timing or usage detail can be embedded in the note if needed).

| Persona | Notes |
|---------|-------|
| e.g. Finance Analyst | Reviews daily margin variance 07:30–09:00 CET |

---
## **3. Lineage & Architecture**  
**Required**  
Diagram link / screenshot:  
Narrative: Source → (Dataflow) → Dataset → Reports → App(s)  
Downstream dependencies (reports/apps/other datasets reusing this):  

---
## **4. Data Sources**  
**Required**  
| Source Name | Type (DB/File/API) | Connection Method | Sensitivity | Refresh Type | Owner | Reliability Notes |
|-------------|--------------------|-------------------|------------|--------------|-------|-------------------|
|  |  |  |  | Full / Incremental |  |  |

---
## **5. Transform / ETL Summary**  
**Required**  
- Key transformation steps (joins, filters, aggregations):  
- Reconciliation logic (e.g. totals match ERP):  
- Assumptions / data caveats:  
- Power Automate / Orchestration jobs (IDs/links):  

---
## **6. Model Design Overview**  
**Required**  
- Schema style (Star / Hybrid / Justification if not Star):  
- Fact Tables (name + grain):  
- Dimensions (name + role; note role-playing):  
- Relationship exceptions (bi-directional & rationale):  

---
## **7. Measures / KPI Catalog**  
**Required**  
| Measure Name | Business Definition | DAX Expression (or link) | Time Context | Data Quality Rule | Owner | Last Modified |
|--------------|---------------------|--------------------------|--------------|-------------------|-------|---------------|
|  |  |  |  |  |  |  |

---
## **8. Security & Access**  
**Required**  
### 9.1 RLS Roles (omit if none)  
| Role | Filter Logic | Mapping Source | Test User | Last Test Date | Notes |
|------|-------------|---------------|-----------|----------------|-------|
|  |  |  |  |  |  |

### 9.2 Workspace & Permissions  
- Workspace name:  
- Roles (Viewer/Contributor/Member/Admin) & justification (list groups):  
- Dataset Build permission scope:  

### 9.3 Sensitivity & Export Settings  
- Sensitivity label applied?  
- Underlying data export allowed? (Y/N + rationale)  

---
## **9. Refresh & Incremental Strategy**  
**Required**  
| Dataset | Schedule (Local Time) | Incremental? | Historic Range | Rolling Window | Avg Duration (min) | P95 Duration (min) |
|---------|-----------------------|-------------|----------------|----------------|--------------------|--------------------|
|  |  |  |  |  |  |  |

Dependencies order (dataflows first, then dataset):  
Partition key & policy notes:  

---
*Template truncated intentionally at Section 9 per customization requirements.*
