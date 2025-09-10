# MODULE 
- A file containing a set of functions you want to include in your application.

# Create a Module
- To create a module just save the code you want in a file with the file extension .py

# Use a Module
- Now we can use the module we just created, by using the import statement
- Suppose you created hello.py now you want to use it in another file then in that file do import hello.py
- Now suppose your hello.py has greeting function that you want to use then you will do import hello.py and then hello.greeting() and your function will be runned
- Remeber folder should be same

# Variables in Module
- The module can contain functions, as already described, but also variables of all types (arrays, dictionaries, objects etc):
Example
Save this code in the file mymodule.py
person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
Example
Import the module named mymodule, and access the person1 dictionary:
import mymodule

a = mymodule.person1["age"]
print(a)

**** You can also import a module as suppose import hello as hey like giving it a nickname

There are several other built in python mudoes such as numpy panda sys dir datetime regex etc.
