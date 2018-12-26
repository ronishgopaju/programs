import re
time=input("please enter time:")
regex= re.sub(r"[a-zA-Z]","",time,flags=re.I) #remove am/pm .........................
regex= re.sub(r"\W","",regex,flags=re.I) #remove '':'' and spaces................... gives only numbers
#print(regex)
t= re.search(r"[a-zA-Z]+",time) #search for am / pm....................
if t is None:
    print("invalid time")
else:
    t=(t.group(0))
    check= int(regex[-2:]) 
    # check if minute is valid or not
    if check>60:
        print("invalid time")
    else:
         #remove minutes 2 string from back.......................................
        regex1=regex[:-2]
         #type casting...................................
        regex1= int(regex1)
        #check am/pm...................
        if t=="am" or t=="AM":
            #print("it is am")
            if regex1>12:
                print ("invalid time")
            else:
                print("good morning")
        #pm then 12-6 is evening and 6-11 is night......................
        elif t=="pm" or t=="PM":
            #print("it is pm")
            if regex1 >= 1 and regex1 <= 6:
                print("good evening")
            elif regex1==12:
                print("good evening")
            elif regex1>6 and regex1<=11:
                print("goodnight")
            else:
                print("invalid time")
        else:
            print("invalid time")
