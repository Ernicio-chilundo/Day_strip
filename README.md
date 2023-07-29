# Day_strip
I will use as main datetime library, when developing the program I can add other libraries. This program will subtract days in the one year to show how many days, hours and seconds are left until your birthday 🥳

from datetime import datetime

date_now = datetime.now()
print("CURRENT DATE:",date_now)
print("WEEKS:",date_now.strftime("%A"))
print()

print("Example >> 02/05/2016 16:00")
date_pn = str(input("Do you want to predict his birthday for what year: ")).strip()
if len(date_pn) == 16:
 date_pn = datetime.strptime(date_pn,"%d/%m/%Y %H:%M")
 sum_date = date_pn - date_now 
 print(f"Missing {sum_date.days} days to your birthday")
 print("Day of the week:",date_pn.strftime("%A in %B at %H:%M hours"))
 
else:
 print("Error! Follow the example above!")

