# Aviation Accident Analysis

## Project Overview
This lab involved a comprehensive analysis of aviation accident data to advise an airline insurer on aircraft safety. The primary goal was to identify manufacturers and models that exhibit low rates of total destruction and minimal severe injury likelihood in the event of an accident [cite: Aviation_Accidents_Cleaning.ipynb].

## Phase 1: Data Cleaning and Preprocessing
The initial phase focused on transforming a raw dataset spanning 1948–2023 into a clean, analytical format.

### Key Cleaning Steps:
* **Temporal Filtering**: Data was restricted to 1983 onwards to comply with the client's 40-year maximum aircraft lifetime requirement [cite: Aviation_Accidents_Cleaning.ipynb].
* **Build Type Selection**: Filtered for 'Professional' builds only, excluding amateur-built aircraft to ensure relevance to commercial and passenger insurance [cite: Aviation_Accidents_Cleaning.ipynb].
* **Standardization**: The `Make` and `Model` columns were standardized (uppercase, trimmed) to resolve inconsistencies in manufacturer naming conventions [cite: Aviation_Accidents_Cleaning.ipynb].
* **Statistical Thresholding**: Manufacturers with fewer than 50 recorded incidents were excluded to ensure that the mean safety metrics were statistically robust [cite: Aviation_Accidents_Cleaning.ipynb].

### Feature Engineering:
* **Severe Injury Rate**: A derived column calculating the fraction of passengers suffering fatal or serious injuries relative to total passengers on board [cite: Aviation_Accidents_Cleaning.ipynb].
* **Destruction Binary**: A boolean indicator identifying whether the aircraft was 'Destroyed' versus damaged or minor, facilitating a precise 'destruction rate' calculation [cite: Aviation_Accidents_Cleaning.ipynb].

## Phase 2: Exploratory Data Analysis (EDA)
The analysis was segmented by aircraft capacity, using a threshold of 20 passengers to distinguish between small and large models [cite: Aviation_Accidents_Data_Analysis.ipynb].

### Findings on Manufacturers:
* **Large Aircraft**: Industry leaders like Boeing and Airbus showed consistently low injury rates. Strip plots revealed that while accidents are rare, they are heavily skewed toward zero injuries, demonstrating high airframe survivability [cite: Aviation_Accidents_Data_Analysis.ipynb].
* **Small Aircraft**: Manufacturers like Cessna and Piper emerged as the safest in the small-scale category. Violin plots indicated a higher variability in outcomes compared to large jets, with a slight bimodal distribution [cite: Aviation_Accidents_Data_Analysis.ipynb].

### Factor Analysis:
* **Weather Conditions**: Analysis showed that accidents in IMC (Instrument Meteorological Conditions) lead to significantly higher rates of aircraft destruction and severe injuries compared to VMC (Visual Meteorological Conditions) [cite: Aviation_Accidents_Data_Analysis.ipynb].
* **Phase of Flight**: High-altitude and high-speed phases (Cruise, Maneuvering) were identified as high-risk, while high-frequency phases (Takeoff, Landing) resulted in more incidents but lower severity [cite: Aviation_Accidents_Data_Analysis.ipynb].

## Conclusion and Recommendations
By meticulously cleaning the data and applying strict sample size filters, this lab produced a set of recommendations based on empirical safety evidence. The process demonstrated the importance of segmenting data by operational context (Small vs. Large) and the significant impact of environmental factors (Weather) on insurance risk assessment [cite: Aviation_Accidents_Data_Analysis.ipynb].

