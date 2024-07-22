# DAB111_final_project_Group_5

# Hotel Booking Management System
This project is a Hotel Booking Management System that uses Flask for the web application framework, SQLite for the database, and Pandas for data manipulation.

## Details of Dataset
Number of variables - 9
Number of rows -119390

Variable names:
hotel - "name of the hotel"
adults - "number of adults"
children - "number of children"
reservation_status - "Reservation status"
reservation_status_date - "Date of the reservation status"
name - "Name of customer"
email- "Age of customer"
phone-number - "Contact number of customer"
credit_card - "Credit card number"

## Installed the required packages:

pip install pandas
pip install -U Flask
pip install sqlite3

## Imported files
import sqlite3
import csv file to read

## Database Setup

The project uses an SQLite database to manage hotel booking data. Follow these steps to set up the database:
- con=sqlite3.connect('hotel.db'): develops a connection to the database('hotel.db'). If the database doesn't exsit, it will create database('hotel.db').
- cursor=con.cursor(): This execute sql commands.
- Created Dataframe using sql commands and query.
- with open ("Database_Data_python.csv") as file: Opens the Data file.
- csv.reader: helps to read the content in the file.
- if row[0]=='hotel': check whether the first coloumn is "hotel". If yes, then continue which removes the header row from csv data.
- cursor.execute("INSERT INTO hotel_booking VALUES(?,?,?,?,?,?,?,?,?)",(row[0],row[1],row[2],row[3],row[4],row[5],row[6],row[7],row[8])): Insert data into the table.
    -  VALUES(?,?,?,?,?,?,?,?,?)= Creates new row in the data table. ? are represented as the placeholders for the values that is to be inserted.
    -  (row[0], row[1], row[2], row[3], row[4], row[5], row[6], row[7],row[8]): used to insert data in each row of csv file into a database.
-  pd.read_csv: Read the data.
- con.commit(): save the updates in the database
- con.close(): close the connection from the database.

## Run the Flask application:
 Open web browser and go to `http://localhost:7300` to access the application.


### Home Page
Home page shows "Hotel booking status" and "Welcome to our Database".


## About Page
 About page shows the source of our data and the describtion of each variable in the data.