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

### Dataset
![image](https://github.com/user-attachments/assets/25385b53-ea1e-4d9e-b5d2-67719f693ea4)

### Entity Relationship Diagram
![image](https://github.com/user-attachments/assets/2694ecc7-2cc2-494e-8851-eb3568cd4bef) ![image](https://github.com/user-attachments/assets/b4073131-c945-4b0a-a68b-05cd3b1f533a)

## Insights and Discussions
### Passed Implants Statistics
Statistical Overview of Implant Dimensions:
- Implants dimensional measurements indicated that both Size A and B have achieved an average volume of 0.5803 mm^3 and 1.1296 mm^3, with deviations from target volumes by +2.39% and -0.35%, respectively.
- Diameter is consistent between the two sizes of implants, with averages differing by only 0.0013 mm, which is expected as both Size A and B implants are manufactured from the same synthesised polymer rods and then cut to different lengths. This does indicate excellent uniformity of the synthesised polymer rods prior to being cut, also reflected by % RSD values of < 1%. 
- Size A implants are half the length of Size B implants by design and is consistent with the length measurements. The SD of lengths are not notably different between the two sizes, being 0.073 and 0.086 mm for Size A and B respectively, though this results in a greater %RSD in Size A lengths than Size B of 2.1% and 1.3%, considering Size A implants are smaller. As the SD in length between the two sizes is marginal, this demonstrates a constant, intrinsic error margins of the cutting procedure rather than other attributing factors such as smaller implants being more difficult to handle for production technicians. Overall, this still represents highly satisfactory levels of cutting accuracy and precision.

Implant Inspection Count:
- 22,234 total implants were cut over 15 days, with Size B implants having a higher pass rate than Size A implants. This indicates that implants of both sizes are yielding satisfactory pass rates using the current upscale cutting method, and the effectiveness of the digital microscope in high-output inspections. 
![image](https://github.com/user-attachments/assets/e13656ad-5c63-4f62-bf1a-93fb0720fefe)

### Pass Rate Assessments
- Size A implants have an overall pass rate of 73.5%, demonstrating slightly cyclical behaviour over a day-by-day basis. The lowest pass rate of 61.2% was on 13th of May, and highest was 81.4%, on the 4th and 9th day of the 10-day production campaign. Though the trendline would not be deemed significant, there does seem to be an improvement in cutting accuracy over time, as daily pass rates achieved over 80% only on the last 2 days. 
- Size B implants however had a much greater pass rate of 93.8%, remaining at a near constant daily-average throughout the 5 days of production, as the lowest and highest rates differed by only 5.5%. This is an expectable outcome due to Size B being double the size and hence easier to achieve the target volume, as well as there possibly being a greater inherent error associated with cutting smaller implants. 

### Size A and B Trend Analysis
Provides more detailed analytics on Size A implant volumes, with finer granularity. Focuses on moving averages and individual implant measurements over time. Also includes dynamic visualisations on both dimension statistics and pass rates at a given time. 

Size A:
- Volume over time
    - The moving average volume of Size A passed implants keeps relatively consistent over the manufacture period, though it always remains above the target volume. There is a similar trend when observing the moving average volume of all implants, with most implants having a volume greater than the target and a few sporadic dips in the average. However, this can be attributed to the digital microscope taking the measurements of implant offcuts thereby occasionally skewing average volumes. 
- Individual implant volumes   
    - The scatterplot provides some finer granularity with respect to implant volumes, where the individual implant volumes can be examined. Significantly more implants fail due to being above the upper specification limit volume than those which are below, which may indicate the cutting device should be recalibrated to deliver slightly lower volumes so more individual implants are within the volume specification threshold. However, it can be noted that there are more low-volume outliers compared to high-volume outliers. This is due to a greater likelihood of the aforementioned offcuts to be created during cutting and subsequently measured, compared to significantly larger implants. 

Size B:
- Volume over time
    - The moving average volume of passed Size B implants is more consistent than Size A implants, keeping very near the target volume throughout. When considering all implants, the moving average is mostly nearly identical, with the occasional drop in the average, again primarily skewed by offcuts. 
- Individual implant volumes
    - Outlier measurements are less frequently observed in Size B implants. Similarly to Size A, there are more low-volume outliers compared to high-volume, resulting from implant offcuts. Overall, Size B implants have a much tighter spread of volumes, which are positioned well within the volume specification window thus yielding exceptional pass-rates. 

### Inspection Efficiency
Efficiency of the digital microscope is represented by plotting the number of implants inspected over the course of production for the two different sized implants. 
- The daily averages of both Size A and B implants are comparable, with 1534 and 1380 implants being inspected on average per day respectively, demonstrating tremendous output which is fitting for production campaigns. The number of implants which are inspected per action for Size A are nearly double that of Size B, which is expectable given being half the size of Size B, and therefore more implants can be cut from the same synthesised rod. 
- Inspection efficiency of Size A implants tends to be inconsistent, bouncing up and down over time. Inspection of Size B implants also lacked consistency, appearing to dip midway and increase near the end. However, inspection rates trended upwards to a significant degree over both production campaigns, suggesting the likelihood of production technician experience over time playing a factor on number of implants inspected. 

## Recommendations/Remarks
- Improving volume accuracy:
    - As it stands, both Size A and B implants are achieving the target implant volume to satisfactory degrees for production campaigns. Though, micro-adjustments to the Size A cutting measurement can be made to lower the target implant volume, so that more Size A implants fall within the volume specification threshold, thereby improving the pass rate of Size A implants. 
- Exploring methods to minimise formation and subsequent inspections of offcuts when cutting implants:
    - Several of the outlier volume measurements, particularly for Size A implants, comprised of implant offcuts. Albeit being small in volume, offcuts represent a degree of wastage when aggregated, and thereby identifying methods of minimising offcuts formation can lead to more synthesised polymer material being available for production and therefore greater implant yield. Production technicians may be able to assist with method optimisation strategies. 



