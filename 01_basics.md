- Python has a simple syntax similar to the English language.
- Python has syntax that allows developers to write programs with fewer lines than some other programming languages.
- Python runs on an interpreter system, meaning that code can be executed as soon as it is written. This means that prototyping can be very quick.
- Python can be treated in a procedural way, an object-oriented way or a functional way.

  #PRINTING A STATEMENT IN PYTHON
  print("hello world")

  #DECLARING VARIABLES IN PYTHON
  x=5  //int
  y=5.6  // float
  z=true //bool
  a="abcde" //string
  b=2+3j  //complex

  #TO CHECK TYPE OF VARIABLE
  print(type(x))   //int
  x.dtype   //int
  %whos //tells about all the varibales that have been declared till now

  #OPERATORS
  //addition
  x= a+b
  print(x)

  //concation of strings
  s1="a"
  s2="b"
  s=s1+s2
  print(s)

  //floor divison
  10//3  -> 3

  //divison
  10/3  -> 3.333

  #BOOL OPERATORS
  a=True
  b=True
  c=False

  //print(a and b)  -> True
  //print(a and c)  -> False
  //print(a or c)   -> True
  //not(a)  -> False
  //d= 3==4   print(d)   -> False

  #SOME OTHER USEFUL FUNCTIONS

  //round - round off the integers
  print(round(4.34567,2))   -> 4.35

  //divmod
  G=divmod(34,9)
  print(G)   ->(3,7)
  print(type(G))   -> tuple
  print(G[1]) -> 7

  //isinstance - check the datatype of variable
  a=isinstance(7.6,int)   -> False
  isinstance(3.4,(int,float))    ->True   //checks for more than one varibale type

  //power
  a=pow(2,4)   -> 16

  //input - to take input from user
  a=input("Enter a number")
  a= float(input("Enter a number")  //will conver the input to folat form....also known as typecasting

  //CONTROL FLOW STATEMENT

  //if statement:
  a=int(input())
  b=int(input())
  if a>b:
      print(a)
      print("I am still inside if condition")
  print()

  //if-ele statement:
  a=int(input())
  b=int(input())
  if a>b:
      print(a)
  else:
      print(b)

  //if-elif - when there is more than one else statement then we use elif
  a=1
  b=5;
  if a==b:
      print("Equal")
  elif a>b:
      print("A")
  else:
      print("B")
  print("Not in if")
    
  //nested-if
 a=int(input())
 if a>10:
      print(">10")
      print("Inside the top if")
      if a>20:
          print(">20")
          print("Inside the nested if")
      else:
          print("<=20")
          print("Inside the else part of nested if")
  print("Outside all iffs")

  #CONTROL LOOP

  //while loop - first check conditions then do the work
  n=int(input())
  i=1
  while i<n:
      print(i**2)
      print("This is iteration number:",i)
      i+=1 
  print("Loop done")

  //for loop
  L=[]  //list format
  for i in range(10):   //for loop
      print(i+1)
      L.append(i**2)    //append will add in empty list

  #FUNCTIONS

  //syntax to write function:
  def function_name(arguments):
     //define function

  //we can have two type of argumnets in our function:
  // VARIABLE NUMER OF INPUT ARGUMENTS - *args
  // HELPS US TO MAKE DINCTIONARY - **args

  #DEFAULT VALUES
  def gg(s=4):
    print(s) -> 4
  //if we do gg(56) ->then it will get updates and 56 will be printed.
  
  
