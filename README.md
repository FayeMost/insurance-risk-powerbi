# Insurance Risk & Premium Analysis

Power BI dashboard analyzing premium drivers across an insurance policyholder dataset — built to identify which factors most influence customer premiums and risk classification.

## Business Problem
Insurance underwriters need to understand which customer attributes most strongly predict premium cost and risk level, in order to price policies accurately and flag high-risk segments.

## Key Insight
Smoking status is the dominant premium driver in this dataset: smokers pay an average of **$32.05K** annually vs. **$8.43K** for non-smokers — a **3.80x** ratio. The scatter plot shows premiums jump sharply once BMI crosses ~30 for smokers, while non-smoker premiums stay flat and low regardless of BMI.

## Dataset
Medical Insurance Costs dataset (Kaggle), 1,338 policyholder records: age, sex, BMI, children, smoker status, region, and annual charges.

## Tools
Power BI (Power Query, DAX), published via Power BI Service.

## What I Built
- Custom Power Query transformations, including a Risk_Tier column (High/Medium/Low based on smoker status and BMI)
- KPI cards: Avg_Premium, Total_Policies, High_Risk_Count
- Bar chart: average premium by region (southeast highest, southwest lowest)
- Scatter plot: BMI vs. annual premium, colored by smoker status, with row-level detail via an Index field
- Slicers: region, smoker, sex, with cross-filtering enabled between visuals
- DAX comparative measures: Smoker_Avg_Premium, NonSmoker_Avg_Premium, Premium_Ratio

## Dashboard

**Full view** — all 1,338 policies, avg premium by region, and the smoker vs. non-smoker DAX comparison ($32.05K vs. $8.43K, 3.80x ratio):

![Full dashboard overview](./Insurance%20Risk%203.png)

**Smoker slicer applied** — isolating smokers shows the BMI/premium relationship clearly: costs stay moderate until BMI ~30, then jump sharply:

![Smoker-filtered scatter and regional comparison](./Insurance%20Risk%202.png)

**Region slicer applied** — filtering to Southwest cross-filters every visual, including the KPI cards (325 policies, 58 high-risk):

![Region-filtered view (Southwest)](./Insurance%20Risk%201.png)
