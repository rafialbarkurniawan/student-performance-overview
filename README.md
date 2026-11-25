# Student Performance Dashboard (UCI Dataset)

## Business Purpose & Context
This dashboard provides an exploratory view of student academic records across two schools in Portugal—**Gabriel Pereira** and **Mousinho da Silveira**—to compare average final grades, absence levels, prior class failures, and weekly study time categories.

## Dataset Source & Attribution
- **Source:** UCI Machine Learning Repository — *Student Performance* dataset.
- **Attribution:** Cortez, P. (2008). Student Performance [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5TG7T. Licensed under CC BY 4.0.

## KPI Definitions
- **Student Records:** Total count of student records in the current filter or drill-through context (`649` on the overview page; `423` for Gabriel Pereira; `226` for Mousinho da Silveira).
- **Average Final Grade:** Mean final grade (`11.91` overall; `12.58` for Gabriel Pereira; `10.65` for Mousinho da Silveira).
- **Average Absences:** Mean number of school absences (`3.66` overall; `4.22` for Gabriel Pereira; `2.62` for Mousinho da Silveira).
- **Average First Period Grade:** Mean first-period grade (`11.40` shown on the overview KPI card).

## Category Transformations
- **Study Time Label:** Groups weekly study time into readable buckets (`Less than 2 hours`, `2 to 5 hours`, `5 to 10 hours`, and `More than 10 hours`).
- **Failure Category:** Groups prior class failure counts into labeled tiers (`No Previous Failure`, `1 Previous Failure`, `2 Previous Failures`, and `3 or More Failures`).
- **Filter Hierarchy:** Supports filtering across `School Name`, `Study Time Label`, and `sex` (`F` / `M`) on the overview page.

## Drill-Through Functionality
Right-clicking or drilling through from a school context opens a dedicated school detail view (with a back navigation button) that filters all visuals and KPI cards on that page to the selected school (`Gabriel Pereira` or `Mousinho da Silveira`), making it easier to inspect school-specific record counts, averages, failure breakdowns, and study-time patterns behind the combined overview numbers.

## Dashboard Screenshots
- **Overview Page:** `student-performance-overview.png` (*Academic Performance Overview*)
- **School Detail Pages:** `gabriel-pereira-school-detail.png` and `mousinho-da-silva-school-detail.png` (filtered detail pages for each school)

## Key Insights Found
- **School Differences:** Gabriel Pereira has a higher average final grade (`12.58`) than Mousinho da Silveira (`10.65`).
- **Study Time Pattern:** Average final grades tend to be highest in the `5 to 10 hours` and `More than 10 hours` categories, lower for `2 to 5 hours`, and lowest for `Less than 2 hours`.
- **Previous Failures:** Higher counts of previous class failures align with lower average final grades across both schools.
- **Absence Variation:** Average absences are higher at Gabriel Pereira (`4.22`) than at Mousinho da Silveira (`2.62`).
- **Drill-Through Context:** Drill-through separates school-level distributions and averages from the combined `649`-record overview, giving clearer context behind summary totals.

## Data Limitations & Caveats
- **Limited geographic scope:** Data originates from two schools in Portugal and cannot be generalized to the entire student population.
- **Collection method:** Data comes from school records and questionnaires rather than a real-time educational monitoring system.
- **No unique student ID:** No unique student identifier is provided; record/row counts should not be presented as verified unique individuals.
- **No causal proof:** Relationships between study time, absences, previous failures, and grades do not establish causation.
- **G1, G2, and G3 correlation:** `G3` is the final grade, while `G1` and `G2` represent earlier periods. Because UCI notes strong correlation among `G1`, `G2`, and `G3`, earlier period grades should not be used as independent proof that other factors caused changes in `G3`.