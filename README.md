# IntroToCS1
This will be a working repository for Intro to Computer Science 1
Gunnar Brown
"Addding Members"

#Noah, Gunnar, Nick
# Team Slytherin

#Lab 2  - Calendar Project



# Greeting
#Variables listed
#Var
#Get input
#If else
#loops
# Create Formating
# Output




import math as m

#greeting -
print('Hey there and welcome to the calendar program! ')


#var list

year = int(input('What year are you looking for? 1800-2099 '))

while year < 1800 or year > 2099:
year = input('Please input a corresponding year. 1800-2099: ')

century_digits = int(str(year)[:2])

year_digits = int(str(year)[-2:])

month = input('Please input a month. ex: Jan, Feb, Mar: ')
monthList = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']


while month not in monthList:
month = input('Please input a correct month. ')

value = year_digits + m.floor(year_digits/4)



#Century Value Calulations
if century_digits == 18:
value = value + 2
elif century_digits == 20:
value = value + 6



#Month Value Calculations

if month == monthList[0] and (year%4 != 0):
value= value +1
elif month == monthList[1] and (year%4 == 0):
value= value +3
if month == monthList[1] and (year%4 != 0):
value= value +4
elif month == monthList[2] or month== monthList[10]:
value= value +4
elif month == monthList[3] or month==monthList[6]:
value= value +0
elif month == monthList[4]:
value= value +2
elif month == monthList[5]:
value= value +5
elif month == monthList[7]:
value= value +3
elif month == monthList[9]:
value= value +1
elif month == monthList[8] or month==monthList[11]:
value= value +6


day = 0
#Days in month
if month == monthList[1]:
if (year%4)==0:
day = 29
else:
day = 28
elif month in('Jan', 'Mar', 'May', 'Jul', 'Aug', 'Oct', 'Dec'):
day = 31
elif month in('Sep', 'Apr', 'Jun', 'Nov'):
day = 30


value = (value + 1)%7

start=0
if value == 1:
start=='Sun'
elif value == 2:
start='Mon'
elif value == 3:
start='Tues'
elif value == 4:
start='Wed'
elif value == 5:
start='Thur'
elif value == 6:
start='Fri'
elif value == 0:
start='Sat'
