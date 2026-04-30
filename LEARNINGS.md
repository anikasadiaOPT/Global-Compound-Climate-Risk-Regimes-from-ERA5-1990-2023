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

+<img width="535" height="429" alt="image" src="https://github.com/user-attachments/assets/bf8615a3-d3f8-4791-8902-4ca8ad50d425" />

**The Color LanguageRed Bands (Positive Z-scores)**: These years had significantly higher-than-average solar radiation. This usually indicates very clear skies and low cloud cover. Look at roughly 2022—it has a strong red stripe across almost the entire year.

**Blue Bands (Negative Z-scores)**: These represent "dimmer" years with high cloud cover or atmospheric aerosols.

*White/Pale Areas**: These are "Normal" months where the weather behaved exactly like the 34-year average.


The 2016 "Deep Blue" event represents a record-breaking negative anomaly with intense cloud cover likely linked to a strong El Niño phase. The 1992–1993 cluster reflects the atmospheric "dimming" and global cooling caused by the volcanic aerosols following the Mt. Pinatubo eruption.

## ✨ Closing Note

This dataset analysis forms the backbone of the research, connecting physical climate processes with data-driven insights. Each variable plays a crucial role in understanding compound climate risks, making the study both scientifically grounded and practically relevant.
