## Python Interview Questions

#### What are Sonar issues?

There are three types of issues: 

Bug – A coding mistake that can lead to an error or unexpected behavior at runtime. 

Vulnerability – A point in your code that's open to attack. 

Code Smell – A maintainability issue that makes your code confusing and difficult to maintain.

#### Pass by reference vs Pass by value

Pass by reference means that you have to pass the function(reference) to a variable which refers that the variable already exists in memory.  Here, the variable( the bucket) is passed into the function directly. The variable acts as a Package that comes with its contents(the objects).

In Pass by value, we pass a copy of actual variables in function as a parameter. Hence any modification on parameters inside the function will not reflect in the actual variable.

#### Class method vs Static method

A class method is a method that is bound to the class and not the object of the class.
They have the access to the state of the class as it takes a class parameter that points to the class and not the object instance.

A static method is also a method that is bound to the class and not the object of the class. This method can’t access or modify the class state. It is present in a class because it makes sense for the method to be present in class.

A class method takes cls as the first parameter while a static method needs no specific parameters. A class method can access or modify the class state while a static method can’t access or modify it. In general, static methods know nothing about the class state. They are utility-type methods that take some parameters and work upon those parameters. On the other hand class methods must have class as a parameter.
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
 
    # a class method to create a Person object by birth year.
    @classmethod
    def fromBirthYear(cls, name, year):
        return cls(name, date.today().year - year)
 
    # a static method to check if a Person is adult or not.
    @staticmethod
    def isAdult(age):
        return age > 18
```
#### List

List items are ordered, changeable, and allow duplicate values.

#### Tuple

Tuple items are ordered, unchangeable, and allow duplicate values.

#### Set

Set items are unordered, unchangeable, and do not allow duplicate values.

#### Dictionary

Dictionary items are ordered, changeable, and does not allow duplicates. Dictionary items are presented in key:value pairs, and can be referred to by using the key name.

#### What is Python?

Python is a high-level, interpreted, general-purpose programming language. Being a general-purpose language, it can be used to build almost any type of application with the right tools/libraries. Additionally, python supports objects, modules, threads, exception-handling, and automatic memory management which help in modelling real-world problems and building applications to solve these problems.

#### Type-checking

Typing refers to type-checking in programming languages. In a strongly-typed language, such as Python, "1" + 2 will result in a type error since these languages don't allow for "type-coercion" (implicit conversion of data types). On the other hand, a weakly-typed language, such as Javascript, will simply output "12" as result. Type-checking can be done at two stages -

Static - Data Types are checked before execution.

Dynamic - Data Types are checked during execution.

#### Python is an interpreted language

Python is an interpreted language, executes each statement line by line and thus type-checking is done on the fly, during execution. Hence, Python is a Dynamically Typed Language. An Interpreted language executes its statements line by line. Languages such as Python, Javascript, R, PHP, and Ruby are prime examples of Interpreted languages. Programs written in an interpreted language runs directly from the source code, with no intermediary compilation step.

#### Python Enhancement Proposal

PEP stands for Python Enhancement Proposal. A PEP is an official design document providing information to the Python community, or describing a new feature for Python or its processes.

#### Scope

Every object in Python functions within a scope. A scope is a block of code where an object in Python remains relevant. Namespaces uniquely identify all the objects inside a program. However, these namespaces also have a scope defined for them where you could use their objects without any prefix. A few examples of scope created during code execution in Python are as follows:

#### Local, Global, Module-level scope, and Outermost scope

A local scope refers to the local objects available in the current function.

A global scope refers to the objects available throughout the code execution since their inception.

A module-level scope refers to the global objects of the current module accessible in the program.

An outermost scope refers to all the built-in names callable in the program.

#### Lists vs Tuples

Lists and Tuples are both sequence data types that can store a collection of objects in Python. The objects stored in both sequences can have different data types. Lists are represented with square brackets ['sara', 6, 0.19], while tuples are represented with parantheses ('ansh', 5, 0.97). 

The key difference between the two is that while lists are mutable, tuples on the other hand are immutable objects. This means that lists can be modified, appended or sliced on the go but tuples remain constant and cannot be modified in any manner.

#### Pass keyword

The pass keyword represents a null operation in Python. It is generally used for the purpose of filling up empty blocks of code which may execute during runtime but has yet to be written.

#### Modules vs Packages

Modules, in general, are simply Python files with a .py extension and can have a set of functions, classes, or variables defined and implemented. They can be imported and initialized once using the import statement. If partial functionality is needed, import the requisite classes or functions using from foo import bar.

Packages allow for hierarchial structuring of the module namespace using dot notation. As, modules help avoid clashes between global variable names, in a similar manner, packages help avoid clashes between module names.

Creating a package is easy since it makes use of the system's inherent file structure. So just stuff the modules into a folder and there you have it, the folder name as the package name. Importing a module or its contents from this package requires the package name as prefix to the module name joined by a dot.

#### Global variables

Global variables are public variables that are defined in the global scope. To use the variable in the global scope inside a function, we use the global keyword.

#### Protected vs Private attributes

Protected attributes are attributes defined with an underscore prefixed to their identifier eg. _sara. They can still be accessed and modified from outside the class they are defined in but a responsible developer should refrain from doing so.

Private attributes are attributes with double underscore prefixed to their identifier eg. __ansh. They cannot be accessed or modified from the outside directly and will result in an AttributeError if such an attempt is made.

#### Self

Self is used to represent the instance of the class. With this keyword, you can access the attributes and methods of the class in python. It binds the attributes with the given arguments.

#### __init__

__init__ is a contructor method in Python and is automatically called to allocate memory when a new object/instance is created. All classes have a __init__ method associated with them. It helps in distinguishing methods and attributes of a class from local variables.

#### Break vs Continue statement

The break statement terminates the loop immediately and the control flows to the statement after the body of the loop.

The continue statement terminates the current iteration of the statement, skips the rest of the code in the current iteration and the control flows to the next iteration of the loop.

#### Unit test

Unit test is a unit testing framework of Python. Unit testing means testing different components of software separately. Imagine a scenario, you are building software that uses three components namely A, B, and C. Now, suppose your software breaks at a point time. How will you find which component was responsible for breaking the software? Maybe it was component A that failed, which in turn failed component B, and this actually failed the software. There can be many such combinations. This is why it is necessary to test each and every component properly so that we know which component might be highly responsible for the failure of the software.

#### Documentation string

Documentation string or docstring is a multiline string used to document a specific code segment. The docstring should describe what the function or method does.

#### Slicing

As the name suggests, ‘slicing’ is taking parts of. Syntax for slicing is [start : stop : step] start is the starting index from where to slice a list or tuple, stop is the ending index or where to sop, step is the number of steps to jump. Default value for start is 0, stop is number of items, step is 1. Slicing can be done on strings, arrays, lists, and tuples.

#### Arrays vs Lists

Arrays in python can only contain elements of same data types i.e., data type of array should be homogeneous. It is a thin wrapper around C language arrays and consumes far less memory than lists.

Lists in python can contain elements of different data types i.e., data type of lists can be heterogeneous. It has the disadvantage of consuming large memory.

#### Memory management in Python

Memory management in Python is handled by the Python Memory Manager. The memory allocated by the manager is in form of a private heap space dedicated to Python. All Python objects are stored in this heap and being private, it is inaccessible to the programmer. Additionally, Python has an in-built garbage collection to recycle the unused memory for the private heap space.

#### Namespace in Python

A namespace in Python ensures that object names in a program are unique and can be used without any conflict. Python implements these namespaces as dictionaries with 'name as key' mapped to a corresponding 'object as value'. This allows for multiple namespaces to use the same name and map it to a separate object. A few examples of namespaces are as follows:

#### Local vs Global Namespace

Local Namespace includes local names inside a function. the namespace is temporarily created for a function call and gets cleared when the function returns.

Global Namespace includes names from various imported packages/ modules that are being used in the current project. This namespace is created when the package is imported in the script and lasts until the execution of the script.

#### Scope resolution

Sometimes objects within the same scope have the same name but function differently. In such cases, scope resolution comes into play in Python automatically. A few examples of such behavior are: Python modules namely 'math' and 'cmath' have a lot of functions that are common to both of them - log10(), acos(), exp() etc. To resolve this ambiguity, it is necessary to prefix them with their respective module, like math.exp() and cmath.exp().

#### Decorators in Python

Decorators in Python are essentially functions that add functionality to an existing function in Python without changing the structure of the function itself.

#### list comprehension

Python comprehensions, like decorators, are syntactic sugar constructs that help build altered and filtered lists, dictionaries, or sets from a given list, dictionary, or set. Using comprehensions saves a lot of time and code that might be considerably more verbose (containing more lines of code).
```python
my_list = [2, 3, 5, 7, 11]

squared_list = [x**2 for x in my_list]    # list comprehension
# output => [4 , 9 , 25 , 49 , 121]

squared_dict = {x:x**2 for x in my_list}    # dict comprehension
# output => {11: 121, 2: 4 , 3: 9 , 5: 25 , 7: 49}
```
#### Lambda function

Lambda is an anonymous function in Python, that can accept any number of arguments, but can only have a single expression. It is generally used in situations requiring an anonymous function for a short time period.
```python
mul = lambda a, b : a * b
print(mul(2, 5))    # output => 10
```
#### Aassignment statement

In Python, the assignment statement (= operator) does not copy objects. Instead, it creates a binding between the existing object and the target variable name. To create copies of an object in Python, we need to use the copy module. Moreover, there are two ways of creating copies for the given object using the copy module -

#### Shallow Copy vs Deep Copy

Shallow Copy is a bit-wise copy of an object. The copied object created has an exact copy of the values in the original object. If either of the values is a reference to other objects, just the reference addresses for the same are copied.

Deep Copy copies all values recursively from source to target object, i.e. it even duplicates the objects referenced by the source object.
```python
from copy import copy, deepcopy

list_1 = [1, 2, [3, 5], 4]

## shallow copy
list_2 = copy(list_1) 
list_2[3] = 7
list_2[2].append(6)
list_2    # output => [1, 2, [3, 5, 6], 7]
list_1    # output => [1, 2, [3, 5, 6], 4]

## deep copy
list_3 = deepcopy(list_1)
list_3[3] = 8
list_3[2].append(7)
list_3    # output => [1, 2, [3, 5, 6, 7], 8]
list_1    # output => [1, 2, [3, 5, 6], 4]
```
#### xrange() and range()

xrange() and range() are quite similar in terms of functionality. They both generate a sequence of integers, with the only difference that range() returns a Python list, whereas, xrange() returns an xrange object.

#### Pickling vs Unpickling

Pickling is the name of the serialization process in Python. Any object in Python can be serialized into a byte stream and dumped as a file in the memory. The process of pickling is compact but pickle objects can be compressed further. Moreover, pickle keeps track of the objects it has serialized and the serialization is portable across versions. The function used for the above process is pickle.dump().

Unpickling is the complete inverse of pickling. It deserializes the byte stream to recreate the objects stored in the file and loads the object to memory. The function used for the above process is pickle.load().

#### Generators

Generators are functions that return an iterable collection of items, one at a time, in a set manner. Generators, in general, are used to create iterators with a different approach. They employ the use of yield keyword rather than return to return a generator object.
```python
## generate fibonacci numbers upto n

def fib(n):
   p, q = 0, 1
   while(p < n):
       yield p
       p, q = q, p + q
x = fib(10)    # create generator object 
 
## iterating using __next__(), for Python2, use next()

x.__next__()    # output => 0
x.__next__()    # output => 1
x.__next__()    # output => 1
x.__next__()    # output => 2
x.__next__()    # output => 3
x.__next__()    # output => 5
x.__next__()    # output => 8
x.__next__()    # error
 
## iterating using loop

for i in fib(10):
   print(i)    # output => 0 1 1 2 3 5 8
```
#### help() function

help() function in Python is used to display the documentation of modules, classes, functions, keywords, etc. If no parameter is passed to the help() function, then an interactive help utility is launched on the console.

#### dir() function

dir() function tries to return a valid list of attributes and methods of the object it is called upon. It behaves differently with different objects, as it aims to produce the most relevant data, rather than the complete information.

#### .py vs .pyc file

.py files contain the source code of a program. Whereas, .pyc file contains the bytecode of your program.

#### In Python, arguments are passed by reference

Pass by value: Copy of the actual object is passed. Changing the value of the copy of the object will not change the value of the original object.

Pass by reference: Reference to the actual object is passed. Changing the value of the new object will change the value of the original object.

In Python, arguments are passed by reference, i.e., reference to the actual object is passed.
```python
def appendNumber(arr):
   arr.append(4)

arr = [1, 2, 3]

print(arr)  #Output: => [1, 2, 3]

appendNumber(arr)

print(arr)  #Output: => [1, 2, 3, 4]
```
#### Iterator

An iterator is an object. It remembers its state i.e., where it is during iteration. __iter__() method initializes an iterator. It has a __next__() method which returns the next item in iteration and points to the next element.

#### Explain how to delete a file in Python?

Use command os.remove(file_name)
```python
import os
os.remove("ChangedFile.csv")
print("File Removed!")
```
#### split() vs join()

You can use split() function to split a string based on a delimiter to a list of strings.

You can use join() function to join a list of strings based on a delimiter to give a single string.
```python
string = "This is a string."
string_list = string.split(' ') #delimiter is ‘space’ character or ‘ ‘
print(string_list) #output: ['This', 'is', 'a', 'string.']
print(' '.join(string_list)) #output: This is a string.
```
#### *args vs **kwargs

*args is a special syntax used in the function definition to pass variable-length arguments. “*” means variable length and “args” is the name used by convention.

**kwargs is a special syntax used in the function definition to pass variable-length keyworded arguments. Here, also, “kwargs” is used just by convention. You can use any other name.

#### Negative indexes

Negative indexes are the indexes from the end of the list or tuple or string. Arr[-1] means the last element of array Arr[]

#### Inheritance

Inheritance gives the power to a class to access all attributes and methods of another class. It aids in code reusability and helps the developer to maintain applications without redundant code. The class inheriting from another class is a child class or also called a derived class. The class from which a child class derives the members are called parent class or superclass. Python supports different kinds of inheritance, they are:

Single Inheritance: Child class derives members of one parent class.

![image](https://user-images.githubusercontent.com/97865583/195967563-e82c2198-08e5-4678-84e4-4dd47b81dc4d.png)
```python
# Parent class
class ParentClass:
    def par_func(self):
         print("I am parent class function")

# Child class
class ChildClass(ParentClass):
    def child_func(self):
         print("I am child class function")
```
Multi-level Inheritance: The members of the parent class, A, are inherited by child class which is then inherited by another child class, B. The features of the base class and the derived class are further inherited into the new derived class, C. Here, A is the grandfather class of class C.

![image](https://user-images.githubusercontent.com/97865583/195967570-d667000f-00ce-436d-a2b0-26f85b49aa96.png)

Multiple Inheritance: This is achieved when one child class derives members from more than one parent class. All features of parent classes are inherited in the child class.

![image](https://user-images.githubusercontent.com/97865583/195967573-86852de7-fdf0-4cba-98f8-af8e4507ce22.png)

Hierarchical Inheritance: When a parent class is derived by more than one child class, it is called hierarchical inheritance.

![image](https://user-images.githubusercontent.com/97865583/195967576-03f1ea67-b7b0-430f-95bc-f5ead6fccce1.png)

#### Access specifiers

Python does not make use of access specifiers specifically like private, public, protected, etc. However, it does not derive this from any variables. It has the concept of imitating the behaviour of variables by making use of a single (protected) or double underscore (private) as prefixed to the variable names. By default, the variables without prefixed underscores are public.

#### Is it possible to call parent class without its instance creation?

Yes, it is possible if the base class is instantiated by other child classes or if the base class is a static method.

#### Empty class

An empty class does not have any members defined in it. It is created by using the pass keyword (the pass command does nothing in python).

#### Finalize method

Finalize method is used for freeing up the unmanaged resources and clean up before the garbage collection method is invoked. This helps in performing memory management tasks.

#### How will you check if a class is a child of another class?

This is done by using a method called issubclass() provided by python. The method tells us if any class is a child of another class by returning true or false accordingly.

#### Pandas

Pandas is an open-source, python-based library used in data manipulation applications requiring high performance.

#### Dataframe

A dataframe is a 2D mutable and tabular structure for representing data labelled with axes - rows and columns.
