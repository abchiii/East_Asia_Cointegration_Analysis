# East Asia Real Exchange Rate Cointegration Analysis

**Author:** Ching-Ting Huang (Collaborated with 4 team members)  

**Course:** ECON90010 Quantitative Analysis of Finance II, University of Melbourne

## 📌 Project Overview
This project investigates the validity of the **Generalised Purchasing Power Parity (G-PPP)** hypothesis across East Asian economies (Mainland China, Hong Kong SAR, and Japan) relative to the United States. 

Using monthly macroeconomic data from **2004 to 2024**, we analyse whether these economies form an "Optimum Currency Area" and whether their Real Exchange Rates (RER) share a stable long-run equilibrium. The study also extends previous work by Liang (1999) to determine if modern RER movements are driven by internal macroeconomic fundamentals rather than regional parity.

## 📊 Research Questions
1. **Regional Integration:** Do China, Hong Kong, and Japan share a long-run cointegration relationship with the US Dollar, supporting the G-PPP hypothesis?
2. **Internal Drivers:** If regional parity does not hold, are RER movements anchored by domestic fundamentals like GDP per capita, Foreign Reserves, and Real Interest Rates?

## 🛠 Methodology
The analysis is conducted in **R** using a rigorous time-series econometric framework:

### 1. Data Preprocessing
* **Time Period:** 2004–2024 (Post-Asian Financial Crisis and post-RMB internationalisation).
* **Interpolation:** Annual data (e.g., GDP per capita) was converted to monthly frequency using the **Denton-Cholette interpolation** method.

### 2. Statistical Tests
* **Unit Root Testing:** Augmented Dickey-Fuller (ADF) and Phillips-Perron (PP) tests were used to confirm non-stationarity (I(1)) for RER and fundamental variables.
* **Cointegration Analysis:** The **Johansen Cointegration Test** (Trace and Max-Eigenvalue statistics) was applied to detect long-run equilibrium vectors.
* **Lag Selection:** Optimal lag lengths determined via the Akaike Information Criterion (AIC).

## 📉 Key Findings
Our empirical results offer a significant update to historical literature (Liang, 1999):

* **Rejection of G-PPP:** We found **no evidence of cointegration** across the RERs of China, Hong Kong, and Japan. This suggests that East Asian markets are less monetarily integrated than in the pre-1999 era, likely due to divergent exchange rate regimes (e.g., China's shift to a managed float).
* **Strong Domestic Anchors:** While regional integration is weak, we found **robust cointegration within individual countries**. 
    * **Hong Kong & Japan:** 1 cointegrating vector found between RER and domestic fundamentals.
    * **China:** 2 cointegrating vectors found.
* **Economic Implication:** Exchange rates in East Asia are currently driven by internal factors—specifically productivity growth (Balassa-Samuelson effect), foreign reserve accumulation policies, and real interest rate differentials.

## 📂 Repository Structure
* `East_Asia_RER_Cointegration_Analysis.Rmd`: The main R Markdown file containing the full econometric code and analysis.
* `Appendix_Interpolation.Rmd`: Supplementary code for converting annual macro data to monthly frequency.
* `data/`: Folder containing raw and processed datasets (e.g., `data.xlsx`, `annual_data.xlsx`).
* `East_Asia_RER_Cointegration_Analysis.pdf`: The formal academic report detailing the theoretical framework and literature review.

## 📦 Libraries Used
* **Econometric Analysis:** `urca` (Cointegration/Unit Root), `vars` (VAR/VECM), `tempdisagg` (Denton-Cholette interpolation).
* **Time Series & Data Handling:** `tsbox`, `dplyr`, `readxl`, `writexl`.
* **Reporting:** `flextable`, `knitr`, `officer`.

---
*This project was completed as part of the Master of Applied Econometrics curriculum.*
