# Mapping Potential Environmental Justice Concerns in Monterey County

**Comparing RMP Facility Proximity with Demographic Characteristics in Monterey County**

## Purpose

This repository contains an exploratory analysis using data from the Environmental Protection Agency's (EPA) Environmental Justice Mapping and Screening tool (EJSCREEN). This project compares Risk Management Program (RMP) facility proximity with the distribution of demographic characteristics in Monterey County. RMP facilities handle regulated substances and are required by the EPA to develop a Risk Management Plan for preventing and responding to accidental chemical releases. RMP facility proximity, the distribution of people of color (POC), and limited english-speaking households were mapped to assess potential environmental justice issues.

## Data 

**Data Access**

The EJSCREEN tool was developed by the EPA and combines environmental and demographic indicators. The demographic indicators are based on the U.S. Census Bureau’s American Community Survey (ACS) 2017–2021 5-year Summary [3].

The raw dataset was originally obtained from the EPA website and was accessed from a [Google Drive folder](https://drive.google.com/file/d/1nG6Nj1bXfzQFOVMO8Km3eNy4SWu1YcIQ/view). 


**Data Organization**

    EDS-HW1
    ├── data
    │   └── ejscreen
    ├── hw1-map-making.html
    ├── hw1-map-making.qmd
    └── README.md

**Libraries:**

* `library(tidyverse)`

* `library(sf)`

* `library(here)`

* `library(stars)`

* `library(tmap)`


**Project Variables:**

* People of color percentage (`PEOPCOLORPCT`)

* Limited english-speaking households percentile (`P_LINGISOPCT`)

* RMP facility proximity percentile (`P_PRMP`)

**Data Cleaning**

EJSCREEN data were filtered to Monterey County and to Census block groups with a reported population. Coordinates for selected communities in Monterey County were stored in a simple feature layer and transformed to match the Coordinate Reference System (CRS) of the EJSCREEN dataset.

**Thresholds**

* High RMP facility proximity
  90th percentile and above (`P_PRMP >= 90`)

* High percentage of people of color
  65% or above (`PEOPCOLORPCT >= 0.65`)

## Author
Veronica Moran

Master of Environmental Data Science (MEDS), UC Santa Barbara

## References

[1]. U.S. Environmental Protection Agency. (2021). *Environmental Justice Screening and Mapping Tool: What is EJSCREEN*. (https://19january2021snapshot.epa.gov/ejscreen/what-ejscreen_.html) [Accessed: October 7, 2026]

[2]. U.S. Environmental Protection Agency. (2025, December 4). *Risk Management Program (RMP) Rule Overview*. (https://www.epa.gov/rmp/risk-management-program-rmp-rule-overview) [Accessed: October 7, 2026]

[3]. U.S. Environmental Protection Agency (EPA), 2023. *EJScreen Technical Documentation*.

[4]. Frey, W. H. (2021, August 13). *New 2020 census results show increased diversity countering decade-long declines in America’s white and youth populations*. Brookings Institution. (https://www.brookings.edu/articles/new-2020-census-results-show-increased-diversity-countering-decade-long-declines-in-americas-white-and-youth-populations/) [Accessed: October 9, 2026]