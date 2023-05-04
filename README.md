## List comprehensions: A concise way to create lists using a single line of code.
```
squares = [x ** 2 for x in range(10)]
```
### USE CASE - You have a list of numbers, and you want to create a new list containing the squares of only the even numbers in the original list.
#### Traditional
```
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
even_squares = []

for num in numbers:
    if num % 2 == 0:
        even_squares.append(num ** 2)

print(even_squares)
```
#### Using List Comprehension
```
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
even_squares = [num ** 2 for num in numbers if num % 2 == 0]

print(even_squares)

```

### Lambda functions: Anonymous, single-expression functions.
```
add = lambda x, y: x + y
```

### Decorators: Functions that modify or extend the behavior of other functions.
```
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
```

### Generators: Functions that allow you to iterate through a sequence of values without creating a list or other collection in memory.
```
def fibonacci(limit):
    a, b = 0, 1
    while a < limit:
        yield a
        a, b = b, a + b

for num in fibonacci(10):
    print(num)
```

### Context managers: A convenient way to manage resources like file handles or network connections.
```
with open("file.txt", "r") as f:
    content = f.read()
```

### Exception handling: The process of catching and managing errors in a controlled manner.
```
try:
    result = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

### Multithreading and multiprocessing: Techniques for executing code concurrently or in parallel to take advantage of multiple CPU cores or to improve performance.
```
import threading

def print_numbers():
    for i in range(10):
        print(i)

thread = threading.Thread(target=print_numbers)
thread.start()
thread.join()
```
