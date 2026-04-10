# Meeting Three Agenda
Agenda for meeting three 4/10/2026

Topics to be covered:

- Python Basics
    - Interpreted vs Compiled languages
    - Python Interactive Interpreter
    - Python as a Calculator 
    - Variables and Data Types
    - Everything is an Object
    - Variable References
    - Comments
    - Control Flow. Condtionals and loops
    - Functions

## Python Basics
See org README for Python Overview

### Interpreted vs Compiled Languages
When we program in a high-level programming language (such as Python), the code that we write is not automatically understandable by the computer we are working on. That feels like a very strange thing, as we typically think of code as being as close to "computer language" as we can get, but that's actually not quite true. Before any of the code we write can be used, it has to be translated into a machine readable format called machine code. There are two main ways that this can be achieved. That is, through the use of either a compiler or an interpreter.

Compilers work by reading the entirety of your written code, analyzing said code, and then creating a completely separate file containing machine code, which can be executed at any time, without access to the original source code.

Interpreters, on the other hand, read through your code line-by-line, executing the code in a series of sequential steps. This process happens every single time you execute your code, unlike with a compiler, where once the code is compiled, it can be run directly without having to do any extra translation.

You can think of compilers and interpreters as though you are trying to read a book in a different language than the one you understand. In the example of a compiled language, this would be equivalent to having a translator read and then translate the whole book, and giving you the translated copy after they are done. You can read it as much as you want, with no extra work needed from you. With an interpreted language, on the other hand, this would be like having a translator read the book to you line-by-line. Once the translator is done reading the book, there is no way for you to read it again without having the translator read the entire book to you once more.

Putting it this way, it might seem as if there is no advantage to having a programming language be interpreted. Why would we even want a language that requires the computer to re-interpret it every single time we execute its code? Or vice-versa, why would we ever want to choose a compiled language over an interpreted language? As with many things in life, each methodology has its own strengths and weaknesses.

In general, interpreted languages are going to have a much smoother development cycle compared to compiled languages. This is due to the fact that any time you make changes to your code in a compiled language, you will have to re-compile before you are able to run that code, and especailly as projects grow in size, compilation can become a very laborious task. With an interpreted language, however, there is no re-compilation that needs to be made, allowing you to run your code instantly after any changes you make.

With this, however, comes the trade off of execution speed. Compiled langauges are typically much faster when it comes to raw computation as they don't have the extra overhead of needing to do on-the-fly translation like interpreted languages do.

There are of coure more reasons, but development speed and execution speed are the two biggest reasons why one might make the choice of using an interpreted or compiled programming language. If you are interested, here is a summary of a few more common trade-offs between compiled and interpreted programming languages:

| Feature           | Interpreted                       | Compiled                                         |
|-------------------|-----------------------------------|--------------------------------------------------|
| Execution Speed   | Slower (translation overhead)     | Faster (running direct machine code)             |
| Development Cycle | Fast (Run immediately after edit) | Slower (Need to re-compile after changes)        |
| Portability       | Runs anywhere with interpreter    | Low Portability (binaries are platform specific) |
| Debugging         | Easier Debugging                  | Less descriptive error messages                  |

### Python Interactive Interpreter
To run Python code, we can either create a Python file, write all of our code in that file, and then run it with the ``python3 "your_file_name_here"`` command, or we can invoke the interactive python interpreter / REPL (Read-Eval-Print Loop) and write code line by line in the command line. We will start with the second method for now. To invoke the interactive Python intepreter, simply run the ``python3`` command in your terminal, and an interactive prompt will pop up where you can then write Python code.

The Python REPL is what we will be using for the time being, but it is not the main place where you will be running Python code in the future. The Python REPL can be very useful for on-the-fly programming, and as you learn Python, it can be a convenient way to test out how a certain object behaves.

### Python as a Calculator
Now that we have our environment fully set up and we know how to run the Python REPL, let's get started with writing some actual python code!

Begin by starting the Python REPL with the ``python3`` command we learned earlier. You should now see the primary prompt, ``>>>``. This meas that the Python REPL is now ready to take Python commands.

You can use the Python REPL as a calculator. Just type an expression and hit enter, and the Python interpreter will print out a value. EX:

```
>>> 2+2
4
>>> 50-5*6
20
>>> (50-5*6)/4
5.0
>>> 8/5 # division always returns a floating-point number
1.6
```

Here are some useful operations to know when doing math in Python:

| Operator | Name           | Example | Description                                                                                                                    |
|----------|----------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| +        | Plus           | x + y   | Adds two given values together                                                                                                 |
| -        | Minus          | x - y   | Subtracts two given values                                                                                                     |
| *        | Multiplication | x * y   | Multiplies two given values                                                                                                    |
| /        | Division       | x / y   | Divides value x by value y (NOTE: Division always returns a floating point number)                                             |
| %        | Modulus        | x % y   | Returns the remainder of value x divided by value y (EX: 5 % 2 = 1)                                                            |
| **       | Exponentiation | x ** y  | Raises value x to the power of value y (EX: 2 ** 4 = 16)                                                                       |
| //       | Floor Division | x // y  | Returns the rounded down result of value x divided by value y (EX: 5 // 2 = 2)(NOTE: Floor division always returns an integer) |


### Variables and Data Types
Variables are special containers that point to an object stored somewhere in memory.

In Python, you can create a variable by assigning it a value using the ``=`` operator.

Example:

```
>>> x = 2
>>> y = 4
>>> z = 'Hello'
>>> print(x)
2
>>> print(y)
4
>>> print(z)
Hello
```

Data types are a very important concept in programming. Variables can store data of different types, and each differnt type can do different things. Python has the following data types built in:

| Type       | Description                                                                                                                    | Example                                             |
|------------|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| str        | Immutable string of Unicode text                                                                                               | "foo"                                               |
| int        | Integers                                                                                                                       | 7, 15, -3, 123456789                                |
| float      | Floating point numbers. Numbers with decimals or written in scientific notation                                                | 3.2, 5.84321, 1.23e10                               |
| complex    | Complex numbers. Written as real + imaginary j                                                                                 | 3 + 5j                                              |
| list       | mutable, ordered collection that can hold multiple different types (including other lists)                                     | [10, "foo", 3.2, [1, 2]]                            |
| tuple      | Immutable, ordered collection that can hold multiple different types. Often used for returning multiple values from a function | (10, "foo", 3.2, [1,2])                             |
| range      | Immutable sequence of numbers, commonly used in for loops. Created using the range() constructor                               | range(10), range(1, 10), range(1, 10, 2)            |
| dict       | Mutable collection that stores data in unique key-value pairs                                                                  | {"name" : "Bob", "age": 99}                         |
| set        | Unordered, mutable collection of unique items with no duplicates. Only immutable data types may be stored                      | {1, 2, 3}                                           |
| frozenset  | Immutable version of a set. Constructor takes iterable as argument                                                             | frozenset([1, 2, 3])                                |
| bool       | Boolean. Represents logical truth values. Either True or False                                                                 | True, False                                         |
| bytes      | Immutable sequence of single bytes.                                                                                            | b"hello", bytes("hello", "utf-8"), "hello".encode() |
| bytearray  | Mutable version of bytes                                                                                                       | bytearray("hello", "utf-8")                         |
| memoryview | I can't even lie, I have no idea wat this is                                                                                   |                                                     |
| NoneType   | Indicates the absence of a value. Represented by the keyword None                                                              | None                                                |

Unlike in many other languages, Python variables do not have a set data type. A variable's data type can change upon reassignment. This is because variables in Python do not store any type information, but rather point to pre-existing objects in memory, which store the information about their type in the actual objects themselves. For example, the following is allowed in Python:

```
>>> a = 3
>>> print(a)
3
>>> a = "foo"
>>> print(a)
foo
```

In a language such as C, this would not be allowed as the variable ``a`` was initially initialized as an int type.

### Everything is an Object
In Python, everything is an object. An object in programming is a self-contained unit of internal data and functions that operate on that data. In Python, all objects must have a type and some form of internal data. 

This way of treating everything as a function can be very useful when programming. It gives you a guarantee that no matter what you are working with, whether it be a number, string, function, class, module, etc., it can all be treated consistently. You can assign any entity to a variable, pass it to a function, store it in a list or dictionary.

### Variable References
Going back to variables, it is important to understand exactly how and when they point to and make copies of the data they are assigned to. When you assign a variable to some data in Python, what you are doing is actually creating a **reference** to that data. This is important to recognize, as it can sometimes lead to unintended effects if you are not careful.

Take the following scenario for example:

Assign variable ``a`` to a list
```
>>> a = [1, 2, 3, 4, 5]
```

Now let's say you want to assign variable ``b`` to that same list, so you set ``b = a``
```
>>> b = a
>>> print(b)
[1, 2, 3, 4, 5]
```

Now let's go ahead and remove the last element from variable ``b`` and see what happens to variable ``a``
```
>>> b.pop()
5
>>> print(a)
[1, 2, 3, 4]
```

We can see that by removing an element from the list referenced by variable ``b``, we also removed the last element of the list referenced by variable ``a`` completely by accident!

What happened here is when we set ``b = a``, Python did not actually make a copy of the list at variable ``a`` and assign it to variable ``b``, but rather, it made variable ``b`` reference the same exact object as varaible ``a``, the original list ``[1, 2, 3, 4, 5]``. So when we removed the last element from variable ``b``, we modified the original list that variable ``a`` was still pointing to.

### Comments
You may find yourself wanting to leave comments in your code while you program (and you absolutely should!). In Python, you may comment out the rest of a line by using the ``#`` symbol. Anything after the pound symbol will be ignored by the Python interpreter. 

Example:

```
for i in range(10):
    # This is a comment.
    # Comments have no effect on how the code will be executed, 
    # They are simply there to leave a note to whoever may read this code in the future.
    print(i)
```

Comments are an excellent way of explaining to your future self, as well as to other people who may read your code what exactly is going on through each step of your code. It is very important to leave regular (but not overwhelming) comments to improve the readability and maintainbaility of your code.

You can also create multiline comments using triple quoted strings (`` '''    ''' ``), although it is recommended to use the ``#`` symbol instead as triple quotes are technically string literals and not comments, and have the potential to cause issues if used incorrectly.

Example:

```
for i in range(10):
    print(i) 

    '''
    This is
    A multiline
    comment
    '''
```

### Control Flow
In Python, there are several ways to control the flow of logic within your code. This is what's known as *control flow*.

#### if statements
Probably the biggest way of doing this is through the use of the ``if`` statement. As the name implies, the ``if`` statement checks whether a given condition is ``True``, and if so, then it runs the code block immediately following the statement.

Here is an example of an ``if`` statement being used:

```
x = 8
if (x % 2 == 0):
    print("x is divisible by 2")
```

The above code assigns a value of 8 to variable ``x``, and then proceeds to check if the remainder of x divided by 2 (using the modulus operator) is equal to 0. If it is, then it prints the statement "x is divisible by 2".

You can also chain an ``if`` statement with an ``elif`` or an ``else`` statement that will run other code if the statement evaluates to ``False``.

Example of ``elif`` and ``else`` being used in conjuction with an ``if`` statement:

```
x = 8
if (x % 3 == 0):
    print("x is divisible by 3")
elif (x % 5 == 0):
    print("x is divisible by 5")
else:
    print("x is neither divisible by 3 nor 5")
```

If any of the if/elif statements evaluate to ``True`` at any point, then any following elif/else statements will not be reached.

You may have noticed that when checking if any of the statements are equal to 0, we used a double equal sign ``==`` instead of a single equal sign ``=``. In Python, a single equal sign represents the assigning of a value to a variable, whereas a double equal sign is used to compare values and check for equality. 

In fact, there are several ways we can compare two values. They are as follows:

| Operation  | Description                                             | Example             |
|------------|---------------------------------------------------------|---------------------|
| a == b     | True if a equals b                                      | 1 == 1 returns True |
| a != b     | True if a is not equal to b                             | 2 != 1 returns True |
| a < b      | True if a is less than b                                | 2 < 3 returns True  |
| a <= b     | True if a is less than or equal to b                    | 2 <= 2 returns True |
| a > b      | True if a is greater than b                             | 3 > 2 returns True  |
| a >= b     | True if a is greater than or equal to b                 | 2 >= 2 returns True |
| a is b     | True if a and b reference the same Python object        |                     |
| a is not b | True if a and b do not reference the same Python object |                     |

#### for loops
``for`` loops allow you to iterate over a collection/iterator. The standard syntax for a ``for`` loop is:

```
for value in sequence:
    # do something
```

We generally use for loops with the ``range()`` constructor. This constructor can be used in 3 different ways:

The first way is to pass one argument inside the parenthesis. This argument represents the stopping point 
