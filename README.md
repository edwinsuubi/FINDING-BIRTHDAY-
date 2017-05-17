# FINDING-BIRTHDAY-
Gives the real day on which someone was born.


import calendar  
a=input("Input your year of birth?\n")
b=input("Now input your birth month using numbers from 1-12:\n")
c=input("Now input the day of the month on which you were born also using numbers from 1-31:\n")
x=calendar.weekday(year=int(a), month=int(b), day=int(c))

#prefix=  ['st','nd','rd']+ 17*['th']+['st','nd','rd']+17*['th']+['st'](this is the other method that can be used.)
if int(c) == 1:
    d = c +"st"
elif int(c)==2:
    d = c +"nd"
elif int(c)==3:
    d = c +"rd"
elif int(c) >= 4 and int(c) <= 20:
    d = c +"th"
elif int(c)==21:
    d = c +"st"
elif int(c) == 22:
    d = c +"nd"
elif int(c) == 23:
    d = c +"rd"
elif int(c) == 31:
    d = c +"st"
else:
    d = c+"th"

if int(b) == 1:
        m = "January"
elif int(b) == 2:
        m = "February"
elif int(b) == 3:
        m = "March"
elif int(b) == 4:
      m = "April"
elif int(b) == 5:
        m = "May"
elif int(b) == 6:
        m = "June"
elif int(b) == 7:
        m = "July"
elif int(b) == 8:
        m = "August"
elif int(b) == 9:
        m = "September"
elif int(b) == 10:
        m = "October"
elif int(b) == 11:
     m = "November"
else:
    m = "December"

    
    
if x == 0:
    y = "Monday"
elif x == 1:
    y = "Tuesday"
elif x == 2:
    y = "Wednesday"
elif x == 3:
    y = "Thursday"
elif x == 4:
    y = "Friday"
elif x == 5:
    y = "Saturday"
else:
    y = "Sunday"

print("you were born on "+y+" "+d+", "+m+" "+a)
