# East Asia Real Exchange Rate Cointegration Analysis

**Author:** Ching-Ting Huang (Collaborated with 4 team members)  

**Course:** ECON90010 Quantitative Analysis of Finance II, University of Melbourne

## 📌 Project Overview
This project investigates the validity of the **Generalized Purchasing Power Parity (G-PPP)** hypothesis across East Asian economies (Mainland China, Hong Kong SAR, and Japan) relative to the United States. 

[cite_start]Using monthly macroeconomic data from **2015 to 2024**, we analyze whether these economies form an "Optimum Currency Area" and whether their Real Exchange Rates (RER) share a stable long-run equilibrium[cite: 14, 15]. [cite_start]The study also extends previous work by Liang (1999) to determine if modern RER movements are driven by internal macroeconomic fundamentals rather than regional parity[cite: 16, 17].

## 📊 Research Questions
1. [cite_start]**Regional Integration:** Do China, Hong Kong, and Japan share a long-run cointegration relationship with the US Dollar, supporting the G-PPP hypothesis? [cite: 15]
2. [cite_start]**Internal Drivers:** If regional parity does not hold, are RER movements anchored by domestic fundamentals like GDP per capita, Foreign Reserves, and Real Interest Rates? [cite: 27]

## 🛠 Methodology
The analysis is conducted in **R** using a rigorous time-series econometric framework:

### 1. Data Preprocessing
* **Time Period:** 2015–2024 (Post-Asian Financial Crisis and post-RMB internationalization).
* [cite_start]**Interpolation:** Annual data (e.g., GDP per capita) was converted to monthly frequency using the **Denton-Cholette interpolation** method[cite: 44].

### 2. Statistical Tests
* [cite_start]**Unit Root Testing:** Augmented Dickey-Fuller (ADF) and Phillips-Perron (PP) tests were used to confirm non-stationarity (I(1)) for RER and fundamental variables[cite: 21].
* [cite_start]**Cointegration Analysis:** The **Johansen Cointegration Test** (Trace and Max-Eigenvalue statistics) was applied to detect long-run equilibrium vectors[cite: 23, 24].
* [cite_start]**Lag Selection:** Optimal lag lengths determined via the Akaike Information Criterion (AIC)[cite: 25].

## 📉 Key Findings
Our empirical results offer a significant update to historical literature (Liang, 1999):

* **Rejection of G-PPP:** We found **no evidence of cointegration** across the RERs of China, Hong Kong, and Japan. [cite_start]This suggests that East Asian markets are less monetarily integrated than in the pre-1999 era, likely due to divergent exchange rate regimes (e.g., China's shift to a managed float)[cite: 96, 101].
* **Strong Domestic Anchors:** While regional integration is weak, we found **robust cointegration within individual countries**. 
    * [cite_start]**Hong Kong & Japan:** 1 cointegrating vector found between RER and domestic fundamentals[cite: 107, 110].
    * [cite_start]**China:** 2 cointegrating vectors found[cite: 109].
* [cite_start]**Economic Implication:** Exchange rates in East Asia are currently driven by internal factors—specifically productivity growth (Balassa-Samuelson effect), foreign reserve accumulation policies, and real interest rate differentials[cite: 112, 115, 116].

## 📂 Repository Structure
* `East_Asia_RER_Cointegration_Analysis.Rmd`: The main R Markdown file containing the full econometric code and analysis.
* `Appendix_Interpolation.Rmd`: Supplementary code for converting annual macro data to monthly frequency.
* [cite_start]`data.xlsx` / `annual_data.xlsx`: Raw and processed datasets sourced from IMF, World Bank, and Federal Reserve[cite: 35, 38].
* `final report_revision.pdf`: The formal academic report detailing the theoretical framework and literature review.

## 📦 Libraries Used
* `urca`: For Unit Root and Cointegration tests.
* `vars`: For Vector Autoregression and VECM estimation.
* `tseries`: For additional time-series diagnostics.
* `tidyverse`: For data manipulation and visualization.

---
*This project was completed as part of the Master of Applied Econometrics curriculum.*
