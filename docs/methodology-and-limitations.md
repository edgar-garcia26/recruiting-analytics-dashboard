# Methodology and limitations

## Delivery approach

1. **Foundation**  
   Defined the business need, scope, objectives, risks, success measures, and deliverables.

2. **Elicitation**  
   Captured stakeholder pain points, reporting priorities, and decisions the dashboard needed to support.

3. **Requirements**  
   Developed requirements, user stories, process maps, and approved wireframes.

4. **Data quality**  
   Profiled the source tracker, documented missing and inconsistent fields, and reviewed probable duplicates.

5. **Preparation**  
   Standardized data types and created refresh-based aging and chronological month logic in Power Query.

6. **Modeling**  
   Created KPI, rate, aging, and display-label measures in DAX.

7. **Visualization**  
   Built four coordinated pages with slicers, navigation, cards, charts, and tables.

8. **Validation**  
   Corrected chronology, labels, table usability, spacing, and final PDF presentation.

## Documented data-quality findings

- Three probable duplicate records were excluded.
- Forty-three application-source values remained `Unknown`.
- Work Type was largely incomplete, so work-arrangement analysis was deferred.
- Twenty-one salary records were missing.
- Hourly and annual salaries were not combined into one average.
- The tracker did not contain follow-up dates, contact history, interview stages, or rejection reasons.

## Interpretation limits

The dashboard represents the latest recorded outcome for each application, not a complete history of status changes.

Application volume should not be treated as a measure of application quality. The small number of recorded interviews also means that category-level interview rates should be interpreted carefully.

## Public-release limitations

The raw dataset and PBIX model are not included because they contain personal job-search records. The public sample file is synthetic.
