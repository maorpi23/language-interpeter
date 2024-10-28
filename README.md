# language-interpeter
## Overview
This project is a custom interpreter implemented in Python that supports a variety of arithmetic operations, logical operations, and programming constructs such as conditionals, loops, lists, dictionaries, and functions. The interpreter uses Python's Abstract Syntax Tree (AST) module to parse and evaluate code, making it capable of interpreting code similar to Python.

## Features
- **Arithmetic and Comparison Operators**: Supports addition, subtraction, multiplication, division, modulus, exponentiation, and floor division. Comparison operators like `>`, `<`, `>=`, `<=`, `==`, and `!=` are also supported.
- **Logical Operators**: `and`, `or`, and `not` for complex logical conditions.
- **Data Structures**: Allows use of lists, tuples, dictionaries, and slicing for indexing and subsetting.
- **Control Structures**: Includes support for `if-else` statements, `for` loops, and `while` loops.
- **Function Calls**: Built-in functions (e.g., `print`, `len`, `sum`, etc.) and custom functions are available.
- **Custom Functions**: `replace_char`, `isUpper`, `isLower`, and various arithmetic functions like `add`, `sub`, `mul`, and `div`.

## Key Components
### Interpreter Class
The core of the interpreter is built within the `Interpreter` class, which has the following methods:

- `tokenize_code`: Parses code to identify constants, variable names, operators, comparisons, logical operations, assignments, loops, and function calls.
- `eval`: Evaluates nodes in the AST, handling constants, variable names, arithmetic operations, comparisons, assignments, loops, and function calls.
- `repl`: A REPL (Read-Eval-Print Loop) for interactive code input and execution.

## Setup and Usage
### Requirements
- Python 3: The interpreter relies on Python 3's `ast` module.
- Math Module: For advanced mathematical functions like square roots and constants.

### Running the interpeter
1. Clone or Download the Repository: Clone the repository or download the files to your local machine.

2. Run the Interpreter: To start the interpreter, run the `interpreter.py` script. It will enter REPL (Read-Eval-Print Loop) mode where you can type and execute code interactively.
Type `exit` and press Enter to exit the REPL.

## Example Usage
```
# Basic arithmetic and variable assignment
x = 10
y = 5
z = x + y * 2

# Comparison and conditional statements
if z > 20:
  print("z is greater than 20")
else:
  print("z is not greater than 20")

# Lists and list operations
numbers = [1, 2, 3, 4, 5]
squares = []
for num in numbers:
  squares.append(num ** 2)
print("Squares:", squares)

# Dictionary
person = {"name": "Alice", "age": 30}
print("Person:", person)

# String operations
greeting = "Hello, " + person["name"] + "!"
print(greeting)

# Built-in functions
print("Length of squares:", len(squares))
print("Sum of squares:", sum(squares))

# Math operations
radius = 5
area = math.pi * radius ** 2
print("Circle area:", area)

# Slicing
print("First three squares:", squares[:3])

# Boolean operations
is_adult = person["age"] >= 18 and person["name"] != ""
print("Is adult:", is_adult)

# Tuple
coordinates = (10, 20)
print("Coordinates:", coordinates)

# Advanced math
print("Square root of 16:", math.sqrt(16))

# Handling potential None values
empty_list = []
print("First element of empty list:", empty_list[0] if empty_list else None)

# Attribute access on None
none_value = None
print("Attribute of None:", none_value.some_attribute if none_value is not None else None)

# Basic list operations
numbers = [1, 2, 3, 4, 5]

# Remove an item from the list
REMOVE numbers[2]

print(numbers)

original_string = "hello world"
new_string = replace_char(original_string, "l", "x")
print(new_string)  # Output: hexxo worxd

text = "Hello World"
print("Is 'Hello' uppercase?", isUpper("Hello"))
print("Is 'hello' lowercase?", isLower("hello"))
print("Is 'HELLO' uppercase?", isUpper("HELLO"))
print("Is 'WORLD' lowercase?", isLower("WORLD"))
```
