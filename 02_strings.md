# STRINGS
Strings in python are surrounded by either single quotation marks, or double quotation marks.
'hello' is the same as "hello"

# DECLARING A STRING
s="Python is a good language"
t="It's good for data science"

# CONCATING TWO STRINGS
v=s+" "+t    -> Python is a good language  It's good for data science

# TYPE CASTING IN STRING
price=12
s="The price of this book"
v=s+'is:'+str(price)

# INDEXING IN STRING
s="How are you and who are you"
print(s[5])   -> r
print(s[0:10])  -> How are yo
print(s[-1])   -> u   //points at last letter
s[-12:-3]   -> ' who are '
s[1]="e"   -> will throw error as python does not support item assignment in strings
s[:12]  -> will start from 0 index
s[3:]  ->will go till end
s[::-1]  -> will reverse the string
print(len(s))  ->27 //print length of string

# FUNCTIONS IN STRING

//strip() - removes white spaces
a= "       priyanka garg     "
b=a.strip()
print(b)   -> priyanka garg

//a.lower() - lowers the letter
a="PRIYANKA"
print(a.lower())  -> priyanka

//a.upper() - works opposite to lower

//a.replace() - will replace something with something
a=" ABC deFg ;; sadfa QF"
d=a.replace(";","#")
print(d)   ->  ABC deFg ## sadfa QF

//a.split()  - will split as soon as given thing encounters
a="abc;def;hgydfa;yy23"
L=a.split(";")
print(L)  -> ['abc', 'def', 'hgydfa', 'yy23']

- you see you get a list so you can index in this like L[1]

  //a.capitalize() - will capitiize the first letter

  // "abc" =="abc"  -> True

  //"abc"<"def" -> True , this operator works on the basis of alphabetical order

  # FORMATTING OF STRING
  print("we are learning \"string\" here")  -> we are learning "string" here.
  or
  print('we are learning "string" here') -> we are learning "string" here.
  rather than
  print("WE are learning"string"here")

  print(r"c:\name\drive") -> c:\name\drive
  rather than
  print("c:\name\drive")  -> as here \n will be treated as next line
  If you want to read it like normal text use r
