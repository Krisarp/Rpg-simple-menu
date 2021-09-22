# Rpg-simple-menu
Simple menu for an assignment

# for the menu have four basic interactions
# Explore
  #When selected have four directions pop and have the player choose
  #when a direction is chosen say "you entered the room to the (North,South,East< or west), same as before"
# Insepct
  #when selected say "You look around the room your in, There is a single chair and a table with a drawer, open the drawer?"
    #give the player a chocie between yes and no
    # IF YES say "you took the pen.
      
   #If no print "you left the pen in the drawer, there will be more"
   
# inventory
  #When sleceted say "You look into your pockets and see a pen"
  
  
 # Fight
  #Though there isn't any monster in this menu game thing, it is an rpg menu so there should be an attack command
  #When selected print "You throw a punch in air, it hits nothing."
  
# quit
  #when selected say "bye for now"
  #then end the program



# Code is below




#Course: CS 30
#period: 3
#Date created: 2021-09-21
#Date Last modified: 2021-09-22
#Name: Kristopher Purser
#Description: A Simple repeasting menu

#Code adapted from Andy Dolinski's "Making a python #Menu"
#https://www.youtube.com/watch?v=63nw00JqHo0&t=35s
#exploration  "gameplay" inspration from Ms. Cotcher's hero_menu  #example
#https://replit.com/@janicecotcher/heromenu#main.py

import sys
import time

slow = .5

#Menufunctionwiththe5options
def menu():
    print ("[1] Explore")
    print ("[2] Inspect")
    print ("[3] Fight")
    print ("[4] Inventory")
    print ("[5] Quit")




#The part where it asks for input
menu()
option = int(input("What do you want to do? "))


while option !=5:
    if option == 1:
        #prints exploring texts
        print()
        time.sleep(slow)
        print("You explore around the room, ")
        print()
        print(" You see a door to the north, south ,east, and west,")

        #lets the player explore more rooms
        direction = str(input("Which door do you want to go to? "))

        if direction ==("north"):
            time.sleep(.2)
            print()
            print ("You went to the north door, same room as before")

        elif direction ==("south"):
            time.sleep(.2)
            print()
            print ("you went to the south door, same room as before")

        elif direction ==("east"):
            time.sleep(.2)
            print()
            print ("You went to the east door, same room as before")

        elif direction ==("west"):
            time.sleep(.2)
            print()
            print ("You went to the west door, same room as before")

        else:
            print()
            print ("that's not a direction")

    elif option == 2:
        #prints the inspecting texts and lets the user look around the room
        time.sleep(.2)
        print()
        print ("You look around the room,")
        print ("in the corner you see a single chair and table with a drawer")
        #Lets the user look into the drawer
        drawer_ans = str(input("Open the drawer?:"))
          
        if drawer_ans == ("yes"):
          print ("You look in the drawer, there is a pen, you take it.")

        elif drawer_ans == ("no"):
          print ("You decide to not open it")

        else:
          print ("You just look at the drawer instead of giving a valid answer")

    elif option == 3:
        #prints the fight text
        time.sleep(.2)
        print()
        print("You punch the air in front of you, nothing happens")

    elif option == 4:
        #prints your inventory
        time.sleep(.2)
        print()
        print ("You look in your pockets, there are pens in it")

    else:
        print()
        print ("Invalid option, please type 1-5")

    time.sleep(slow)
    print("")
    menu()
    option = int(input("What do you want to do? "))

time.sleep(.2)
print ("Bye for now")
sys.exit()
