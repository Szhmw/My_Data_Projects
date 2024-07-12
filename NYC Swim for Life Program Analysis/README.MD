
# NYC Swim for Life Program Analysis

A dashboard to monitor Swim for Life program offered in New York City and a data story to advocate for affordable swimming education. Interactive Tableau dashboard can be found [here](https://public.tableau.com/shared/6GR6ZR3MQ?:display_count=n&:origin=viz_share_link).

![Alt text](https://github.com/Szhmw/My_Data_Projects/blob/6da5034f8a3292cacf5716a4fe6dc5268cf03688/NYC%20Swim%20for%20Life%20Program%20Analysis/dashboard.png)

### Key Metrics and Dimensions:
#
- **Number of Sessions Attended:** How many sessions a student completed.
- **Attended or Not:** If the session is attended or not.
### Conclusions:
---

- Attendance: Close to 16,000 students enrolled in the program. On average 91% of them attended at least one session. 

- Gender comparison: The total signup numbers, total sessions attendance, and attendance rates are pretty balanced among genders.

- Borough comparison: Although there are more training sites in Manhattan, students attended more sessions at the training sites in Queens. 
To improve attendance, it's worth investigating factors like pool facilities and staff training across different training sites.

It could also indicate a gap among students in different boroughs in terms of swimming ability. This disparity could be due to socioeconomic factors. Students and parents with fewer resources might be more motivated to participate in the program to bridge learning gaps.

- Pool use: Swim for Life takes place mostly in public park pools along with a few other partners. There's only a small portion of public pools that are available in the progrom. Might consider expanding the program to include more public pools and offering weekend classes could increase accessibility.

### Future Research ideas:

- Get more info about attendees' pre and post program swimming ability comparison to better measure the quality of the program.

- According to NYC Youth Risk Behavior Survey from 2017, there's a huge gap in race when it comes to swimming ability. The report should include more details on race.

#### The Data

The data was downloaded from NYC OpenData

- `instacart_orders.csv`: each row corresponds to one order on the Instacart app
    - `'order_id'`: ID number that uniquely identifies each order
    - `'user_id'`: ID number that uniquely identifies each customer account
    - `'order_number'`: the number of times this customer has placed an order
    - `'order_dow'`: day of the week that the order placed (which day is 0 is uncertain)
    - `'order_hour_of_day'`: hour of the day that the order was placed
    - `'days_since_prior_order'`: number of days since this customer placed their previous order
- `products.csv`: each row corresponds to a unique product that customers can buy
    - `'product_id'`: ID number that uniquely identifies each product
    - `'product_name'`: name of the product
    - `'aisle_id'`: ID number that uniquely identifies each grocery aisle category
    - `'department_id'`: ID number that uniquely identifies each grocery department category
- `order_products.csv`: each row corresponds to one item placed in an order
    - `'order_id'`: ID number that uniquely identifies each order
    - `'product_id'`: ID number that uniquely identifies each product
    - `'add_to_cart_order'`: the sequential order in which each item was placed in the cart
    - `'reordered'`: 0 if the customer has never ordered this product before, 1 if they have
- `aisles.csv`
    - `'aisle_id'`: ID number that uniquely identifies each grocery aisle category
    - `'aisle'`: name of the aisle
- `departments.csv`
    - `'department_id'`: ID number that uniquely identifies each grocery department category
    - `'department'`: name of the department

The data is provided by TripleTen, who took it from Kaggle and modified it.

#### The Process

I first explored the dataset to find and fix missing and duplicate values, and I merged DataFrames from different sources. Finally, I analyzed the data using visualizations and pivot tables.

### Results

Taking the time to explain my results at each step was a key element in this process, and this was my first attempt at doing it. I wrote an introduction and conclusion that outlined what I did, and made suggestions for Instacart to consider in the future.

Please have a look at the Jupyter Notebook included for a full description of results.
