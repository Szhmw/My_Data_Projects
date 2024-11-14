# Gemini Hotel Group Revenue and Trend Analysis from 2018 to 2020
Gemini Hotel Group operates two hotel types: city and resort. The Director of Development aims to understand past sales performance and identify trends in customer behavior. To address this, a Power BI dashboard was developed to monitor key performance indicators (KPIs).

## Requirements Gathered From the Stakeholders:

1. **Revenue Growth:** Is our hotel revenue increasing year-over-year?
2. **Parking Capacity:** Should we expand our parking facilities?
3. **Data Trend:** What trends are evident in the data?

## Data Structure & Initial Checks

- Data from 2018 to 2020 (note: 2020 data is incomplete). 
- `Discount` column is located in the `market_segment` table.
- **Revenue** calculation requires considering discounts.
- **Hotel type** is identified by the `hotel` in the dataset.
- **Parking Needs** are assessed using the `required_car_parking_spaces` column.

### Dashboard Visualization:

![Alt text](https://github.com/Szhmw/My_Data_Projects/blob/8095efad837e57576ce392c5deddfcff66300482/Gemini%20Hotel/hotel_dash.jpg)


### Key Metrics and Dimensions:

- **Total Revenue:** Calculated using total stay nights, average daily rate (ADR), and discounts.
- **Total Nights:** Combined both weekend and weekday nights.
- **Parking Percentage:** Percentage of required parking spaces utilized relative to total nights booked.


### Findings:

- **Revenue Growth:** Total revenue has increased from 2018 to 2020, with a slight fluctuation in 2020 likely due to COVID-19 impacts.
- **Revenue and Hotel Types:** Both hotel type contributes almost equally to the total revenue.
- **Parking Utilization:** Parking needs generally remain below 5%.
- **Discount Trends:** Customers consistently receive an average discount of 25.8% across various booking channels.

### Recommendations:

- **Parking Capacity:** Based on historical data, there's no immediate need to expand parking facilities. However, future customer behavior changes may necessitate a reevaluation.
- **Location and Hotel Type:** Location and hotel type significantly influence parking requirements. For example, US resort hotel guests exhibit higher parking needs.

### Additional Considerations:

- **Data Completeness:** Address the missing 2020 data to obtain a more accurate picture of recent trends.
- **Customer Segmentation:** Deeper analysis of customer segments (e.g., business, leisure) can provide valuable insights into parking and other preferences.
- **External Factors:** Consider the impact of external factors like economic conditions and travel trends on future demand.

### SQL Code Used to Combined Datasets and Query Data: 
```sql
with hotels as (
select * from dbo.['2018$']
union
select * from dbo.['2019$']
union
select * from dbo.['2020$'])

select * from hotels
left join dbo.market_segment$
on hotels.market_segment = dbo.market_segment$.market_segment
left join meal_cost$
on hotels.meal = meal_cost$.meal
```
