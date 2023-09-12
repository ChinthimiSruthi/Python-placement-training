# Python-placement-training
list1=[1,2,3,"Sruthi",True]
print(list1[1:5:2])
#list index starts from 1
print(list1[::-1])
print(list1[-1:-2:2])#if starting index is -1 then the list will be empty
print(list1[-5:-2:2])#-1 index starts from 
text1="hello,world!"
text2="welcome"
list1=[1,2,3,"Sruthi"]
sliced_text1=text1[6:-1:2]
sliced_text2=text1[-6:1:-2]
print(sliced_text1)
print(sliced_text2)
list1.append("Michella")
print(list1)
list1.append(4)
print(list1)
list1.insert(3,5)#3 represents index where the number 5 should be placed
print(list1)
list1.pop(3) #Here 3 represents index
print(list1)
list1.reverse()
print(list1)
val=1,2,3
print(val) #Here in output it will print tuple automatically without mentioning val in brackets-()
tuple1=(10,20,30)
result1=tuple1[0]
print(result1)
tuple2=(10,20,30)
x,y,z=tuple2
print(tuple2)
print(x,y,z)
tuple3=(10,20,30,40)
#x,y,z=tuple3
#print(tuple3) #Throws error as count is not same
concat_tuple=tuple2+tuple3
print(concat_tuple)
#REPETITION
#Tuples can be replaced using the * operator
original_tuple=(1,2,3)
repeated_tuple=original_tuple*3
print(repeated_tuple)
#Tuples are immutable that we cannot change
numbers=[1,2,3,4,5]
squared_numbers=[x ** 2 for x in numbers] #multiplies the numbers with 2 or any given  number that wants to be multiplied with numbers
print(squared_numbers)
# tuple has only two built-in methods- count() and index()
#Count()- The Count() methods counts the occurances of a specific element in a tuple
tuple4=(1,2,3,4,5,6,6,7,8,9)
count_tuple=tuple4.count(6) #Counts number of 6's in tuple4
print(count_tuple)
#index()-The index() method finds the index of the of the element specified
index_tuple=tuple4.index(4) #Prints the index of number 4
print(index_tuple)
#Tuples with list
list2=[1,2,3]
list3=[3,4,6]
print(list(zip(list2,list3)))
tuple_list=([1,2,3],["a","b","c"])
for sublist in tuple_list:
    for item in sublist:
      print(item)
#Set is unordered without any index
set1={1,2,3,4,"sruthi"}
print(set1)
set2=set([6,7,8])   #set using set() constructor
print(set2)
set3={1,2,3}
set3.add(4)
print(set3)
set4={5,6,7}
set4.remove(6)
print(set4)
set5={8,9,10}
set5.discard(8)
print(set5)
set6={1,2,4}
set7={4,5,6}
union=set6|set7
print(union)
intersection=set6&set7
print(intersection)
difference=set6-set7
difference1=set7-set6
print(difference)
print(difference1)
score=float(input("Enter score of students:"))
if score>=90:
  print("A")
elif score>=80 and score<=89:
  print("B")
elif score>=70 and score<=79:
  print("C")
else:
  print("D")
my_dict={"name":"Alice","age":30,"city":"NewYork"}
name=my_dict["name"]  #"Alice"
age=my_dict["age"]  #30
print(name)
print(age)
all_keys=my_dict.keys()
all_values=my_dict.values()
all_items=my_dict.items()
print(all_keys)
print(all_values)
print(all_items)
number=int(input("Enter a number:"))
if number%2==0:
  print("Even number")
else:
  print("Odd number")
#PASSWORD VALIDATION
lower,upper,digit=0,0,0
char=input("Enter password:")
if(len(char)>=8):
  for i in char:
    lower+=1
    if(i.isupper()):
      upper+=1
    if(i.islower()):
      digit+=1
if(lower>=1 and upper>=1 and digit>=1):
  print("valid password")
else:
  print("Invalid password")
#another way:
password=input("Enter password:")
length=len(password)>=8
uppercase=any(char.isupper() for char in password)
lowercase=any(char.islower() for char in password)
digit=any(char.isdigit() for char in password)

if(length and uppercase and lowercase and digit):
  print("Strong Password")
else:
  print("Weak Password")
  #create a game where the computer generates random numbers from 1 to 100 #and check whether the number entered is high or low

import random
target =random.randint(1,100)

while True:
  guess=int(input("Guess the number: "))
  if guess < target:
    print("Too Low")
  elif guess > target:
    print("Too High")
  else:
    print("Congrats")
    break
#Iterating through lists:
fruits=["apple","banana","cherry"]
for i in fruits:
    print(i)

flowers={"name":"sruthi","age":19,"place":"hyderabad"}
for i in flowers:
  print(i,flowers[i])

#write a program to check if a given positive integer is a prime number
number=int(input("Enter a number: "))
if number>1:
  for i in range(2,int(number/2)+1):
    if number%i==0:
      print("It is not a prime number")
      break
    else:
      print("It's a prime number")
else:
  print("Not a prime number")

#Default parameters
def power(base,expo=2): #Here we can give expo=2 in default without expressing as power(2,4)
  return base**expo

print(power(2,4))
print(power(4))
#Keyword arguments: args,kwargs
def average(*args):
  return sum(args)/len(args)

print(average(5,10,15))

def person_info(name,age):
  print(f"Name: {name},Age: {age}")

person_info(age=19,name="Sruthi")
class student:
  def __init__(self):
    self.name="Sruthi"
    self.age=19
    self.marks=96.00

  def putdata(self):
    print("Name: ",self.name)
    print("Age: ",self.age)
    print("Marks: ",self.marks)

s=student()
s.putdata()
class Dog:
  def __init__(self,name,breed):
    self.name=name
    self.breed=breed
  def bark(self):
      print(f"{self.name} is barking!")
dog1=Dog("Buddy","Golden Retriever")
dog2=Dog("Max","Poodle")

dog1.bark()
dog2.bark()
class bank:
  def __init__(self,name,balance):
    self.name=name
    self.balance=balance
  def deposit(self,amount):
      if amount>0:
        self.balance+=amount
        print(f"Deposited ${amount}.Newbalance: ${self.balance}")
      else:
        print("Invalid amount.Please deposit a positive amount.")
  def withdraw(self,amount):
      if amount<=0:
        print("Invalid amount.Please withdraw a positive amount.")
      elif amount>self.balance:
        print("Insufficinet balance.")
      else:
        self.balance-=amount
        print(f"withdraw ${amount}. Newbalance : ${self.balance}")

account1 = bank("Alice",1000)
account1.deposit(500)
import json

data={"name":"Sruthi","Age":19}
#dumps is serialisation: converting normal objects into json format
json_string=json.dumps(data)

json_string='{"name":"Sruthi","Age":19}'
#loads is deserialisation: converting json format() into objects
python_object=json.loads(json_string)
import json 

data = { "name": "Sruthi", "age":19 }

with open ("sample.json", "w") as out:
    json.dump(data,out)

with open ("sample.json", "r") as read:
  print (json.load (read))
