# TurkishIdentificationSearch

def validation(x):
    strx = str(x)
    nub1 = (int(strx[0]) + int(strx[2]) +int(strx[4])+ int(strx[6]) + int(strx[8])) * 7
    nub2 = int(strx[1]) + int(strx[3]) +int(strx[5])+ int(strx[7]) 
    finNum = nub1 - nub2
    num10 = finNum%10
    num3 = (int(strx[0]) + int(strx[2]) +int(strx[4])+ int(strx[6]) + int(strx[8]) + int(strx[1]) + int(strx[3]) +int(strx[5])+ int(strx[7]) + int(strx[9]))
    num11 = num3%10
    if num10 == int(strx[9]) and num11 == int(strx[10]):
        return True
    else:
        return False
     
for x in range(10000000000,100000000000,+2):
    if validation(x):
        print(x)
