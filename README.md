# Stochastic-Decision-Model-for-Hotel-Reservations

**About Project**

This project is about developing a decision model for Hotel Paradise to optimize occupancy and profits during peak season while maintaining guest satisfaction. The model supports the sales manager in making informed decisions on pricing, managing reservations, and minimizing risks through scenario analysis and simulations.

**About Model**

The decision model allows the hotel sales manager to manage reservations efficiently, aiming to maximize daily profits and occupancy. It enables input for reservations, walk-ins, cancellations, and miscellaneous costs. The model outputs daily profit figures, whether the hotel is sold out, and the number of available rooms out of 250. It also shows room availability based on the chosen overbooking rate for real-time decision-making. The manager can set room prices, select cancellation rates, and adjust the overbooking rate to optimize outcomes.

**Conceptual Model**

<img width="856" alt="Screenshot 2024-10-14 at 12 09 20 PM" src="https://github.com/user-attachments/assets/10d5922f-b038-42d0-bcd2-456975d5ee16">

- Stochastic Inputs –  Daily Reservations , Walk ins, Late cancellations.
- Fixed inputs – Number of Rooms (250 fixed capacity), Housekeeping costs $7500 per day.
- Decision Variables – Room rate, Late cancellation fee, Overbooking rate.
- Calculated Variables – Number of Rooms occupied, Total Sales Revenue per day, Total cost per day, Total overbooked rooms, Total overbooked compensation,
- Output Variables – Daily profit, Sold out (Yes/No), Total number of rooms available, Overbooking limit available.

**Assumptions**

- Demand is higher at the $230 price point, and it varies only with room price, not with cancellations or miscellaneous expenses.
- A non-refundable late cancellation fee of 100% is charged upfront.
- Overbooking compensation equals one night’s room price, and walk-ins are accepted within overbooking limits to manage risks.
- The manager typically uses a 255 overbook rate and a $230 cancellation fee.

**Spreadsheet based Decision Model**

<img width="1141" alt="Screenshot 2024-10-14 at 12 13 29 PM" src="https://github.com/user-attachments/assets/8f30d927-8d34-44f3-bfd9-24dc2c927f9a">

- The data is shown here for the base case of $230 room price.
- The stochastic inputs have been modelled with the most suitable probability distribution.
- The room price can be selected with a dropdown selection for either $215, $230.
- The overbooking rate and Late cancellation fee can also be adjusted accordingly.
- The manager can edit the Stochastic inputs as needed to see changes in Calculated variables and Outputs.

**Scenario Analysis**

The following scenario analysis was done to identify the best case, base case and worst case for the hotel. The scenario's presented here are when the other stochastic inputs are at base case for the given price. 

Many other scenarios were done, I am only presenting a few here considering space. 

Reservations when price $230 

<img width="594" alt="Screenshot 2024-10-14 at 12 16 49 PM" src="https://github.com/user-attachments/assets/c16edbdd-833b-4ca1-8710-e8f107e5944f">

Reservations when price $215

<img width="597" alt="Screenshot 2024-10-14 at 12 18 22 PM" src="https://github.com/user-attachments/assets/ec66d4e5-e53c-4eac-8687-01d649cc88ad">

Walk ins when price $230 

<img width="598" alt="Screenshot 2024-10-14 at 12 19 29 PM" src="https://github.com/user-attachments/assets/c78adc81-2eb0-4308-885f-7c51755ac3a1">

Walk ins when price is $215

<img width="594" alt="Screenshot 2024-10-14 at 12 19 53 PM" src="https://github.com/user-attachments/assets/eebda50e-75a3-4544-828a-6fba3ae76d33">

- At $230 , when the worst case of 150 reservations will result in a -$13800.00 loss where as when $215 the worst case of 190 reservations will result in -$6525.00 loss.
- At $230 the best case of 250 reservations will result in a $6900 profit where as at $215 the best case of 235 reservations will result in only $3150.00 profit.
- At $230 , when the worst case of 10 walk ins will result in a -$3450.00 loss where as when $215 the worst case of 20 reservations will result in -$2225.00 loss.
- At $230 the best case of 80 walk ins will result in a $3450.00 profit where as at $215 the best case of 90 walk ins will result in $3150.00 profit.

**Simulation output distribution and risk analysis**

1000 simulation trials was done for the four stochastic variables. 

Since this model was developed without any past data, the challange was to understand the appropriate probability distribution for our stochastic variables to model the uncertainty. Therefore, first the most suitable probability distributions were selected as illustrated below. 

<img width="1151" alt="Screenshot 2024-10-14 at 12 34 45 PM" src="https://github.com/user-attachments/assets/c69460f0-292d-4436-9bd1-4595716a4b01">

Once the probability distributions were selected, random numbers were used along with the suitable distribution type.

The stochastic data created with random numbers are visualized below. (When price $230). 

<img width="547" alt="Screenshot 2024-10-14 at 12 39 39 PM" src="https://github.com/user-attachments/assets/2f437b29-34fc-43ef-9abb-f2f3b29576da">
<br>
<img width="600" alt="Screenshot 2024-10-14 at 12 40 12 PM" src="https://github.com/user-attachments/assets/ed260bff-6a6d-46ef-a42b-c72e7c0b8671">
<br>
<img width="600" alt="Screenshot 2024-10-14 at 12 40 36 PM" src="https://github.com/user-attachments/assets/1683e82b-6d5e-4a53-b705-fb4b09a2c436">
<br>

**Simulation Trials**

- A sample of the simulation trials pages for prices $230 and $215 are illustrated below.
- Further, convergence tracking is also done to identify how the output values will stabilze over the course of the trials.

**Convergence of room occupancy and profits at both prices**

<img width="500" alt="Screenshot 2024-10-14 at 1 01 57 PM" src="https://github.com/user-attachments/assets/e94174b9-f29d-4e94-acd8-68f8952c8e69">

<img width="504" alt="Screenshot 2024-10-14 at 1 03 35 PM" src="https://github.com/user-attachments/assets/54a2c05e-1367-4e76-9eb2-dd34f8080dd0">

<img width="500" alt="Screenshot 2024-10-14 at 1 04 15 PM" src="https://github.com/user-attachments/assets/f59fe16d-8be4-48a0-bfe0-72df0cf3c02d">

<img width="502" alt="Screenshot 2024-10-14 at 1 02 16 PM" src="https://github.com/user-attachments/assets/f1558251-8ec2-480f-9715-d4f5a0ac20b9">



**Room price over 1000 trials**
<img width="1393" alt="Screenshot 2024-10-14 at 12 45 55 PM" src="https://github.com/user-attachments/assets/8678a2bf-536e-4405-90a4-c0b516e8724d">
<img width="1342" alt="Screenshot 2024-10-14 at 12 58 34 PM" src="https://github.com/user-attachments/assets/3ddd606d-f710-4f64-b507-279c1c7a7d49">


**Risk profile and interpretation at room price $230 and $215**

<img width="699" alt="Screenshot 2024-10-14 at 1 08 29 PM" src="https://github.com/user-attachments/assets/cc32174e-01d8-4c0d-96e7-c300085b9181">


- When price is $230 there is a 32.70% probability of the daily profits being $7200, 25.20% probability of profits being $4100 and 13.70% probability of profits of $10300.
- There is a 0.1% chance of the hotel facing the highest loss at $17579.67 when room price is set to $230. 
- There is 1.3% chance that the hotel will make the highest profit is $13389.91 when room price is set to $230

<img width="698" alt="Screenshot 2024-10-14 at 1 08 47 PM" src="https://github.com/user-attachments/assets/de9d3ddc-0618-4a3f-b4a7-9080cb12541d">

- The distribution is skewed to the left.
- When price is $215 there is a 30.10% probability of the daily profits being $7280, 28.2% probability of profits being $4320 and 12.9% probability of profits of $10240.
- At this price, the hotel has over 73.2% chance of making a daily profit over $4000 and over 87.5% chance of not making a loss. 
The highest possible loss at this price is $16413.79 and highest profit is $13175.95

<img width="1235" alt="Screenshot 2024-10-14 at 12 54 37 PM" src="https://github.com/user-attachments/assets/dd4900ed-9da2-4c59-a43d-903440c68fb8">

<img width="1234" alt="Screenshot 2024-10-14 at 12 55 28 PM" src="https://github.com/user-attachments/assets/742432ee-9895-4aef-815e-c03e79d39ee4">

- There is a 22.2% chance of making a loss when the room price of the room is set at $230. While there is a chance (8.4%) of making a loss of greater than $5000, it is much more likely (13.8%) that the loss will be contained under $5000.
- The chance of making a loss decreases to 18.1%% when the room price is set at $215, and similarly the highest probability of loss is around 0 to $5000 range.
- The lower room price is also more likely to deliver a profit over $10000 (2.2% vs. 1.7%). Further, room price at $215 has a higher chance (45.5% vs 40.5%) of delivering profits between 0 to $5000. Both prices have roughly same chance of profits between $5000 to $10000.
- If the room price is set at $230 then reservations would need to exceed 250 to avoid making a loss. Similarly, if room price is set to $215 reservations would need to exceed 250 to avoid making a loss.  If the room price is set at $230 then walk ins would need to exceed 70 to avoid making a loss. Similarly,
- if room price is set to $215 walk ins would need to exceed 60 to avoid making a loss.

**Conclusion and Recommendations**

- The lower room price at $215 has less risk of causing a loss, than the room price at $230.
- The room price of $215 has a higher chance (2.2%) of delivring higher profits (over $10 000) than the $230 room price. (1.7% chance of profits over $10 000).
- At both price points, the hotel will need similar number of reservations and walk ins to generate similar profit levels. (Above 250 reservations and 60 walk ins to avoid loss and above).
- Therefore, considering lower risk and higher chance of increased profits, it is advisable that the hotel manager set the room price at $215.
- Further, it is advised to have a higher overbook rate to reduce posed by risk of cancellations.
- It is recommended to keep both reservations above 250 and walk ins above 60 through marketing efforts. 





