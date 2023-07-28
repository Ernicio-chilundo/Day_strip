# Day_strip
#I will use as main datetime library, when developing the program I can add other libraries. This program will subtract days in the one year to show how many days, hours and seconds are left until your birthday 🥳

from datetime import datetime

date_now = datetime.now()
print("CURRENT DATE:",date_now)
print("WEEKS:",date_now.strftime("%A"))
print()

print("Example >> 02/05/2016")
date_pn = str(input("Date of birth: ")).strip()
if len(date_pn) == 10:
 date_pn = datetime.strptime(date_pn,"%d/%m/%Y")
 print(date_pn)
 print("WEEKS:",date_pn.strftime("%A"))

else:
 print("Error! Follow the example above!")
