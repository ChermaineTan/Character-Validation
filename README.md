# Character-Validation

import time
import random
import datetime
def GetInt():
  print(random.randint(0,100000))

def GetStr():
  wordlist=["remain","resignation","face","core","population","paradox","symbol","attitude","yearn","feminist","diamond","overview","extreme","good","store","curtain","restaurant","counter","bride","quantity"]
  print(random.choice(wordlist))

def GetReal():
  print(random.uniform(0, 1000000))

def GetBool():
  if (random. getrandbits(1))==1:
    print(True)
  else:
    print(False)

def GetChar():
  alphabet=["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z",1,2,3,4,5]
  print(random.choice(alphabet))

def GetDate():
  start = datetime.date(2000, 1, 1)
  end = datetime.date(2020, 2, 1)
  time_ = end- start
  days_= time_.days
  random_number_of_days = random.randrange(days_)
  random_date = start + datetime.timedelta(days=random_number_of_days)
  print(random_date)
Lives=4
Points=0
now = time.time()
while True:
  answers=["integer","char","boolean","real","date","string"]
  GetInt()
  userinput=input("What data type is this?")
  if userinput==answers[0]:
    print("correct")
    Points=Points+1
  else:
    print("Wrong")
    Lives=Lives-1
    if Lives<1:
      break
  GetChar()
  userinput=input("What data type is this?")
  if userinput==answers[1]:
    print("correct")
    Points=Points+1
  else:
    print("Wrong")
    Lives=Lives-1
    if Lives<1:
      break
  GetBool()
  userinput=input("What data type is this?")
  if userinput==answers[2]:
    print("correct")
    Points=Points+1
  else:
    print("Wrong")
    Lives=Lives-1
    if Lives<1:
      break
  GetReal()
  userinput=input("What data type is this?")
  if userinput==answers[3]:
    print("correct")
    Points=Points+1
  else:
    print("Wrong")
    Lives=Lives-1
    if Lives<1:
      break
  GetDate()
  userinput=input("What data type is this?")
  if userinput==answers[4]:
    print("correct")
    Points=Points+1
  else:
    print("Wrong")
    Lives=Lives-1
    if Lives<1:
      break
  GetStr()
  userinput=input("What data type is this?")
  if userinput==answers[5]:
    print("correct")
    Points=Points+1
  else:
    print("Wrong")
    Lives=Lives-1
    if Lives<1:
      break
  break
print(f"Score is {Points}")
now2=time.time()
timetaken=(now2-now)
print(timetaken,"seconds")
print(int(Points*100/timetaken),"score overall")
