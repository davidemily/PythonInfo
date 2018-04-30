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
