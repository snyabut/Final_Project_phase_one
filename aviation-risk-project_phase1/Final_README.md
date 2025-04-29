# Aviation Risk Analysis for Business Recommendations

## Overview

This project analyzes civil aviation accident data from the National Transportation Safety Board (NTSB) covering **1990–2023**.  
The goal is to identify aircraft models with lower accident risk based on historical fatality and damage outcomes.  
The insights help guide strategic decisions as the company enters the aviation sector by purchasing and operating aircraft.

---

## Business Understanding

### Business Goal
Support the company’s new aviation division in selecting aircraft models that present lower operational risks.

### Stakeholder
The Head of Aviation Division — responsible for making aircraft purchasing decisions.

### Key Business Questions
- Which aircraft models have historically shown **lower fatal accident rates**?
- Which models have demonstrated **lower severe damage rates**?
- Are there models that perform well on **both** fatality and damage metrics?
- What are the **accident trends** in aviation from 1985 to 2023?

---

## Data Understanding & Analysis

### Source of Data
- **Dataset:** National Transportation Safety Board (NTSB) Aviation Accident Database (1962–2023)
- **Files Used:**
  - `AviationData.csv`

### Data Cleaning and Preparation
- Standardized column names
- Dropped irrelevant or highly missing columns
- Converted dates; extracted.
- Filled missing numeric values with `0`; filled categorical nulls with `'Unknown'`
- Created new features:
  - `combined_aircraft_type` = Make + Model
  - `is_fatal` and `is_severe_damage` binary flags

### Data Filtering
- Focused on events **from 1985 onwards**
- Included only relevant `purpose_of_flight` categories
- Excluded amateur-built aircraft
- Focused on `ACCIDENT` investigation types only

---

## Key Visualizations

- **Accident Counts Over Time (1985–2023)**  
  Showed gradual decrease in aviation accidents, stabilizing after 2010.
  
- **Top 5 Aircraft by Lowest Fatal Accident Rate (%)**  
  Highlighted models like the Cessna 172S and Piper PA-28-161.

- **Top 5 Aircraft by Lowest Severe Damage Rate (%)**  
  Showed aircraft least likely to suffer substantial/destroyed damage.

- **Scatter Plot – Fatal vs. Severe Damage Rates**  
  Visualized aircraft models' risk profiles on both fatal and severe dimensions.

---

## Key Findings

- **Accident Trends:**  
  Aviation accidents decreased from 1985 to 2010, then stabilized.

- **Variation Across Models:**  
  Fatal accident rates ranged from around **2% to over 15%**.  
  Severe damage rates ranged from **40% to 90%** among different aircraft types.

- **Low-Risk Models Identified:**  
  Certain models consistently performed well on both fatality and severe damage metrics.

- **Limitation:**  
  The analysis is based on **proportions of accidents**. It does **not account for flight hours** (exposure), which could affect risk interpretation.

---

## Recommendations

### 1. Focus on Safer Aircraft Models
Prioritize aircraft types with historically lower fatal and severe damage rates:

Lowest Fatal Accident Rate                         | Lowest Severe Damage Rate:
----------------------------------------------------------------------------------------------------
LET BLANIK L-13                                    | BOEING 777
PIPER PA 18                                        | PIPER PA 46-350P
BOEING 777                                         | BEECH 1900D
GRUMMAN-SCHWEIZER G-164A                           | CESSNA 180J
SCHWEIZER SGS 2-33A                                | CESSNA 140A


### 2. Caution with Higher-Risk Models
Exercise caution with aircraft types showing high fatal or damage rates:
- BOEING 737-200
- BOEING 737
- BOEING 737-300
- BEECH 1900C
- BEECH 200

---

## Interactive Dashboard

Explore the dashboard here:  
 [Link to Interactive Dashboar](https://public.tableau.com/app/profile/samwel.ongechi/viz/Tableaudraft_17459046483820/Dashboard1?publish=yes)

Features:
- Filter by aircraft type, year, and purpose of flight
- View accident rates and severity visualizations
- Compare models interactively


