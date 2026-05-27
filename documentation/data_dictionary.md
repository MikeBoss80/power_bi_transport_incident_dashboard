# Data Dictionary — London Transport Safety Analysis

This document describes the structure, meaning, and preparation considerations of the dataset used in the **London Transport Safety Analysis Power BI Dashboard**.

The dataset contains transport-related incident records reported across London boroughs between **2015 and 2018**, including information about routes, operators, incident categories, victim demographics, and injury outcomes.

---

## Dataset Structure

| Column Name | Data Type | Description | Example Values | Notes |
|-------------|------------|-------------|----------------|-------|
| Date Of Incident | Date | Date when the transport-related incident occurred. | `2015-12-01`, `2017-04-14` | Used for trend and time-series analysis. |
| Route | Text | Transport route identifier associated with the incident. Includes numeric and alphanumeric routes. | `11`, `244`, `N11`, `88` | Missing values standardized as `Unknown`. |
| Operator | Text | Transport operator responsible for the service involved in the incident. | `London General`, `Metroline`, `Arriva London` | Used for operator-level analysis. |
| Group Name | Text | Parent organization or transport group associated with the operator. | `Go Ahead`, `Arriva Group` | Used for grouped transport company analysis. |
| Borough | Text | London borough where the incident occurred. | `Westminster`, `Lambeth`, `Croydon` | Used for geographical analysis and hotspot identification. |
| Injury Result Description | Text | Description of the injury severity or medical outcome resulting from the incident. | `Injuries treated on scene`, `Taken to hospital`, `Fatal` | Used for severity and outcome analysis. |
| Incident Event Type | Text | Type or category of the incident event. | `Slip Trip Fall`, `Collision Incident`, `Assault`, `Fire` | Used to identify the most frequent incident categories. |
| Victim Category | Text | Category of the person affected by the incident. | `Passenger`, `Pedestrian`, `Cyclist`, `Driver` | Used for victim segmentation analysis. |
| Victims Sex | Text | Reported sex of the victim involved in the incident. | `Female`, `Male`, `Unknown` | Used for demographic analysis. |
| Victims Age | Text | Age category of the victim. | `Adult`, `Youth`, `Child`, `Elderly` | Used for age-group segmentation. |

---

## Data Cleaning & Preparation

The following preprocessing actions were applied to improve consistency and analytical quality:

### Missing Values Handling
- Missing values in the **Route** column were standardized using the category:

```txt
Unknown
```

This approach preserves records while maintaining consistency during filtering and route-level analysis.

### Data Standardization
- Route identifiers containing alphanumeric values (e.g., `N11`) were preserved as valid route codes.
- Text values were standardized to improve consistency across categories and filtering.

### Data Modeling
The dataset was prepared for interactive analysis in **Power BI**, enabling:

- Dynamic filtering
- Cross-visual interactions
- Temporal analysis
- Victim segmentation
- Geographic comparisons by borough
- Operator performance analysis

---

## Analytical Scope

This dataset supports the analysis of:

- Transport incident trends over time
- High-risk boroughs
- Most affected victim groups
- Incident severity distribution
- Transport operator comparisons
- Most common incident event types
- Victim demographic patterns
