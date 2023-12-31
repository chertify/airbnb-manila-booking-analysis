**AIRBNB PROFIT IN MANILA PRE AND POST COVID, 2019-2023**

![alt text](https://github.com/chertify/airbnb-manila-booking-analysis/blob/main/images/airbnb-cover.png?raw=true)

Dataset Source: df_raw.xlsx<br/>
Dataset Output: df_cmpt.xlsx<br/>
Python: Short_Term_Stays(Data_Manipulation).ipynb

Tableau Public:
"Airbnb Profit in Manila Pre and Post COVID, 2019-2023"
https://public.tableau.com/app/profile/chertify/viz/AirbnbProfitinManilaPreandPostCOVID192019-2023/Dashboard5

---

**INTRODUCTION**

Airbnb is popular for providing short-term stays to guests across the globe. A simple search on their app can bring you to a number of options that displays the photos of the room, facilities it provides, the pricing and minimum stay.

The dataset we will be exploring and analyzing dates from November 2019 to January 2023 provided by a Superhost at Airbnb located in Manila. It is a Studio type of condo near Intramuros, de La Salle University-Manila, Rizal Park, Star City, CCP, and other nearby tourist attractions.

The goal of this data is to understand the earning performance and historical data of a Studio condo in Manila from the aforementioned date in the middle of a COVID-19 pandemic.

**CHALLENGES AND EXPECTATIONS**

- As Airbnb does not indicate the Confirmation Code to which the payout belongs to, there's no way to find out directly how much was received from a particular booking. Part of our data preprocessing includes identifying the total amount received of a particular booking (after resolution adjustment or resolution payout) by assigning this value to its own Confirmation Code.
- When displaying monthly earnings, this will always be assigned to the month of initial booking. Suppose, Guest A initially booked for March 27 for 7 days. Then he extended his booking to another 7 days which will begin on April 3 and end on April 9. The consolidated total earning of that booking will be reflected in the March monthly report. In this regard, even if Guest A extends to another 30 days, the earning will still reflect in the March monthly report and not in April monthly report. Our report should display the total number of days of this booking which can best explain why March had a higher earning. (There is still room for improvement to assign precisely the nightly booking to its own monthly earning.)
- Payout includes cleaning fee.

**DATA PRIVACY**

To protect the privacy of the data, we have excluded the name of the guest and changed the Confirmation Code of each booking by employing Python programming

**TOOLS AND SOFTWARE**

We will be using Python for data preprocessing, exploratory data analysis, and Tableau for data visualization and reporting.

**THE DATASET**

The data contains 277 entries and 11 variables.

**Variables**

- Date (object) - mm/dd/yyyy - One day after Start Date
- Type (object) - (Reservation, Resolution Payout, Misc Credit, Resolution Adjustment, Adjustment, Payout) - type of transaction
- Confirmation Code (object) - transformed 10-letter string in reference to guest; with null
- Start date (object) - date when transaction kicked in; with null
- Nights (float64) - number of nights of stay
- Currency (object) - currency received or sent
- Amount (float64) - amount of transaction; with null if 'Type' Payout category
- Paid Out (float64) - amount of transaction on 'Type' Payout category; with null
- Host Fee (float64) - amount the host pays Airbnb service. This amount is already deducted from 'Amount' on 'Type' Reservation.
- Cleaning Fee (float64) - amount included in the transaction on 'Type' reservation. This is the amount charged to guests.
- Earning Year (float64) - year of earning

To view how data is processed and analyzed, please check the Python Notebook found on root directory:

_Short_Term_Stays(Data_Manipulation).ipynb_
