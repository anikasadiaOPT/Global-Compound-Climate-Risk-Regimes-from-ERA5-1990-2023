# 📔 Project Reflections & Technical Growth

> *A journey through data, machine learning, climate science, and the pursuit of academic excellence (1990–2023).*

---

## 🌟 Overview

This document serves as a *“Behind the Scenes”* look at the **Global Compound Climate Risk Regimes** project. Beyond the code and the graphs, it reflects the depth of challenges encountered and the professional skills developed throughout the research journey. It captures not only technical execution, but also critical thinking, persistence, and scientific curiosity.

---

## 📊 Dataset Deep-Dive

Understanding the data was the most critical part of this research. I worked with multi-dimensional datasets to identify compound risks, ensuring both scientific accuracy and meaningful interpretation.

---

### 🗺️ ECMWF ERA5 Climate Reanalysis

From the ERA5 monthly surface-level datasets, we have taken 6 variables: **t2m, tcc, si10, tp, ssr, and avg_tprate**. Below is a refined analysis of the key variables:

---

### 🌡️ t2m (2-meter temperature)

It is used as the primary thermodynamic state variable to define compound climate risk. It is considered because human beings and all living beings mainly breathe in this region, it is used to track global warming trends, and most crops (like rice or wheat) exist within this 0–2 meter zone. Its unit is (K).

---

### 🌧️ tp (Total Precipitation)

tp indicates the total amount of water on the Earth's surface because some places have a tropical monsoon or long-lasting rainfall or snowfall. Somewhere in the world, tp is inversely related to t2m. It is highly important to calculate the moisture-deficit component (the amount of water required to bring back the soil moisture) of MCSI (Multivariate Climate State Index).

---

### ☁️ tcc (Total Cloud Coverage)

tcc has both daytime and nighttime effects.

* **In Daytime:** High tcc can reflect solar radiation to space and helps the surface become cooler (It is called the **Albedo effect**). Low tcc can increase the temperature.

* **In Nighttime:** The greenhouse gases try to leave the surface, but **high tcc** traps them on Earth. As a result, the temperature of the Earth is increasing, and the snows are melting, etc. With **low tcc**, the heat escapes from the Earth to space and the upper atmosphere. As a result, the temperature decreases very fast.

---

### ssr (Surface Solar Radiation)






What I have learned during this journey:

1. Monthly Climatology calculation($\mu_{m}$):: From 1990 to 2023, I calculated 12 months mean/year. Total mean = 12 * 33 = 486 number of means.
                       <img width="372" height="113" alt="image" src="https://github.com/user-attachments/assets/12877dfc-ab01-4a75-a100-6f7ca15e0ad5" />



2. Anommalies Calculation  ($x'_{t}$): to remove seasonal noise.


                          <img width="316" height="72" alt="image" src="https://github.com/user-attachments/assets/2d6a5d80-fbbe-4fb2-b297-283646fc8a9e" />

Anomalies of SSR:

<img width="535" height="429" alt="image" src="https://github.com/user-attachments/assets/bf8615a3-d3f8-4791-8902-4ca8ad50d425" />

**The Color LanguageRed Bands (Positive Z-scores)**: These years had significantly higher-than-average solar radiation. This usually indicates very clear skies and low cloud cover. Look at roughly 2022—it has a strong red stripe across almost the entire year.

**Blue Bands (Negative Z-scores)**: These represent "dimmer" years with high cloud cover or atmospheric aerosols.

**White/Pale Areas**: These are "Normal" months where the weather behaved exactly like the 34-year average.


The 2016 "Deep Blue" event represents a record-breaking negative anomaly with intense cloud cover likely linked to a strong El Niño phase. The 1992–1993 cluster reflects the atmospheric "dimming" and global cooling caused by the volcanic aerosols following the Mt. Pinatubo eruption.

<img width="533" height="468" alt="image" src="https://github.com/user-attachments/assets/0e088f1f-f8d1-4f47-8bef-05c99ff71349" />
Fig: Graph of tp
<img width="549" height="463" alt="image" src="https://github.com/user-attachments/assets/71265ba1-0968-42c7-af74-766c3135548e" />
Fig: Graph of ssr

<img width="533" height="462" alt="image" src="https://github.com/user-attachments/assets/c7d42cd1-8e84-4ea5-9494-ab3f6b37fdae" />
Fig: Graph of si10


Panel A: The Heatmap | Identification of Temporal Regimes
Purpose: This graph acts as a "Climate Fingerprint" for a specific location or region over the entire 1990–2023 period.

Function: It is used to visually detect the persistence and recurrence of risk. By stacking years against months, you can identify if a "regime" (like the 2016 blue stripe in image_d72070.png) was a short-lived event or a multi-month compound crisis.

Scientific Value: It proves that you have successfully removed the seasonal cycle, allowing the reviewer to see purely the interannual variability and long-term anomalies.




Panel B: The Line Plot | Quantification of Statistical Extremes
Purpose: This provides a High-Resolution Timeline of the most significant anomalies identified in Panel A.

Function: It is used to show the magnitude (Severity) of the Z-scores. While the heatmap shows "when," the line plot (like image_fd4238.png) shows "how much."

Scientific Value: This is the primary evidence for your PC1-Based MCSI. It illustrates the exact peaks (e.g., Z-scores exceeding +3 or -3) that drive the variance in your Principal Component Analysis, making it essential for the statistical "Predictability" part of your paper.




Panel C: The Spatial Map | Geographic Attribution of Risk
Purpose: This illustrates the Global Footprint of a specific regime at its peak intensity.

Function: It is used to move from a single point to a Global Scale. By plotting a map for a specific timestamp (e.g., January 2016), you can attribute the risk to specific geographical drivers, such as the warming of the Tropical Pacific.

Scientific Value: In a paper on Compound Risk, this map is used to show "Co-location." If you plot a map of Temperature and Precipitation anomalies side-by-side, you can visually demonstrate that the "Risk Regime" is hitting the same countries or agricultural zones simultaneously.



Before applying Unsupervised ML, we have to use Temporal Embedding to map months onto a circle using sine and cos functions.
Because Cos  is used to move the curve left/right along the X-axis.
        Sine is used to move the curve up/down along the Y-axis.

Why Temporal Embedding? Because after December, when it comes to January, it assumes a new start. But in the real world, December is very close to January.

Build 








## ✨ Closing Note

This dataset analysis forms the backbone of the research, connecting physical climate processes with data-driven insights. Each variable plays a crucial role in understanding compound climate risks, making the study both scientifically grounded and practically relevant.
