# Hotel-Booking-Analysis

This repository provides a complete pipeline for hotel booking analytics and network optimization. It covers robust data preparation, exploratory analysis, feature engineering, and predictive modeling designed to support geographic expansion, rate negotiation, and inventory risk management.

### Project Overview
A workforce lodging provider faces challenges in aligning hotel supply with client demand while maintaining competitive negotiated rates. The project analyzes 119,000+ booking records to identify geographic coverage gaps, audit corporate rate competitiveness against public markets, and predict cancellation risks to minimize revenue leakage.

### Data Preparation & Cleaning
* Converted and parsed arrival dates into proper time-series objects
* Calculated total stay duration and total guest counts to filter invalid records
* Checked for and removed outliers in Average Daily Rate (ADR) (e.g., negative rates or extreme values)
* Handled missing values in agent, company, and country columns
* Performed descriptive statistics and initial profiling to validate data integrity

### Exploratory Data Analysis (EDA)
* Analyzed correlations between cancellations and factors like lead time, special requests, and room type
* Visualized seasonality to identify peak pricing months where negotiated rate leverage is critical
* Benchmarked "Corporate" vs. "Online TA" rates to audit discount effectiveness
* Explored geographic distributions to identify high-value (High ADR) but under-served markets

### Feature Engineering & Modeling
* Addressed categorical complexity by encoding market segments and distribution channels
* Engineered business metrics including `Revenue_at_Risk`, `Lead_Time_Category`, and `Seasonality_Index`
* Built a predictive classification model using Random Forest to score cancellation probability
* Evaluated feature importance, identifying "Lead Time" and "Deposit Type" as primary risk drivers

### Strategic Analysis & Risk Prediction
* Decomposed booking behaviors to isolate "Unmet Demand" in specific global regions
* Modeled the financial impact of cancellations, quantifying potential revenue leakage per market segment
* Generated actionable "Hit Lists" for the supply team: properties requiring renegotiation and regions requiring urgent expansion

### Key Insights
* **Negotiation:** Corporate rates currently offer a ~10-15% discount, but this spread significantly narrows in July/August, signaling a need for fixed-rate caps during peak season
* **Coverage:** High-value demand exists in specific European markets (e.g., Portugal, UK) that are currently under-supplied relative to their booking volume
* **Risk:** Cancellations are strongly correlated with Lead Time; bookings made >90 days in advance have a 2x higher risk, necessitating stricter deposit policies for long-lead reservations
* **Revenue:** Approximately 37% of potential revenue is at risk due to cancellations, primarily from the "Online TA" segment

### Conclusion
This project demonstrates end-to-end data science skills: from cleansing, EDA, feature engineering to strategic auditing and predictive risk modeling—providing actionable insights for workforce lodging network optimization.
