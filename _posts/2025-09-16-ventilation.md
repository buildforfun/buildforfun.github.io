---
title: Ventilation
date: 2025-09-16 21:02:00
categories: bem
---

# Ventilation

Total air out = total air in
Total air out - total air in = 0

External influences that affect a dwelling: wind, temp, altitude, shelter 

Airflow paths
- Windows: each openable part is a path, opening ratio,  
- Vents: solver adjusts opening to meet target ach 
- Leaks : air tightness test, 4 facades + 1 roof, coefficient spread by surface area
- Mechanical ventilation: imev, cmev, mvhr


Windows:
- Openable window parts (0-1) scales the flow coefficient 
- Responds to heating or user schdeule

Vents
- Trickle vents or air bricks 
- Adjustable vents (0-1)
- Equivalent area and discharge coefficient
- Min and max air change rate schedules 

Leaks:
- Infiltration through gaps in the building envelope
- Leakage coefficient is calculated from test - 50Pa
- Split into 5 airflows: 2 windward(low height and high height), 2 leeward , 1 roof pat

Mechanical ventilation
- Airflow is not pressure driven - based on design flow rate, control schedule,
- MVHR - supplies and extracts air at the same time 
- Treated as fixed flow

Each path has: 
- Flow coefficient
- Flow exponent
- Height above ground
- Wind pressure coefficient 

Calculate
1. External pressure for each path 
2. Internal pressure 
3. Pressure difference 
4. Volumetric flow rate (+ve if air enters)
5. Solve mass balance equation - solve for internal reference pressure that balances all flows using mass balance equations for all baths (total-total=0)
6. air change rate
7. ventilation heat loss 
