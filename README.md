# DATA_VALIDATION_PROJECT
DATA VALIDATION RULES FOR PASSPORT OFFICE DATABASE USING MS- EXCEL

Project Overview:
In this project, I used Excel to create a data validation system for a Passport Office database. The data includes columns like:

SR No (Serial Number)
Name of Client
Aadhar Number
Phone Number
Date of Birth (DOB)
Appointment Time
Age
City
Landline Number
Customer Feedback
I applied data validation techniques to make sure the data entered into each column is accurate, valid, and follows certain rules.

Explanation of Data Validation Techniques:
SR No (Serial Number):

For the SR No column,
 I used a formula to automatically generate the serial number whenever someone enters a Name of Client. This way, each new row gets a unique serial number without anyone needing to type it in.
Formula used:
=IF(B2="","",AGGREGATE(2,5,$A$1:A1)+1)

Name of Client:
I ensured that only text can be entered in the "Name of Client" column. So, when someone tries to enter something that isn't text (like a number), it will show an error message.
Validation rule:
=ISTEXT(B1)=TRUE

Aadhar Number:
For the Aadhar Number column, I used a validation rule to prevent duplicate entries. This means no two people can have the same Aadhar number in the list.
Validation rule:
=COUNTIF(C:C,C1)=1

Phone Number:
For Phone Numbers, I restricted the input to 10 digits only (no country code). This ensures the phone number format is consistent.
Date of Birth (DOB):

For the DOB column, 
I restricted entries to only people who are 18 years or older. This is important for ensuring the person is of legal age.
Formula used:
=DATEDIF(E2,TODAY(),"Y") (This calculates the age based on the current date)

Appointment Time:
For the Appointment Time column, I restricted the time to between 10 AM and 5 PM. This ensures appointments are scheduled during working hours.

Age Column:
In the Age column, I used a formula to automatically calculate the person's age based on their DOB.
Formula used:
=DATEDIF(E2,TODAY(),"Y")

City:
For the City column, I created a list of accepted cities (in column M). When a user enters a city, the system checks if it's in the list of accepted cities. If not, it shows a message asking if they want to accept the new city or not.
This helps to ensure that only cities from the accepted list are used.

Landline Number:
For the Landline Number column, I added an input message to let the user know that if they don't have a landline number, they can simply leave it empty. This makes it easier for users who don't have a landline.

Customer Feedback:
In the Customer Feedback column, I asked customers to give a rank between 1 and 5. This feedback system helps in rating the services based on customer satisfaction.

Summary:
In this project, I used Excel's data validation tools to ensure that the data entered into the Passport Office database is accurate and follows specific rules. By using formulas, custom validation rules, and input messages, I was able to make data entry more efficient and error-free.

Each validation rule has a specific purpose:
Preventing duplicate or incorrect data
Ensuring valid age, phone numbers, and appointment times
Giving users helpful messages for input guidance
This system makes it easier for users to enter data correctly and helps keep the information organized.

THANKS.

