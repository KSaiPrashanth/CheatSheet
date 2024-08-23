# Python Cheat Sheet : The Basics

## Data Types

### String
Series of characters or data stored as text
my_string = "Hello"

### String Operations
- returns the string with all uppercase letters
    ```python
    my_string.upper()
    ```
- returns the length of a string
    ```python
    len(my_string)
    ```
- returns the index of the first instance of the string inside the subject string, otherwise -1
    ```python
    my_string.find('l')
    ```
-  replaces any instance of the first string with the second in my_string
    ```python
    my_string.replace('H', 'C')
    ```

### Integer
A whole number
```python
my_integer = 12321
```
### Float
A decimal number
```python
my_decimal = 3.14
```
### Boolean
Discrete value true or false
```python
a = True
b = False
```

### Dictionary
Changeable collection of key-value pairs
```python
my_dictionary = {'banana': 1, 12: 'laptop', (0,0):'center'}
```

### Dictionary Operations
- Access value using key
    ```python
    my_dictionary['banana']
    ```
- Get all keys in a dictionary as a list
    ```python
    my_dictionary.keys()
    ```
- Get all values in a dictionary as a list
    ```python
    my_dictionary.values()
    ```

### Tuple
Unchangeable collection of objects
```python
tup = (1, 3.12, False, "Hi")
```

### List
Changeable collection of objects
```python
my_collection = [1, 1, 3.12, False, "Hi"]
```

### List Operations
- returns the length of a list
    ```python
    len(my_collection)
    ```
- Add multiple items to a list
    ```python
    my_collection.extend(["More", "Items"])
    ```
- Add a single item to a list
    ```python
    my_collection.append("Single")
    ```
- Delete the object of a list at a specified index
    ```python
    del(my_collection[2])
    ```
- Clone a list
    ```python
    clone = my_collection[:]
    ```
- Concatenate two lists
    ```python
    my_collection_2 = ["a", "b", "c"]
    my_collection_3 = my_collection + my_collection_2
    ```
- Calculate the sum of a list of ints or floats
    ```python
    number_collection = [1,2,3,4.5]
    sum(number_collection)
    ```
- Check if an item is in a list, returns Boolean
    ```python
    item in my_collection
    ```
- Check if an item is not in a list, returns Boolean
    ```python
    item not in my_collection
    ```

### Set
Unordered collection of unique objects
```python
a = {100, 3.12, False, "Bye"}
b = {100, 3.12, "Welcome"}
```

### Set Operations
- Convert a list to a set
    ```python
    my_set = set([1,1,2,3])
    ```
- Add an item to the set
    ```python
    a.add(4)
    ```
- Remove an item from a set
    ```python
    a.remove("Bye")
    ```
- Returns set a minus b
    ```python
    a.difference(b)
    ```
- Returns intersection of set a and b
    ```python
    a.intersection(b)
    ```
- Returns the union of set a and b
    ```python
    a.union(b)
    ```
- Returns True if a is a subset of b, false otherwise
    ```python
    a.issubset(b)
    ```
- Returns True if a is a superset of b, false otherwise
    ```python
    a.issuperset(b)
    ```

### Indexing
Accessing data from a string, list, or tuple using an element number
```python
my_string[element_number]
my_collection[element_number]
my_tup[element_number]
```

### Slicing
Accessing a subset of data from a string, list, or tuple using element numbers from start to stop -1
```python
my_string[start:stop]
my_collection[start:stop]
my_tup[start:stop]
```



## Comparison Operators
Comparison 0perators compare operands and return a result of true or false
### Equal
```python
a == b
```
### Less Than
```python
a < b
```
### Greater Than
```python
a > b
```
### Greater Than or Equal
```python
a >= b
```
### Less Than or Equal
```python
a <= b
```
### Not Equal
```python
a != b
```

### Python Operators
- `+` : Addition
- `-` : Subtraction
- `*` : Multiplication
- `/` : Division
- `//` : Integer Division (Result rounded to the nearest integer)



## Conditional Operators
Conditional 0perators evaluate the operands and produce a true of false result

### And
Returns true if both statement **a and b are true**, otherwise false
```python
a and b
```

### Or
Returns true if either statement **a or b are true**, otherwise false
```python
a or b
```

### Not
Returns the **opposite** of the statement
```python
not a
```



## Loops
### For Loops
```python
for x in range(x):
```
Executes loop x number of times
 ```python
for x in iterable:
```   
Executes loop for each object in an iterable like a string, tuple, list, or set

### While Loops
```python
while statement:
```
Executes the loop while statement is true



## Conditional Statement
```python
if statement_1:
    # Execute of statement_1 is true
if statement_2:
    # Execute if statement_1 is false and statement_2 is true
else:
    # Execute if all previous statements are false
```



## Try/Except
```python
try:
    # Code to try to execute
except a:
    # code to execute if there is an error of type a
except b:
    # code to execute if there is an error of type b
except:
    # code to execute if there is any exception that has not been handled
else:
    # code to execute if there is no exception
```



## Error Types
- IndexError - When an index is out of range

- NameError - When a variable name is not found

- SynntaxError - When there is an error with how the code is written

- ZeroDivisionError - When your code tries to divide by zero



## Range
- Produce an iterable sequence from 0 to stop-1
    ```python
    range(stop)
    ```

- Produce an iterable sequence from start to stop-1 incrementing by step
    ```python
    range(start, stop, step)
    ```


## Webscraping
- Import BeautifulSoup
  ```python
  from bs4 import BeautifulSoup
  ```

- Parse HTML stored as a string
  ```python
  soup = BeautifulSoup(html, 'html5lib')
  ```

- Returns formatted html
  ```python
  soup.prettify()
  ```

- Find the first instance of an HTML tag
  ```python
  soup.find(tag)
  ```

- Find all instances of an  HTML tag
  ```python
  soup.find_all(tag)
  ```



## Requests
- Import the requests library
  ```python
  import requests
  ```
<br>

- Send a get requests to the url optional parameters
  ```python
  response = requests.get(url, parameters)
  ```
<br>

- Get the url of the response
  ```python
  response.url
  ```

- Get the status code of the response
  ```python
  response.status_code
  ```

- Get the headers of the request
  ```python
  response.request.headers
  ```

- Get the body of the requests
  ```python
  response.request.body
  ```

- Get the headers of the response
  ```python
  response.headers
  ```

- Get the content of the response in text
  ```python
  response.text
  ```

- Get the content of the response in json
  ```python
  response.json()
  ```

<br>

- Send a post requests to the url optional parameters
  ```python
  requests.post(url, parameters)
  ```



## Functions
- Create a function
  ```python
  def function_name(optional_parameter_1, optional_parameter_2):
    # code to execute
    return optional_output
  ```

- Calling a function
  ```python
  output = function_name(parameter_1, parameter_2)
  ```



## Working with Files
### Reading a File
- Opens a file in read mode
  ```python
  file = open(file_name, "r")
  ```

- Return the file name
  ```python
  file.name
  ```

- Return the mode of file was opened in
  ```python
  file.mode
  ```

- Reads the contents of a file
  ```python
  file.read()
  ```

- Read a certain number of characters of a file
  ```python
  file.read(characters)
  ```

- Read a single line of a file
  ```python
  file.readline()
  ```

- Read all the lines of a file and stores it in a list
  ```python
  file.readlines()
  ```

- Closes a file
  ```python
  file.close()
  ```

### Writing to a File
- Opens a file in write mode
  ```python
  file = open(file_name, "w")
  ```

- Writes content to a file
  ```python
  file.write(content)
  ```

- Adds content to the end of a file
  ```python
  file.append(content)
  ```



## Objects and Classes
- Creating a class
  ```python
  class class_name:
    def __init__(self. optional_parameter_1, optional_parameter_2)
        self.attribute_1 = optional_parameter_1
        self.attribute_2 = optional_parameter_2

    def method_name(self, optional_parameter_1):
        # Code to execute
        return optional_output
  ```

- Create an instance of a class
  ```python
  object = class_name(parameter_1, parameter_2)
  ```

- Calling an object method
  ```python
  object.method_name(parameter_3)
  ```
