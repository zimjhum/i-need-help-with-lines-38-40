# i-need-help-with-lines-41-44
lines 41 through 44 are giving me a hard time no matter how I go about it 


# open file
filename = input('enter data file name:')
infile = open(filename, 'r')
#print(infile.read())

# #read line from file
datalist = []
#
for line in infile:
     #we want to get data from line
    date, l, h, r, s, sd, w = line.split(';')
     #^^^^^ you must have the same as the # of coulumns or else it will not work
    date = str(date)
    lowtemp = int(l)
    hightemp = int(h)
    rainfall = float(r)
    snow = float(s)
    snow_depth = str(sd)
    wind = str(w)
    y, m, d = date.split("-")
    month = int(m)
    day = int(d)
    year = int(y)
    # #put data into list
    datalist.append([day, month, year, lowtemp, hightemp, rainfall])
# #close file
infile.close()


######## analyze data##########
#get date
month = int(input('for the date you care about, enter the month:'))
day = int(input('for the day date you care about, please enter the day:'))
#year = int(input('for the date you care about, please enter the year: '))

#find historical data for that date
gooddata = []
for singleday in datalist:
     if (singleday[0] == day) and (singleday[1] == month):
        gooddata.append([singleday[2], [singleday[3], [singleday[4], [singleday[5]])

#analyze historical data

########## present data##########
