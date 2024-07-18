This project is about creating the database about Railway Reservation System.
The railway reservation system facilitates the passengers to enquire about
the trains available on the basis of source and destination, booking and
cancellation of tickets, enquire about the status of the booked ticket, etc. The aim
of case study is to design and develop a database maintaining the records of
different trains, train status, and passengers. The record of train includes its
number, name, source, destination, and days on which it is available, whereas
record of train status include dates for which ticket can be booked, total number
of seats available, and number of seats already booked.
Passengers can book their tickets for the train in which seats are available.
For this, passenger has to provide the desired train number and the date for which
ticket is to be booked. Before booking a ticket for a passenger, the validity of train
number and booking date is checked. Once the train number and booking date are
validated, it is checked whether the seat is available. If yes, the ticket is booked
with confirm status and corresponding ticket ID is generated which is stored
along with other details of the passenger. The ticket once booked can be cancelled
at any time. For this, the passenger has to provide the ticket ID (the unique key).
The ticket ID is searched and the corresponding record is deleted. With this, the
first ticket with waiting status also gets confirmed.

List of Assumption Since the reservation system is very large in reality, it
is not feasible to develop the case study to that extent and prepare documentation
at that level. Therefore, a small sample case study has been created to demonstrate
the working of the reservation system. To implement this sample case study, some
assumptions have been made, which are as follows:

1. The number of trains has been restricted to 20.
2. Only two categories of tickets can be booked, namely, AC (a)and General(b).
3. The total number of tickets that can be booked in each category (AC and
General) is 10.
4. The total number of tickets that can be given the status of waiting is 2.
5. The in- between stoppage stations and their bookings are not considered.

List of trains has to be maintained. Detailed Passenger information is to be
maintained In the booking procedure, the train number, train date, and category
are read from the passenger. On the basis of the values provided by the passenger,
corresponding record is retrieved from the Train Status. If the desired category is
AC, then total number of AC seats and number of booked AC seats are compared
in order to find whether ticket can be booked or not. Similarly, it can be checked
for the general category. If ticket can be booked, then passenger details are read
and stored in the Passenger table. In the cancellation procedure, ticket ID is read
from the passenger and corresponding record is searched in the Passenger. If the
record exists, it is deleted. After deleting the record (if it is confirmed), first record
with waiting status for the same train and same category are searched from the
Passenger table and its status is changed to confirm.
