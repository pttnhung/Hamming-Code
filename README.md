
### 1. **Definition**
- A list in Python is an ordered collection of items (or elements). 

### 2. **Creation**
- Lists are created using square brackets `[]`, with elements separated by commas.
  ```python
  my_list = [1, 2, 3, 4, 5]
  print(my_list)  # Output: [1, 2, 3, 4, 5]
  ```
- Lists can also be created using the `list()` constructor.
  ```python
  my_list = list([1, 2, 3, 4, 5])
  print(my_list)  # Output: [1, 2, 3, 4, 5]
  ```

### 3. **Characteristics**
- **Ordered**: Lists maintain the order of elements.
- **Mutable**: Elements can be changed after the list is created.
- **Allow duplicates**: Lists can have duplicate elements.
- **Heterogeneous**: Lists can contain different data types.

### 4. **Accessing Elements**
- **Indexing**: Elements can be accessed using their index, starting from 0.
  ```python
  first_element = my_list[0]
  print(first_element)  # Output: 1
  ```
- **Negative Indexing**: Access elements from the end of the list.
  ```python
  last_element = my_list[-1]
  print(last_element)  # Output: 5
  ```
- **Slicing**: Access a range of elements.
  ```python
  sub_list = my_list[1:3]  # Elements from index 1 to 2
  print(sub_list)  # Output: [2, 3]
  ```

### 5. **Modifying Lists**
- **Changing Elements**:
  ```python
  my_list[0] = 10
  print(my_list)  # Output: [10, 2, 3, 4, 5]
  ```
- **Adding Elements**:
  - `append()`: Adds an element to the end of the list.
    ```python
    my_list.append(6)
    print(my_list)  # Output: [10, 2, 3, 4, 5, 6]
    ```
  - `insert()`: Adds an element at a specific position.
    ```python
    my_list.insert(1, 2.5)
    print(my_list)  # Output: [10, 2.5, 2, 3, 4, 5, 6]
    ```
  - `extend()`: Adds multiple elements to the end of the list.
    ```python
    my_list.extend([7, 8, 9])
    print(my_list)  # Output: [10, 2.5, 2, 3, 4, 5, 6, 7, 8, 9]
    ```

### 6. **Removing Elements**
- `remove()`: Removes the first occurrence of a specific element.
  ```python
  my_list.remove(2)
  print(my_list)  # Output: [10, 2.5, 3, 4, 5, 6, 7, 8, 9]
  ```
- `pop()`: Removes and returns an element at a specific index (default is the last element).
  ```python
  last_element = my_list.pop()
  print(last_element)  # Output: 9
  print(my_list)       # Output: [10, 2.5, 3, 4, 5, 6, 7, 8]
  ```
- `clear()`: Removes all elements from the list.
  ```python
  my_list.clear()
  print(my_list)  # Output: []
  ```

### 7. **List Operations**
- **Concatenation**: Use `+` to concatenate lists.
  ```python
  my_list = [1, 2, 3]
  new_list = my_list + [4, 5, 6]
  print(new_list)  # Output: [1, 2, 3, 4, 5, 6]
  ```
- **Repetition**: Use `*` to repeat the list.
  ```python
  repeated_list = my_list * 2
  print(repeated_list)  # Output: [1, 2, 3, 1, 2, 3]
  ```
- **Membership**: Use `in` to check if an element exists in the list.
  ```python
  is_in_list = 4 in my_list
  print(is_in_list)  # Output: False
  ```

### 8. **Built-in Functions and Methods**
- `len()`: Returns the number of elements in the list.
  ```python
  length = len(my_list)
  print(length)  # Output: 3
  ```
- `min()`, `max()`: Returns the minimum or maximum element.
  ```python
  smallest = min(my_list)
  largest = max(my_list)
  print(smallest)  # Output: 1
  print(largest)   # Output: 3
  ```
- `sum()`: Returns the sum of all elements.
  ```python
  total = sum(my_list)
  print(total)  # Output: 6
  ```
- `index()`: Returns the index of the first occurrence of an element.
  ```python
  index_of_element = my_list.index(2)
  print(index_of_element)  # Output: 1
  ```
- `count()`: Returns the count of a specific element.
  ```python
  count_of_element = my_list.count(2)
  print(count_of_element)  # Output: 1
  ```
- `sort()`: Sorts the list in ascending order.
  ```python
  my_list.sort()
  print(my_list)  # Output: [1, 2, 3]
  ```
- `reverse()`: Reverses the elements of the list.
  ```python
  my_list.reverse()
  print(my_list)  # Output: [3, 2, 1]
  ```

### 9. **List Comprehensions**
- A concise way to create lists.
  ```python
  squares = [x**2 for x in range(10)]
  print(squares)  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
  ```

### 10. **Nested Lists**
- Lists within lists.
  ```python
  nested_list = [[1, 2, 3], [4, 5, 6]]
  first_element = nested_list[0][1]  # Accesses the element 2
  print(first_element)  # Output: 2
  ```

### 11. **Copying Lists**
- **Shallow Copy**: Using `copy()` method or slicing.
  ```python
  my_list = [1, 2, 3]
  new_list = my_list.copy()
  another_list = my_list[:]
  print(new_list)      # Output: [1, 2, 3]
  print(another_list)  # Output: [1, 2, 3]
  ```
- **Deep Copy**: Using `copy` module for nested lists.
  ```python
  import copy
  nested_list = [[1, 2, 3], [4, 5, 6]]
  deep_copied_list = copy.deepcopy(nested_list)
  print(deep_copied_list)  # Output: [[1, 2, 3], [4, 5, 6]]
  ```

### 12. **Common Use Cases**
- **Iteration**: Looping through elements.
  ```python
  for element in my_list:
      print(element)
  # Output:
  # 1
  # 2
  # 3
  ```
- **Conditional List Comprehensions**:
  ```python
  even_squares = [x**2 for x in range(10) if x % 2 == 0]
  print(even_squares)  # Output: [0, 4, 16, 36, 64]
  ```
- **Filtering**: Using list comprehensions or `filter()` function.
  ```python
  filtered_list = list(filter(lambda x: x % 2 == 0, my_list))
  print(filtered_list)  # Output: [2]
  ```


### 1. **Simple Print**
Print the entire list as it is.
```python
my_list = [1, 2, 3, 4, 5]
print(my_list)
# Output: [1, 2, 3, 4, 5]
```

### 2. **Print Elements Using Loop**
Print each element in the list using a for loop.
```python
for element in my_list:
    print(element)
# Output:
# 1
# 2
# 3
# 4
# 5
```

### 3. **Print Elements Using List Comprehension**
Use a list comprehension to print each element.
```python
[print(element) for element in my_list]
# Output:
# 1
# 2
# 3
# 4
# 5
```

### 4. **Print with Indexes**
Print each element along with its index.
```python
for index, element in enumerate(my_list):
    print(f"Index {index}: {element}")
# Output:
# Index 0: 1
# Index 1: 2
# Index 2: 3
# Index 3: 4
# Index 4: 5
```

### 5. **Print Using Join (For String Lists)**
Join list elements into a single string and print.
```python
string_list = ["apple", "banana", "cherry"]
print(", ".join(string_list))
# Output: apple, banana, cherry
```

### 6. **Print Elements with Separator**
Print list elements separated by a custom separator.
```python
print(*my_list, sep=", ")
# Output: 1, 2, 3, 4, 5
```

### 7. **Pretty Print**
Use the `pprint` module to print lists in a more readable format.
```python
import pprint
nested_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
pprint.pprint(nested_list)
# Output:
# [[1, 2, 3],
#  [4, 5, 6],
#  [7, 8, 9]]
```

### 8. **Print with Custom Formatting**
Use formatted string literals (f-strings) for custom formatting.
```python
for element in my_list:
    print(f"Element: {element}")
# Output:
# Element: 1
# Element: 2
# Element: 3
# Element: 4
# Element: 5
```

### 9. **Print Using Map Function**
Use the `map()` function to print each element.
```python
list(map(print, my_list))
# Output:
# 1
# 2
# 3
# 4
# 5
```

### 10. **Print Nested Lists**
Print each sublist in a nested list.
```python
nested_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for sublist in nested_list:
    print(sublist)
# Output:
# [1, 2, 3]
# [4, 5, 6]
# [7, 8, 9]
```

### 11. **Print Using JSON**
Use the `json` module to print lists in JSON format.
```python
import json
print(json.dumps(my_list))
# Output: [1, 2, 3, 4, 5]
```

### 12. **Print List of Dictionaries**
Print each dictionary in a list of dictionaries.
```python
list_of_dicts = [{'name': 'Alice', 'age': 25}, {'name': 'Bob', 'age': 30}]
for d in list_of_dicts:
    print(d)
# Output:
# {'name': 'Alice', 'age': 25}
# {'name': 'Bob', 'age': 30}
```



### 1. **Simple Print**
Print the type directly.
```python
variable = [1, 2, 3]
print(type(variable))
# Output: <class 'list'>
```

### 2. **Formatted String Literals (f-strings)**
Use f-strings for a more readable format.
```python
variable = 42
print(f'The type of variable is {type(variable)}')
# Output: The type of variable is <class 'int'>
```

### 3. **Using a Loop**
Print the type of each element in a list.
```python
variables = [42, 'hello', 3.14, [1, 2, 3]]
for var in variables:
    print(f'The type of {var} is {type(var)}')
# Output:
# The type of 42 is <class 'int'>
# The type of hello is <class 'str'>
# The type of 3.14 is <class 'float'>
# The type of [1, 2, 3] is <class 'list'>
```

### 4. **List Comprehension**
Use a list comprehension to print the type of each element in a list.
```python
variables = [42, 'hello', 3.14, [1, 2, 3]]
[print(f'The type of {var} is {type(var)}') for var in variables]
# Output:
# The type of 42 is <class 'int'>
# The type of hello is <class 'str'>
# The type of 3.14 is <class 'float'>
# The type of [1, 2, 3] is <class 'list'>
```

### 5. **Using `map()` Function**
Use the `map()` function to print the type of each element.
```python
variables = [42, 'hello', 3.14, [1, 2, 3]]
list(map(lambda var: print(f'The type of {var} is {type(var)}'), variables))
# Output:
# The type of 42 is <class 'int'>
# The type of hello is <class 'str'>
# The type of 3.14 is <class 'float'>
# The type of [1, 2, 3] is <class 'list'>
```

### 6. **Printing Types of Dictionary Values**
Print the type of each value in a dictionary.
```python
dictionary = {'name': 'Alice', 'age': 25, 'height': 5.5, 'hobbies': ['reading', 'swimming']}
for key, value in dictionary.items():
    print(f'The type of {key} is {type(value)}')
# Output:
# The type of name is <class 'str'>
# The type of age is <class 'int'>
# The type of height is <class 'float'>
# The type of hobbies is <class 'list'>
```

### 7. **Function to Print Type**
Create a reusable function to print the type of any variable.
```python
def print_type(variable):
    print(f'The type of the variable is {type(variable)}')

print_type('Hello, world!')
# Output: The type of the variable is <class 'str'>
```

### 8. **Nested Structures**
Print the type of elements in nested structures.
```python
nested_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for sublist in nested_list:
    for element in sublist:
        print(f'The type of {element} is {type(element)}')
# Output:
# The type of 1 is <class 'int'>
# The type of 2 is <class 'int'>
# The type of 3 is <class 'int'>
# The type of 4 is <class 'int'>
# The type of 5 is <class 'int'>
# The type of 6 is <class 'int'>
# The type of 7 is <class 'int'>
# The type of 8 is <class 'int'>
# The type of 9 is <class 'int'>
```

Certainly! Here's an overview of Python conditions and loops, along with examples:

## Python Conditions

### 1. **if Statement**
The `if` statement is used to test a condition and execute a block of code if the condition is `True`.

```python
x = 10
if x > 5:
    print("x is greater than 5")
# Output: x is greater than 5
```

### 2. **if-else Statement**
The `if-else` statement provides an alternative block of code to execute when the condition is `False`.

```python
x = 3
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
# Output: x is not greater than 5
```

### 3. **elif Statement**
The `elif` (else if) statement is used to check multiple conditions.

```python
x = 5
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")
# Output: x is equal to 5
```

### 4. **Nested if Statements**
You can nest `if` statements inside other `if` statements.

```python
x = 10
y = 20
if x > 5:
    if y > 15:
        print("x is greater than 5 and y is greater than 15")
# Output: x is greater than 5 and y is greater than 15
```

### 5. **Logical Operators**
Combine conditions using logical operators `and`, `or`, and `not`.

```python
x = 10
y = 20
if x > 5 and y > 15:
    print("Both conditions are true")
# Output: Both conditions are true

if x > 15 or y > 15:
    print("At least one condition is true")
# Output: At least one condition is true

if not x > 15:
    print("x is not greater than 15")
# Output: x is not greater than 15
```

## Python Loops

### 1. **for Loop**
The `for` loop is used to iterate over a sequence (such as a list, tuple, or string).

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
# Output:
# apple
# banana
# cherry
```

### 2. **range() Function**
The `range()` function generates a sequence of numbers, which is often used with `for` loops.

```python
for i in range(5):
    print(i)
# Output:
# 0
# 1
# 2
# 3
# 4

for i in range(2, 5):
    print(i)
# Output:
# 2
# 3
# 4

for i in range(0, 10, 2):
    print(i)
# Output:
# 0
# 2
# 4
# 6
# 8
```

### 3. **while Loop**
The `while` loop executes as long as a condition is `True`.

```python
i = 1
while i < 5:
    print(i)
    i += 1
# Output:
# 1
# 2
# 3
# 4
```

### 4. **break Statement**
The `break` statement is used to exit a loop prematurely.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
# Output:
# 0
# 1
# 2
# 3
# 4
```

### 5. **continue Statement**
The `continue` statement skips the current iteration and continues with the next one.

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)
# Output:
# 1
# 3
# 5
# 7
# 9
```

### 6. **Nested Loops**
You can use one or more loops inside another loop.

```python
for i in range(3):
    for j in range(2):
        print(f"i = {i}, j = {j}")
# Output:
# i = 0, j = 0
# i = 0, j = 1
# i = 1, j = 0
# i = 1, j = 1
# i = 2, j = 0
# i = 2, j = 1
```

### 7. **else in Loops**
The `else` block after a `for` or `while` loop executes when the loop finishes normally (without encountering a `break` statement).

```python
for i in range(5):
    print(i)
else:
    print("Loop completed")
# Output:
# 0
# 1
# 2
# 3
# 4
# Loop completed

for i in range(5):
    if i == 3:
        break
    print(i)
else:
    print("Loop completed")
# Output:
# 0
# 1
# 2
```


Sure! Here's a comprehensive overview of functions in Python along with examples:

## Python Functions

### 1. **Definition**
A function is a block of organized, reusable code that is used to perform a single, related action.

### 2. **Defining a Function**
Functions are defined using the `def` keyword, followed by the function name, parentheses `()`, and a colon `:`. The code block within every function starts with an indentation.

```python
def my_function():
    print("Hello from a function")
```

### 3. **Calling a Function**
Once a function is defined, you can call it by using its name followed by parentheses.

```python
my_function()
# Output: Hello from a function
```

### 4. **Function Parameters**
Functions can take arguments (parameters) to perform operations with them.

```python
def greet(name):
    print(f"Hello, {name}")

greet("Alice")
# Output: Hello, Alice
```

### 5. **Default Parameter Values**
You can provide default values for parameters. If an argument is not passed during the function call, the default value will be used.

```python
def greet(name="Guest"):
    print(f"Hello, {name}")

greet()
# Output: Hello, Guest
greet("Alice")
# Output: Hello, Alice
```

### 6. **Return Statement**
The `return` statement is used to exit a function and return a value.

```python
def add(a, b):
    return a + b

result = add(3, 4)
print(result)
# Output: 7
```

### 7. **Multiple Return Values**
Functions can return multiple values as a tuple.

```python
def add_and_subtract(a, b):
    return a + b, a - b

result = add_and_subtract(5, 3)
print(result)
# Output: (8, 2)

sum_result, diff_result = add_and_subtract(5, 3)
print(sum_result)  # Output: 8
print(diff_result)  # Output: 2
```

### 8. **Variable-Length Arguments**
- **Arbitrary Positional Arguments**: Use `*args` to pass a variable number of arguments to a function.

  ```python
  def my_function(*args):
      for arg in args:
          print(arg)

  my_function(1, 2, 3)
  # Output:
  # 1
  # 2
  # 3
  ```

- **Arbitrary Keyword Arguments**: Use `**kwargs` to pass a variable number of keyword arguments to a function.

  ```python
  def my_function(**kwargs):
      for key, value in kwargs.items():
          print(f"{key}: {value}")

  my_function(name="Alice", age=25)
  # Output:
  # name: Alice
  # age: 25
  ```

### 9. **Scope and Lifetime of Variables**
- **Local Variables**: Variables declared inside a function are local to that function and are not accessible outside it.
- **Global Variables**: Variables declared outside any function are global and can be accessed inside functions using the `global` keyword.

  ```python
  global_var = "I am global"

  def my_function():
      local_var = "I am local"
      print(local_var)
      print(global_var)

  my_function()
  # Output:
  # I am local
  # I am global

  print(global_var)  # Output: I am global
  # print(local_var)  # Error: NameError: name 'local_var' is not defined
  ```

  ```python
  global_var = "I am global"

  def my_function():
      global global_var
      global_var = "Changed globally"
      print(global_var)

  my_function()
  print(global_var)  # Output: Changed globally
  ```

### 10. **Lambda Functions**
Lambda functions are small anonymous functions defined using the `lambda` keyword. They can have any number of arguments but only one expression.

```python
add = lambda a, b: a + b
print(add(3, 5))
# Output: 8

# Equivalent to:
def add(a, b):
    return a + b
```

### 11. **Docstrings**
A docstring is a string literal that appears as the first statement in a function. It's used to document the function's purpose.

```python
def my_function():
    """This is a docstring explaining the function."""
    print("Hello")

print(my_function.__doc__)
# Output: This is a docstring explaining the function.
```

### 12. **Higher-Order Functions**
Functions that take other functions as arguments or return them as results are known as higher-order functions.

```python
def greet(name):
    return f"Hello, {name}"

def print_greeting(func, name):
    print(func(name))

print_greeting(greet, "Alice")
# Output: Hello, Alice
```

### 13. **Decorators**
Decorators are a way to modify or enhance functions. They are defined with the `@` symbol.

```python
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
# Output:
# Something is happening before the function is called.
# Hello!
# Something is happening after the function is called.
```

