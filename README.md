# lab6_Pseudocode.py
This is my lab 6 for my CIS class.

# Lab6.py
# CIS 129
# Elias Wilber
# 12937




from math import *

# The following code is Pseudocode
# Please convert the following code to Python Code and save as Lab6.py

# main module                                
def main():
    totalHotDogs = 0
    totalHotDogs = getTotalHotDogs()

    FRANKS = 10 # USE TO BE TORTILLAS
    BUNS = 8 # USE TO BE BEANS

# Local variables
    franksLeft = 0
    bunsLeft = 0
    minFranks = 0
    minBuns = 0 


    franksLeft = (FRANKS - totalHotDogs % FRANKS) % FRANKS
    minFranks = ceil(totalHotDogs / FRANKS)
    bunsLeft = (BUNS - totalHotDogs % BUNS) % BUNS
    minBuns = ceil(totalHotDogs / BUNS)
    showResults(franksLeft, minFranks, bunsLeft, minBuns)

def getTotalHotDogs():
    peopleAttending  = 0 
    dogsPerPerson = 0 
    
    peopleAttending = int(input("Enter the number of people attending the cookout: "))

    dogsPerPerson = int(input("Enter the number of Hot Dogs for each person: "))
    
    total = peopleAttending * dogsPerPerson
    return total


def showResults(franksLeft, minFranks, bunsLeft, minBuns):
    print("Minimum packages of Hot Dogs needed: ", minFranks)
    print("Minimum packages of buns needed: ", minBuns)
    print("Hot Dogs left over: ", franksLeft)
    print("Servings of buns left over: ", bunsLeft)


main()

