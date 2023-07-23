Booking of Short Terms Stays Analysis

There are two files:

- Short Term Stays (EDA)
- Short_Term_Stays(Data_Manipulation)

CSV Source file is found on /data/booking_01_2017-06_2023_ed.csv

Tableau is found on /Tableau/airbnb_tableau3.twbx

---

Airbnb Historical Data

Airbnb is popular for providing short-term stays to guests across the globe. A simple search on their app can bring you to a number of options that displays the photos of the room, facilities it provides, the pricing and minimum stay.

We will be looking into the data from November 2019 to January 2023 provided by a Superhost at Airbnb located in Manila. It is a Studio type of condo near Intramuros, de La Salle University-Manila, Rizal Park, Star City, CCP, and other nearby tourist attractions.

Unfortunately, the data does not provide us the origin of guests. Neither does it provide the demographic, which could help us understand the profile of guests further. So this data will only be dedicated on understanding the earning performance and historical data of a Studio condo in Manila from the aforementioned date in the middle of COVID-19 pandemic.

Although the amount of payout is described in the data, it does not refer to which Confirmation Code it belongs to, so we do not know the exact amount we have received from a particular Confirmation Code. It is important to note that transaction may involve adjustment and resolution payout that is external to 'Type' Reservation transaction.

We will be using Python for data cleaning and data preparation, and Tableau for data visualization.

About Dataset

The data contains 277 entries and 11 variables.

Variables

Date (object) - mm/dd/yyyy - One day after Start Date
Type (object) - (Reservation, Resolution Payout, Misc Credit, Resolution Adjustment, Adjustment, Payout) - type of transaction
Confirmation Code (object) - 10-letter string in reference to guest; with null
Start date (object) - date when transaction kicked in; with null
Nights (float64) - number of nights of stay
Currency (object) - currency received or sent
Amount (float64) - amount of transaction; with null if 'Type' Payout category
Paid Out (float64) - amount of transaction on 'Type' Payout category; with null
Host Fee (float64) - amount host pays Airbnb service. This amount is already deducted from 'Amount' on 'Type' Reservation.
Cleaning Fee (float64) - amount included in the transaction on 'Type' reservation. This is the amount charged to guests.
Earning Year (float64) - year of earning
