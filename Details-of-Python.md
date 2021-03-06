# History of Python
Python was implemented in late 1989. The language was invented to be a language capable of exception handling and to interact with the Amoeba operation system. In 2000, the Python 2.0 was introduced to include a cycle-detecting garbage collector, support for Unicode, and for a shift to a community-based development process.

The language was created to replace the language ABC. It has become popular on its own though due its easability in reading, object-orientation, structured programming, functional programming, and ability to be used as a scripting language.

# Unique Features of Python
While the Python language has evolved over the years by taking in aspects of other languages, it does have a few specific features. First, Python explicitly passes self as a form of a parameter to object member functions. The language also combines things such as data entry - prompting the user for entry and reading it in - to a simple function called 'input()'. Finally, the language incorporates a large number of datatypes such as ordereddict, namedtupke, array, list, tuple, diction, etc; making it popular in the scientific community. 

# Name Space of Python
Name spaces are implemented in Python by using a Dictionary -- Key to value lookup. Some examples of a Python name space are **global names** of a module, **local names** a function, **built-in names** such as abs() and cmp(). The name spaces exist only in the scope they are created.

# Types
Python accomodates numeric types such as int, long and float. It also includes some built-in data types such as dictionary, list, set, and tuple. The determination of value or reference in Python is difficult as everything is an object in this language. This means that while the language is passed by value, the value is a reference, or pointer, to the specific object. An easier way to look at values and references in Python is to think of them just names, with the mutable or immmutatable being important. If the passed names are mutatable, they can be rebranded to be anything they need. 

Types in Python can be created or altered. In fact, everything object in Python can be extended to include addictional functions or change the default functions. 

# Classes
Classes in Python are created by using the 'class' keyword, the class name, and then a colon before inserting everything needed in the class.
For example:
```
class Car:
  def drive(self):
    print("This car is being driven.")
```
Creates a car class with the drive function.

To instantiate a new instance of the class, the user would create a variable and assign it to the class;:
```
x = Car()
```
This calls the '__init__()' function on the class. This function can be extended if the creator wanted the instance to do additional features, such as assign variable or run additional functions, in the instantiation period.
To de-initialize a class in Python the developer can use the close function on an object. This will delete the reference to the object. If the developer wanted to reuse the object in a pool, the developer could modify the close function to just erase the data inside. 

# Instance reference name in data type (class)
Python uses the 'self' keyword to reference the name of the data type. Python is special in that self doesn't need to be added to the signature as each object recognizes the current instance as 'self'

# Properties
Using 'getters' and 'setters' aren't typically used in Python but can be utilized. The typical way is just to use plain attributes to pass the information and then to dereference the attribute using the 'del' function.
However, getters and setters can be added to the code to make it consistent to other programming. These can be added using the 'property' decorator without altering the original code
```
class obj:
  @property
  def attribute(self):
    return self.__attribute
  @attribute.setter
  def attribute_setter(self, value):
    self.__attribute = value
 ```
 
 # Interfaces / protocols
 Python doesn't use interfaces or protocols, as it uses the idea of duck-typing. Duck-typing is applying the idea of "if it looks like a duck, it must be a duck", in programming. This comparison is done at runtime and is handled by the type checking. Generally if the object type and methods work, the interface will work; else a exception will be thrown.
 
# Inheritance / extension
Inheritance in Python is handled by inluding the parent in the parenthesis after a class declaration.
```
class Person(object):
  def foo(self):
  ...
class Waiter(Person):
  ...
```
In this example, Person is inheriting from Object and Waiter is inheriting from Person. A waiter can use the Person's foo method by using "super().foo()" or by calling it as "Person.greet(self)" from Waiter.

# Reflection
Reflection refers to the ability of the language to tell attributes about objects that might be passed as parameters to a function. Python is dynamically typed so this ability is important. Using "type(obj)" will return the type of the object in question. Python also has other commands available to assist in reflection. Python uses the "Isinstance()" command to test if an object is an instance of a type or class. The "getattr()" command can return a value of an attribute of an object.

# Memory Management
Python stores all objects and data structures in a private heap. This heap is controlled by the Python memory manager, which deals with sharing, segmentation, preallocation, and cachine.
In addition, Python uses reference counting and garbage collection to maintain memory usage. 
#### Reference Counting 
Reference counting is the idea that an object needs to be maintained when the count of that object is greater than 0. 
#### Garbage Collection
Garbage collection is automatic in Python and happens when the code can no longer 'reach' an object. Examples of garbage collection are when "del" is used on an object or when an object is set equal to None(Null). Garbage collection is typically performed automatically but can be manually called by using "gc.collect()"

# Comparisons of References and Values
Python uses "==" and "is" for comparing references and values.  In Python, "==" refers to value equality. This is for checking if two objects have the same value. On the other hand, "is" refers to reference equality. This is used when checking if two references refer to the same object.
```
a = 500
b = 500
a == b # returns True
a is b # returns False
```

# Nul/Nil references
Python uses the "None" singleton instead of Nul or Nil. Objects can be assigned to None.

# Lambda
Lambda functions were added to Python because of increased demand from Lisp programmers. Lambdas are easily assigned in Python:
```
f = lambda x, y : x + y
f(1,1) # returns 2
```
This functional programming is especially useful with Python's list comprehension and is normally used with functions such as "map()", "filter()", and "reduce()"
In addition to lambdas, functions are treated as first-class objects and can be passed as an argument or return value to another function object.

# Listeners or Event Handlers
Python's open source nature has led to a large number of different frameworks that handle events. The most popular include: pydispatcher, zope.event, EventHook, Event class, Pynotify, and louie. The different ways come with different benefits and difficulties.
For example, the EventHook can be simply added to an existing class upon initialization:
```
class MyBroadcaster()
  def __init__():
    self.onChange = EventHook()

theBroadcaster = MyBroadcaster()
# add a listener to an event
theBroadcaster.onChange += myFunction()
```
Please look at the associated documentation to choose which one may work best for different environments.

# Singleton
Singletons are less common in Python when compared to a language like Java. Python, by nature, does not have the "final" keyword that Java uses to enforce a singleton. Singleton can be made in Python though by using different methods, including creating a dictionary of "instances" and enforcing only one can be made.
For example:
```
def singleton(cls):
  instances = {}
  def getInstance():
    if cls not in instances:
      instances[cls] = cls()
    return instances[cls]
  return getInstance
```
Using a pattern like that above enforces a psuedo final keyword as the function will return the current singleton if more than one singletons are attempted to be created.

# Procedural Programming
Python does support procedural programming. Python is one of the few object oriented languages that does not enforce the idea that code be written in a OO style. Utilizing procedural programming allows Python to be written using a 'step-by-step' style, similiar to programming in C or C++.

# Functional Programming
Python supports functional programming. The FP ability was later added to Python, which means it can be programmed in the same style as more popular functional languages such as Haskell and OCaml. Programming in a functional style allows Python to not save 'side effects', or functions that modify internal state. Programming in 'pure' functional programming normally is not done in Python though, but instead functional programming functions will be added in in support of other features.

# Multithreading
Python supports multithreading through different modules and libraries, most notably the "threading" module.
```
import threading
t1 = threading.Thread(target, args)
t1.start()
t1.join()
```
Using multithreading allows large tasks to be split up into smaller tasks to be accomplished separately and takes advantage of a CPU's ability to handle multiple processes.
