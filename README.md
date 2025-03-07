# Poly-Ocular Implant Dimension Inspections for Upscale Production

## Project Background
Poly-Ocular is an Australian ophthalmology company specialising in the development of innovative biodegradable polymeric implants capable of sustained drug delivery to the eye. One of Poly-Ocular’s partner contract research organisations (CRO), Company PMP, responsible for producing ocular implants at large-scale, has implemented a digital microscope to the manufacture process to inspect and measure the dimensions of implants cut at two different sizes (Size A and B). This digital inspection technique is expected to significantly improve efficiency by inspecting the volume of up to 60 implants at a time, compare against set upper and lower bound specifications to determine whether implants pass, and provide greater dimensional details of implants when compared to the typical method of manual inspection of implants by mass via analytical balances. This analysis aims to extract new insights pertaining to implant inspections, including the dimensions of Size A and B implants to determine accuracy and precision of cutting during upscale production, pass rates per specifications, and trend analyses over time. Inspection efficiency is observed to measure the improvement in productivity resulting from implementation of the digital microscope. 

_<ins>Disclaimer</ins>: The original dataset for this analysis, and therefore resulting insights, have been altered, and key details of this project left intentionally vague or anonymised as to avoid the use of any confidential information._

## Analytic Objectives

1. To have a better statistical grasp of the inspected implant dimensions and understanding the accuracy and precision of implants cut at Size A and Size B for production.
    - Statistics: Averages, Standard Deviations (SD), and % Relative Standard Deviations (%RSD)
    - On: Length, Diameter, and Volume
    - Grouped by: Passed implants, and Total implants

2. To visualise inspection data to better understand trends pertaining to implant volumes, pass rates and inspection efficiency for Size A and B implants. 
    - Time series:
        - Plotting average and individual implant volumes, and trends over time.
        - Pass rates at a given time, and over time.
    - Granular visualisation

Analysis will be conducted on Microsoft Power BI. 

The Microsoft Power BI Desktop file (.pbix) can be downloaded for viewing using the following [link](https://github.com/RafeedF/1-Implant_Dimensions_Analysis/blob/main/Implant%20Dimension%20Analytics%20Project.pbix).

## Executive Summary
Dimensional analysis of passed Size A and B implants revealed that implant measurements were consistent across the board, with both sizes achieving volumes close to the target volume specifications, deviating by +2.35% and -0.35% respectively, thereby demonstrating accuracy. The low % relative standard deviations (%RSD) observed for Size and B implants of 1.93% and 2.12% also showed high levels of precision. This indicated that the cutting output of Size A and Size B implants during manufacture was satisfactory and appropriate for upscaled production. 
Pass rate assessments showed that Size A implants were more susceptible to failing volume specifications than Size B implants, with overall pass rates of 73.5% and 93.8% respectively. 
Trend-over-time analysis of the two implant sizes suggested that though there were no significant trending changes in volume over time for both size groups, Size A demonstrated a slight increase in pass-rates over time, whereas Size B remained near-constant. 
Assessment of individual implants volumes revealed that a significant proportion of failed Size A implants tended to exceed the upper volume specification, indicating the cutting device may require slight recalibration to lower implant volumes. Majority of Size B implants however were sufficiently within the target volume window and therefore no adjustments are necessary. 

## Dataset Overview
The digital microscope collects and records all data as measurements are taken, and is saved as an exportable Excel file. These files have been 
Datasets consist of the following columns:
- Implant #
- Time of Measurement (Date/Time)
- OK/NG (Passed or Failed on Volume Specification)
- Lot/Slide #
- Serial Counter
- Diameter (mm)
- Length (mm)
- Volume (mm^3)

_Italisised columns have been disregarded as they are not relevant for this analysis._

Dataset has undergone cleaning/wrangling prior to analysis (Power Query).

### Dataset
![image](https://github.com/user-attachments/assets/25385b53-ea1e-4d9e-b5d2-67719f693ea4)

### Entity Relationship Diagram
![image](https://github.com/user-attachments/assets/2694ecc7-2cc2-494e-8851-eb3568cd4bef) ![image](https://github.com/user-attachments/assets/b4073131-c945-4b0a-a68b-05cd3b1f533a)

## Insights and Discussions
### Passed Implants Statistics
Statistical Overview of Implant Dimensions:
- Implants dimensional measurements indicated that both Size A and B had achieved average volumes of 0.5803 mm^3 and 1.1296 mm^3, with deviations from target volumes by +2.39% and -0.35%, respectively.
- Diameter was consistent between the two sizes of implants, with averages differing by only 0.0013 mm, which was expected as both Size A and B implants were manufactured from the same synthesised polymer rods and subsequently cut to different lengths. This indicated excellent uniformity of the synthesised polymer rods prior to being cut, and also reflected by % RSD values of < 1%. 
- Size A implants were half the length of Size B implants by design which was consistent with the length measurements. The SD of lengths were not notably different between the two sizes, being 0.073 and 0.086 mm for Size A and B respectively, though this resulted in a greater %RSD in Size A lengths than Size B of 2.1% and 1.3%, considering Size A implants were smaller. As the SD in length between the two sizes was marginal, this demonstrated a constant, intrinsic error margin of the cutting procedure rather than other attributing factors such as smaller implants being more difficult to handle for production technicians. Overall, this still represented highly satisfactory levels of cutting accuracy and precision.

Implant Inspection Count:
- 22,234 total implants were cut over 15 days, with Size B implants having a higher pass rate than Size A implants. This indicated that implants of both sizes were yielding satisfactory pass rates using the current upscale cutting method, and the effectiveness of the digital microscope in high-output inspections. 

![image](https://github.com/user-attachments/assets/e13656ad-5c63-4f62-bf1a-93fb0720fefe)

### Pass Rate Assessments
- Size A implants had an overall pass rate of 73.5%, demonstrating slightly cyclical behaviour over a day-by-day basis. The lowest pass rate of 61.2% was on 13th of May, and highest was 81.4%, on the 4th and 9th day of the 10-day production campaign. Though the trendline would not be deemed significant, there did seem to be an improvement in cutting accuracy over time, as daily pass rates achieved over 80% on the last 2 days. 
- Size B implants however had a much greater pass rate of 93.8%, remaining at a near constant daily-average throughout the 5 days of production, as the lowest and highest rates differed by only 5.5%. This was an expectable outcome due to Size B being double the size and hence easier to achieve the target volume, as well as there possibly being a less inherent error associated with cutting larger implants. 

![image](https://github.com/user-attachments/assets/6bcbb6eb-6e8f-40e1-a8e5-9e1e77c5d0a8)

### Size A and B Trend Analysis
Provides more detailed analytics on Size A implant volumes, with finer granularity. Focuses on moving averages and individual implant measurements over time. Also includes dynamic visualisations on both dimension statistics and pass rates at a given time. 

Size A:
- Volume over time
    - The moving average volume of Size A passed implants kept relatively consistent over the manufacture period, though it always remained above the target volume. There was a similar trend when observing the moving average volume of all implants, with most implants having a volume greater than the target and a few sporadic dips in the average. However, this could be attributed to the digital microscope taking the measurements of implant offcuts thereby occasionally skewing average volumes. 
- Individual implant volumes   
    - The scatterplot provided some finer granularity with respect to implant volumes, where the individual implant volumes could be examined. Significantly more implants failed due to being above the upper specification limit volume than those which were below the lower specification, which could have suggested that recalibration of the cutting device may have be required to deliver slightly lower volumes, so that more individual implants could be within the volume specification threshold. However, it could be noted that there were more low-volume outliers compared to high-volume outliers. This was due to a greater likelihood of the aforementioned offcuts being created during cutting and subsequently measured, compared to large outliers implants. 

![image](https://github.com/user-attachments/assets/245d9b12-4cd9-4974-b4de-a9d94d704a0a)

Size B:
- Volume over time
    - The moving average volume of passed Size B implants was more consistent than Size A implants, keeping very near the target volume throughout. When all implants are considered, the moving average was mostly nearly identical, with occasional drops in the average, again primarily skewed by offcuts. 
- Individual implant volumes
    - Outlier measurements were less frequently observed in Size B implants. Similarly to Size A, there were more low-volume outliers compared to high-volume, resulting from implant offcuts. Overall, Size B implants had a tighter spread of volumes, positioned well within the volume specification window and thus yielding exceptional pass-rates. 

![image](https://github.com/user-attachments/assets/1639e3b1-95b0-47b0-b5dc-c8f03f70b5ea)

### Inspection Efficiency
Efficiency of the digital microscope was represented by plotting the number of implants inspected over the course of production for the two different sized implants. 
- The daily averages of both Size A and B implants were comparable, with 1534 and 1380 implants being inspected on average per day respectively, which demonstrated tremendous output which was suitable for production campaigns. The number of implants which were inspected per action for Size A was nearly double that of Size B, which was expectable given being half the size of Size B, and therefore more implants could be cut from the same synthesised polymer rod. 
- Inspection efficiency of Size A implants tended to be inconsistent, bouncing up and down over time. Inspection of Size B implants also lacked consistency, appearing to dip midway and increase near the end. However, inspection rates trended upwards to a significant degree over both production campaigns, which suggested the likelihood of production technician experience over time playing a factor in the number of implants inspected. 

![image](https://github.com/user-attachments/assets/a9c9852f-34f5-4dbf-97b6-b0779589e681)

## Recommendations/Remarks
Overall, the production of these implants had proved to be satisfactory for the purpose of upscaled production. Implants were cut to target volume accurately and with high precision, and both Size A and B implants yielded sufficient pass rates. Efficiency of inspections was also highly appropriate for upscaling activities. Given the generally positive insights extracted from this analysis, the following recommendations can be made to PMP to optimise their current processes:
- Improving volume accuracy:
    - As it stands, both Size A and B implants have achieved the target implant volume to satisfactory degrees for production campaigns. Though, micro-adjustments to the Size A cutting measurement can be made to lower the target implant volume, so that more Size A implants fall within the volume specification threshold, thereby improving the pass rate of Size A implants. 
- Exploring methods to minimise formation and subsequent inspections of offcuts when cutting implants:
    - Several of the outlier volume measurements, particularly for Size A implants, comprised of implant offcuts. Albeit being small in volume, offcuts represent a considerable degree of wastage when aggregated, and thereby identifying methods of minimising offcuts formation can lead to more of the synthesised polymer material being available for production of valid implants and therefore greater yield. Consulting production technicians to discuss possible method optimisation strategies to minimise offcuts may be beneficial to improve overall implant output.



