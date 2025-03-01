# Poly-Ocular Implant Dimension Inspections for Production Campaigns
This Power BI project takes a look at the dimensions of implants at two different sizes to determine implant cutting precision (per size) as well as assessing the efficiency in the implementation of emerging technology for implant inspections. 

## Project Background
Poly-Ocular is a Australian ophthalmology company specialising in the development of innovative biodegradable polymeric implants capable of sustained drug delivery to the eye. One of Poly-Ocular’s partner contract research organisations (CRO), Company PMP, responsible for producing ocular implants at large-scale, has implemented a digital microscope to the manufacture process to inspect and measure the dimensions of implants cut at two different sizes (Size A and B). This digital inspection technique significantly improves efficiency by inspecting the volume of up to 60 implants at a time, comparing against upper and lower bound specifications to determine whether implants have passed, and provides greater dimensional details of implants when compared to the typical method of manual inspection of implants by mass via analytical balances. This analysis aims to extract insights pertaining to the dimensions of Size A and B implants to determine accuracy and precision of cutting, pass rates per specifications, and trend analyses over time. Inspection efficiency is observed to gauge level of improvement in productivity resulting from implantation of the digital microscope. 

_<ins>Disclaimer</ins>: The original dataset for this analysis, and therefore resulting insights, have been altered, and key details of this project left intentionally vague or anonymised as to avoid the use of any confidential information._

## Analytic Objectives

1. Calculations: To have a better statistical grasp of the inspected implant dimensions and understanding the accuracy and precision of implants cut at Size A and Size B for production.
  - Statistics: Averages, Standard Deviations (SD), and % Relative Standard Deviations (%RSD)
  - On: Length, Diameter, and Volume
  - Grouped by: Passed implants, and Total implants

2. Visualisations: To illustrate inspection data to better understand trends pertaining to implant volumes, pass rates and inspection efficiency for Size A and B implants. 
  - Time series:
      - Plotting average and individual implant volumes, and trends over time.
      - Pass rates at a given time, and over time.
  - Granular visualisation

 Analysis will be conducted on Microsoft Power BI.

## Executive Summary
Dimensional analysis of passed Size A and B implants demonstrated that implant measurements were consistent across the board, with both sizes achieving volumes close to the target volume specifications, deviating by +2.35% and -0.35% respectively, thereby demonstrating accuracy. The low % relative standard deviations (%RSD) observed for Size and B implants of 1.93% and 2.12% also showed high levels of precision. This indicated that the cutting output of Size A and Size B implants during manufacture was satisfactory and appropriate for upscaled production. 
Pass rate assessments showed that Size A implants were more susceptible to failing volume specifications than Size B implants, with overall pass rates of 73.5% and 93.8% respectively. 
Trend-over-time analysis of the two implant sizes suggest that though there is no significant trending changes in volume over time for both size groups, Size A demonstrates a slight increase in pass-rates over time, whereas Size B remains almost constant. A possible reason for this may be improvements in cutting techniques over time, given Size A implants were cut and inspected before the Size B implants, where production technicians would be more experienced in the process. 
Assessment of individual implants volumes revealed that a significant proportion of failed Size A implants tended to exceed the upper volume specification, indicating the cutting device may require slight recalibration to lower implant volumes. Majority of Size B implants however were sufficiently within the target volume window and therefore no adjustments are necessary. 

## Dataset Overview
Instrument collects all data. Exportable Excel file for the two FP batches (80 and 160 mcg).
Dataset consists of the following columns:
- Implant #
- Time of Measurement (Date/Time)
- OK/NG (Passed or Failed on Volume Specification)
- Lot/Slide #
- Serial Counter
- Diameter (mm)
- Length (mm)
- Volume (mm3)
Dataset has undergone cleaning/wrangling prior to analysis (Power Query).

**Dataset**\
![image](https://github.com/user-attachments/assets/25385b53-ea1e-4d9e-b5d2-67719f693ea4)

**Entity Relationship Diagram**\
![image](https://github.com/user-attachments/assets/2694ecc7-2cc2-494e-8851-eb3568cd4bef) ![image](https://github.com/user-attachments/assets/b4073131-c945-4b0a-a68b-05cd3b1f533a)





