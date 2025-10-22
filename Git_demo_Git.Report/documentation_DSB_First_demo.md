# Power BI Semantic Model & Report Documentation

## 0. Metadata Header
| Field | Value | Notes |
|-------|-------|-------|
| Model Name | DSBFirst_demo Semantic Model | |
| Report(s) / App(s) Served | Overblik | Section name |
| Version | v5.66 | From report config |
| Status | Draft | Update when promoted |
| Sensitivity Classification | Internal | Adjust if needed |
| Business Owner | (Fill in) | |
| Technical Owner | (Fill in) | |
| Data Steward | (Fill in) | Required for certification |
| Support Channel | (Fill in) | Teams / DL |
| Last Updated | 2025-10-22 | |
| Jira/DevOps References | (Fill in) | |

## 1. Purpose & Scope
- Business objectives: Overview of calendar (years, months, holidays).
- Core questions:
  - Count of dates per year/month.
  - Distribution of holidays across months/years.

## 2. Audience & Usage
| Persona | Notes |
|---------|-------|
| Analyst | Reviews calendar & holiday counts |
| Finance Analyst | Potential planning reference |

## 3. Lineage & Architecture
Source (ANALYST v_dim_Tid_Kalender) → Semantic Model → Report (Overblik) → App (if published)
Downstream dependencies: None listed.

## 4. Data Sources
| Source Name | Type | Connection | Sensitivity | Refresh Type | Owner | Reliability Notes |
|-------------|------|-----------|-------------|--------------|-------|-------------------|
| ANALYST v_dim_Tid_Kalender | Database Table | Import/DirectQuery (TBD) | Internal | Full | (Fill in) | Stable calendar dimension |

## 5. Transform / ETL Summary
- Aggregations: Count, Min, CountNonNull.
- Filter: Year between 2023 and 2025.
- Reconciliation: Counts align with source table rows.
- Caveats: Limited year range.
- Orchestration: (Fill in if dataflows / pipelines)

## 6. Model Design Overview
- Schema: Simple (single dimension referenced).
- Fact tables: None (dimension-driven visuals).
- Dimension: v_dim_Tid_Kalender (Year, Month Name, Date, Holiday flag).
- Relationship exceptions: None.

## 7. Measures / KPI Catalog
| Measure | Definition | Expression | Time Context | Data Quality Rule | Owner | Last Modified |
|---------|------------|-----------|--------------|-------------------|-------|---------------|
| Count of DATO_KORT | Dates per year/month | COUNT(DATO_KORT) | Year, Month | Non-null dates | (Fill in) | 2025-10-22 |
| Min of DATO_KORT | Earliest date per year/month | MIN(DATO_KORT) | Year, Month | Valid date | (Fill in) | 2025-10-22 |
| CountNonNull HELLIGDAG | Holidays per year/month | COUNTNONNULL(HELLIGDAG) | Year, Month | Non-null holiday flag | (Fill in) | 2025-10-22 |

## 8. Security & Access
### 8.1 RLS
No RLS implemented.

### 8.2 Workspace & Permissions
- Workspace: (Fill in)
- Roles & groups: (Fill in)
- Build permissions: (Scope) (Fill in)

### 8.3 Sensitivity & Export
- Label: Not applied.
- Underlying data export: Allowed (review if sensitive).

## 9. Refresh & Incremental Strategy
| Dataset | Schedule | Incremental | Historic Range | Rolling Window | Avg Duration (min) | P95 Duration (min) |
|---------|----------|------------|----------------|----------------|--------------------|--------------------|
| DSBFirst_demo Semantic Model | (Fill in) | No | N/A | N/A | (Fill in) | (Fill in) |

Dependencies: None beyond source.
Partition notes: Not applicable.

## Open Items
- Confirm connection mode.
- Populate ownership & support fields.
- Add lineage diagram.
- Validate sensitivity & export policy.

## Change Log
| Date | Change | Author |
|------|--------|--------|
| 2025-10-22 | Initial Confluence MD export | (Fill in) |
