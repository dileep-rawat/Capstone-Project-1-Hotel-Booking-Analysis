# Capstone-Project-1-Hotel-Booking-Analysis

# Objective:
The Hotel Booking demand dataset (attached) contains booking information for a city hotel and a resort hotel. It includes information such as booking time, length of stay, number of adults, children/babies, number of available parking spaces, among other things.
            
We are provided with a hotel bookings dataset that contains booking information for a city hotel and a resort hotel. It includes information such as booking time, length of stay, number of adults, children/babies, number of available parking spaces, among other things. Our main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

# Dataset:
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.


# Tools and Libraries Used:
We have used Python 3 to its following packages:

- Pandas
- Numpy
- Matplotlib
- Seaborn
- Folium
- Plotly Express

# Data Cleaning and Feature Engineering:
(1) Removing Duplicate rows:
 - All duplicate rows were dropped.

(2) Handling null values:
 - Null values in columns `company`and `agent` were replaced by 0.
 - Null values in column `country` were replaced by `others`.
 
(3) Converting columns to appropriate data types:
  - Changed data type of `children`, `company`, `agent` to int type.

(4) Creating new columns:

- Created new column `total_stay` by adding `stays_in_weekend_nights`+`stays_in_week_nights`.
- Created new column `total_people` by adding `adults`+`children`+`babies`.

# **Exploratory Data Analysis:**

Exploratory Data Analysis is done on the below mentioned categories:-
- Univariate Analysis
- Hotel wise Analysis
- Distribution channel wise Analysis
- Booking cancellation Analysis
- Customer Centric Analysis

# Conculsion:

- City Hotel is most preferred by guests and thus city hotels has got maximum number of bookings. So from business perspective, we should target those months between May to Aug.
- In case of city hotel, months with high bookings (May, June, September, October) witnessed more cancellations. 
- Guest numbers for the Resort hotel go down slighty from June to September though variations in bookings and cancellations are less in case of resort hotel. 
- Both hotels have the fewest guests during the winter.
- Most of the bookings we have received from TA/TO and  the least booking we have received from Corporate.
- Since 98.7 % of the guests prefer No deposit type of stay.The high rate of cancellations can be due to high no deposit policies.
- Most common stay length is less than 4 days and generally people prefer city hotel for shorter stay, but for longer stay resort hotel is preferred.Resort hotel has slightly high avg lead time that means customers plan their trips very early.
- Resort hotel has higher retention rate compare to city hotel that means customers are willing to stay again in resort hotel but retention rate for city hotel 3.20% and for resort hotel is 5.03% which is very less.
Most preferred Room type is "A".
most preferred meal is BB(Bed & Breakfast) whike HB(Half-Board) and SC(Self Catering) are equally preferred.93.8 % guests did not required the parking space and only 6.2 % guests required only 1 parking space.

- City hotel has significantly longer waiting time then resort hotel, hence city Hotel is much busier than Resort Hotel.
Also,City hotels has slightly high avg lead time then resort hotel.Thus, city hotel makes slightly more revenue then resort hotel.
The City hotel has more guests during spring and autumn, when the prices are also highest, In July and August there are less visitors, although prices are lower. Thus, customers can get good deal on bookings in July and August in city hotel.

- Cancellations are high when done through agents compared to direct bookings. Hotels need to do marketing and give special incentives for direct bookings as these may establish personal one to one relationships promoting customer loyalty.

- Guest numbers for the Resort hotel go down slighty from June to September, which is also when the prices are highest. Thus, these months should be avoided for bookings.

- We have a huge number of visitors from western europe, namely Portugal, UK and France being the highest.We can instruct the marketing team to target people of this region.

- The highest Booking received by the hotels are through TA/OT so they are one of the most trusted booking provider.Also Direct booking count is greater than GDS system so still customer does not have complete faith over online booking platforms.


- The Average daily rate is more in Resort hotel than City Hotel. Prices in the Resort Hotel are much higher during the summer and prices of city hotel varies less and is most expensive during Spring and Autumn.

- Those who were not assigned same room as reserved does not affects adr.
From pie chart we can analyse that only 5.39% guest cancelled their reservation after assigning different rooms.

- 2016 seems to be year where hotel booking is at its highest and it seems summer period is a peak for hotel booking.Trend for the arrival day of month has been roller coaster.

- The majority of the stays are over the weekday's night so target should be given and on the other day  of the month it was random..


# Challenges Faced:

- There was a lot of duplicate data.
- Data was present in wrong datatype format.
- Choosing appropriate visualization techniques to use was difficult.
- A lot of null values were there in the dataset.


