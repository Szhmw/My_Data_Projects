## Data Structure & Initial Checks

- Data from 2018 to 2020 (note: 2020 data is incomplete). 
- `Discount` column is located in the `market_segment` table.
- **Revenue** calculation requires considering discounts.
- **Hotel type** is identified by the `hotel` in the dataset.
- **Parking Needs** are assessed using the `required_car_parking_spaces` column.

### Key Metrics and Dimensions:

- **Total Revenue:** Calculated using total stay nights, average daily rate (ADR), and discounts.
- **Total Nights:** Combined both weekend and weekday nights.
- **Parking Percentage:** Percentage of required parking spaces utilized relative to total nights booked.

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
