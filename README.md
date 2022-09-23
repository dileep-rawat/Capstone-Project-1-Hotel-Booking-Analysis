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
- Pycountry

# Data Cleaning and Feature Engineering:
(1) Removing Duplicate rows
 - All duplicate rows were dropped.

(2) Handling null values
 - Null values in columns "company" and 'agent' were replaced by 0.
 - Null values in column 'country' were replaced by 'others'.
 - Null values in column children were replaced by the mean of the column.
 
(3) Converting columns to appropriate data types
  - Changed data type of children, company, agent to int type.
  - Changed data type of reservation_status_date to date type.

(4) Creating new columns

- Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
- Created new column total_people by adding adults+children+babies.

# **Exploratory Data Analysis:**

