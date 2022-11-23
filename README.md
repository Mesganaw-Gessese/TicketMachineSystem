# TicketMachineSystem
This Is The Ticket Machine System Code With Timer
cosmetics = 0
perfumes = 0
medicine =0

import time
def countdown(time_sec):
    while time_sec:
        mins, secs = divmod(time_sec, 60)
        timeFormat = '{:02d}:{:02d}'.format(mins, secs)
        # print(timeformat,end="\r")
        time.sleep(1)
        time_sec -= 1
        print(timeFormat)


    print("try again later")

def activities():
    act =input(
        "What kind of activity you want to do?\n"
        "insert 'c' for cosmetics\n"
        "insert 'p' for perfumes\n"
        "insert 'm' for pharmaceuticals\n"
        "please choose your product area: "

    )
    return act

def message():
    print("Please wait and someone will assist you shortly.")
    print("_________________________________________________")
    # return msg
    # return msg




list =[346369309,123456789]
cou =0
ID = int(input("please insert your id: "))
while cou < 3:

  if ID in list:
      order = activities()
      if order == "c":
          cosmetics += 1
          print("_________________________________________________")
          print("Your number is:", f"C -{cosmetics}")
          message()
      elif order == "p":
          perfumes += 1
          print("_________________________________________________")
          print("Your number is:", f"P -{cosmetics}")
          message()
      elif order == "m":
          medicine += 1
          print("_________________________________________________")
          print("Your number is:", f"M -{cosmetics}")
          message()
      stoping = input("Do you want to take another number y/n ?")
      if stoping == "n":
          break
  else:
      cou = 0
      while cou < 3:
          y = int(input("Invalid id, please enter again:"))
          cou = cou + 1
      countdown(30)






