# Guess_number
import random
num= random.randint(20,90)

temp =input("number?")
guess=int (temp)
count=0
state=0
times =3
while state!= 1 and count<times:


    if count>=1:
        temp = input("number?")
        guess=int (temp)
    if num<=guess<=100:
        state = 1
    else:
        state = 0

    if num<=guess<=100:
        print("you so good")
    else :
        print("not right")
        if guess>100:
            print ("too large")
        elif guess<num:
            print ("too small")
        count=count+1
        first ='you have '
        sec1=' only '
        sec=' chance'
        secs=' chances'
        s1= first +sec1 + str( times-count ) + str(sec)
        s2 = first + str(times-count ) + str(secs)

        if times-count==1:
            print(s1)
        elif 1<times-count<=times:
            print(s2)
if num<=guess<=100:
    print ("game over! you win")
else:
    print ("game over! you loss")
