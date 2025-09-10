#JSON 
JSON is a syntax for storing and exchanging data.
JSON is text, written with JavaScript object notation.
Python has a built-in package called json, which can be used to work with JSON data.
Convert from JSON to Python:
import json
# some JSON:
x =  '{ "name":"John", "age":30, "city":"New York"}'
# parse x:
y = json.loads(x)
# the result is a Python dictionary:
print(y["age"]) -> 30

Convert from Python to JSON:
import json
# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}
# convert into JSON:
y = json.dumps(x)
# the result is a JSON string:
print(y) -> {"name": "John", "age": 30, "city": "New York"}

***you can convert python duct list tuple string int folat etc yo json strings
When you convert from Python to JSON, Python objects are converted into the JSON (JavaScript) equivalent:
Python	JSON
dict	Object
list	Array
tuple	Array
str	String
int	Number
float	Number
True	true
False	false

- sometimes the output of json.dumps is difficult to read so we have some parameters ro parse our string
  - indent: parameter to define the numbers of indents: json.dumps(x, indent=4)
  - separators parameter to change the default separator:json.dumps(x, indent=4, separators=(". ", " = "))
  - sort_keys parameter to specify if the result should be sorted or not:json.dumps(x, indent=4, sort_keys=True)

# REGEX 
RegEx can be used to check if a string contains the specified search pattern.
Python has a built-in package called re, which can be used to work with Regular Expressions.
import re
Functions in regex are as follows:
Function	Description
findall	- Returns a list containing all matches
search	- Returns a Match object if there is a match anywhere in the string
split	- Returns a list where the string has been split at each match
sub	- Replaces one or many matches with a string
Re also has some metacharacters ehich hold special meaning:
Such as ^ means starts with $ mrans end with and many more.
