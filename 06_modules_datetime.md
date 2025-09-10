# DATETIME
A date in Python is not a data type of its own, but we can import a module named datetime to work with dates as date objects
import datetime

x = datetime.datetime.now()
print(x) //helps us to display current date
-> Output : 2025-09-10 08:28:35.841970

Return the year and name of weekday:
import datetime
x = datetime.datetime.now()
print(x.year)
print(x.strftime("%A")) //will return day of the week

# Creating Date Objects
To create a date, we can use the datetime() class (constructor) of the datetime module.
The datetime() class requires three parameters to create a date: year, month, day.
Example
Create a date object:
import datetime
x = datetime.datetime(2020, 5, 17)
print(x)
*** Also take paramenters such as (hour, minute, second, microsecond, tzone), but they are optional, and has a default value of 0, (None for timezone)

# The strftime() Method
The datetime object has a method for formatting date objects into readable strings.
The method is called strftime(), and takes one parameter, format, to specify the format of the returned string:
	
%a	Weekday, short version	Wed	
%A	Weekday, full version	Wednesday	
%w	Weekday as a number 0-6, 0 is Sunday	3	
%d	Day of month 01-31	31	
%b	Month name, short version	Dec	
%B	Month name, full version	December	
%m	Month as a number 01-12	12	
%y	Year, short version, without century	18	
%Y	Year, full version	2018	
%H	Hour 00-23	17	
%I	Hour 00-12	05	
%p	AM/PM	PM	
%M	Minute 00-59	41	
%S	Second 00-59	08...like this many more are there refer w3 schools for it 
