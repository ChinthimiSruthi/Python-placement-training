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
