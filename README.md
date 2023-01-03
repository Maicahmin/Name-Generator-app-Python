# Name-Generator-app-Python

will Create 3 lists for first name, middle name, and last name with 10 items per list

The application will ask the user to generate a new name.
 
If yes, use a random number between 0 - 9 to randomly select items in the lists

Display the generated name "Congratulations! Your new name is"

If No, display the word "Thank you!" and display all the names that user generated.

----------------------------------------------------------------------------------------------

import random

fname = ["Angela", "Pharsa", "Harith", "Lunox", "Hanabi", "Ling", "Lancelot", "Gusion", "Chang'e", "Aamon"]

mname = ["Min", "Kim", "Lee", "Cy", "Tae", "Nam", "Jung", "Seok", "Tan", "Jeon"]

lname = ["DelaCruz", "Bautista", "Mercado", "DelMonte", "Ramos", "Garcia", "Santos", "Reyes", "Cruz", "Perez"]

store = []


while True:

    name = input("Do you want to generate a new name? [y/n]: ")
    
    if name.upper() == "Y":
    
        mix = random.randint(0, 10)
        
        chose = fname[mix] + " " + mname[mix] + " " + lname[mix]
        
        store.append(chose)
        
        print(f"\nCongratulations! Your new name is: {chose}\n")
        
        continue
        
    elif name.upper() == "N":
    
        print("\nThank you!")
        
        print("\nList of generated names: ")
        
        for x in store:
        
            print(f"{x}")
            
        break
