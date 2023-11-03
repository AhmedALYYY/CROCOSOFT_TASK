# CROCOSOFT_TASK

Car Hire Management System
Requirements
The Car Hire Management System is designed to streamline the rental process for cars and vans. Key features include:

Vehicle Categorization:

Vehicles are categorized into small cars (up to 4 people), family cars (up to 7 adults), and vans.
Booking Information:

Each booking includes details such as customer information, selected vehicle, date of hire, and return date.
Time Constraints:

Customers are restricted from hiring a car for longer than a week.
Booking Process:

If a vehicle is available, customer details are recorded, and a new booking is made.
Advanced Booking:

Potential or existing customers can book a vehicle up to 7 days in advance, subject to availability.
Payment Process:

Customers are required to pay for the vehicle at the time of hire.
Availability Check:

Employees can efficiently check the availability of cars and vans in response to inquiries.
Invoice Generation:

An invoice is generated at the time of booking for the customer's records.
Confirmation Letter:

For advance bookings, a confirmation letter is sent to the customer.
Daily Reports:

A report is automatically generated at the start of each day, providing an overview of bookings.
Entity Relationship Diagram (ERD)
ERD

Getting Started Locally
Prerequisites
Install pipenv:
pip install pipenv
Setup
Activate the virtual environment:


pipenv shell
Install dependencies:


pipenv install
Create a MySQL database:


mysql -u root -p
mysql> CREATE DATABASE car_rent;
Update MySQL configuration in the .env file.

Start the Flask server:
flask run

SQL Schema


# Creating a connection cursor
cursor = mysql.connection.cursor()

# Executing SQL Statements
cursor.execute('''
    CREATE TABLE IF NOT EXISTS CUSTOMER (
        CUSTOMER_ID INTEGER NOT NULL AUTO_INCREMENT,
        FIRST_NAME VARCHAR(30) NOT NULL,
        LAST_NAME VARCHAR(30) NOT NULL,
        EMAIL_ADDRESS VARCHAR(64) NOT NULL,
        TELEPHONE_NUMBER CHAR(12) NOT NULL,
        PRIMARY KEY (CUSTOMER_ID)
    )
''')


