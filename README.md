# Marketing-Analytics-Project

# Social Media Marketing Channel Performance Analysis

## Business Problem
A company wants to know which social media advertising channel
delivers the best return on investment (ROI), to guide budget
allocation decisions for future marketing campaigns.

## Dataset
- Source: Kaggle - Social Media Advertising Dataset
- ~300,000 rows covering campaigns across Instagram, Facebook,
Twitter, and Pinterest
- Columns include: Channel, Clicks, Impressions, Conversion Rate,
Acquisition Cost, ROI, Customer Segment, Campaign Goal

## Tools Used
- SQL (PostgreSQL) - data aggregation and analysis
- Excel - visualization and dashboard

## Key Findings <img width="1570" height="917" alt="image" src="https://github.com/user-attachments/assets/ea5d72f6-dc2d-4077-b1e2-d12f0ad8ccd6" />

- Pinterest campaigns show a dramatically lower average ROI (~0.72)
compared to Facebook, Twitter, and Instagram (all averaging ~4.0)
- Conversion rate is nearly flat across all campaign goals
(0.0799-0.0802), suggesting campaign goal has little effect on
conversion rate in this dataset
- Average ROI is also fairly consistent across customer segments
(3.16-3.19), with Technology and Health performing slightly better

## Recommendation
Channel choice is the strongest lever for improving ROI.
Reallocating budget away from Pinterest toward Facebook, Twitter,
or Instagram could meaningfully improve overall campaign returns,
while further segmenting by campaign goal or customer type shows
comparatively little impact.

## Sample SQL Query
SELECT channel_used, AVG(roi)
FROM social_media_advertising
GROUP BY channel_used
ORDER BY AVG(roi) DESC;
