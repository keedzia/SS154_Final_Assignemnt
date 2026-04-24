# Watching the Watchers: Body-Worn Cameras and Their Role in De-escalating Police Lethal Force

## Authors
Nika Gudelj, Karolina Kędzia, Joseph (Sang Seung) Sa  
Minerva University — SS154 Econometrics and Economic Systems  
Spring 2026

## Overview
This repository contains the R code for our final project examining whether the presence of body-worn cameras (BWCs) causally reduces police officers' reliance on lethal force during fatal encounters in the United States between 2015 and 2022.

## Research Question
Does the presence of a body-worn camera on an officer reduce their reliance on lethal force?

## Data
- **Primary dataset**: Washington Post Fatal Force Database (2015–2022), 8,002 fatal police shooting incidents
- **Instrument**: City-level federal Bureau of Justice Assistance (BJA) Body-Worn Camera grants (CFDA 16.835)
- **Dataset link**: [SS154 Police Force Dataset (IV update)](https://docs.google.com/spreadsheets/d/1ZuJv4wR6yPswZuRPkcL5ay-bHw5EznC9AMBgt-CnDpU/edit?gid=601390919#gid=601390919)
- **Codebook**: [Variable Codebook](https://docs.google.com/document/d/1RBhRQPWqvPH_UEIJPim9pGNow-uNVjxqWKvWKMndsmg/edit?tab=t.0)

## Key Variables
| Variable | Description |
|---|---|
| `lethal_response` | Outcome: 1 = shot only, 0 = shot and Tasered |
| `body_camera` | Treatment: BWC present (TRUE/FALSE) |
| `bwc_grant_active` | Instrument: city received federal BWC grant |
| `race` | Race of victim |
| `age` | Age of victim |
| `gender` | Gender of victim |
| `signs_of_mental_illness` | Mental illness indicator |
| `threat_level` | Threat level at time of incident |
| `flee` | Fleeing behavior |
| `armed` | Weapon type carried |
| `state` | US state |

## Methods
- Logistic Regression (with and without state fixed effects)
- Instrumental Variables / 2SLS (`ivreg` from AER package)
- OLS Linear Probability Model (robustness check)
- Manual IV Second Stage (robustness check)


## Requirements
```r
install.packages(c("dplyr", "AER", "lmtest", "kableExtra"))
```
