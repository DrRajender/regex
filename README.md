# regex
'''Regex Pattern match required in Complex String along with Number &amp; Space'''

import re
f = open("C:/Users/Rajender/OneDrive/Desktop/raj1.txt", "r")
lines=f.readlines()
line2=str(lines)
my_string='/*** DX ERROR:      10942 MODULE HAS INCORRECT VERSION ***/'
patt=re.compile(r"^\d+\s MODULE HAS INCORRECT VERSION")
matches=patt.finditer(line2)
while True:
    for match in matches:
        print(match.group())
        if (match.group()=="MODULE HAS INCORRECT VERSION"):
            print("Consistent")
        else:
            print("Inconsistent")
