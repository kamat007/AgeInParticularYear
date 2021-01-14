# AgeInParticularYear

age = input("Enter your age or the birth year: ")
length = len(age)

def turn_100():
    print("after", 100 - int(age), "years you will be 100")

def In_year():
    year = input("Enter the year you would like to know your age at ")
    at_year = int(year) - int(age)
    print("In", year, "you will be", at_year, "years old.")

if age.isdigit() is True:
    try:
        if length >= 1 or length <= 3:
            if int(age) >= 120:
                print("You seem to be the oldest person alive")
            else:
                if length <= 2:
                    print(f"Your are {age} years old")
                    ques1 = input("would you like to know after how many years you will turn 100 years old?").lower()
                    if ques1 == 'y' or ques1 == 'yes':
                        turn_100()
                    elif ques1 == 'n' or ques1 == 'no':
                        print("OK")
                    else:
                        print("Wrong Input!!! Looks like you don't wanna know.")
        elif length == 4:
            print(f"Your birth year is {age}")
            year1 = 2021 - int(age)
            if year1 >= 121:
                print("Are you IMMORTAL?!")
            else:
                ques2 = input("Would you like to know your age in particular year?").lower()
                if ques2 == 'y' or ques2 == 'yes':
                    In_year()
                elif ques2 == 'n' or ques2 == 'no':
                    print("OK")
                else:
                    print("Wrong Input!!! Looks like you don't wanna know.")
        else:
            print("Wrong input")
    except Exception as e:
        print(e)
else:
    print("You must give the input in integer, it should be either your age or your birth year")
