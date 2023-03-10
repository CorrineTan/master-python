### OOP Basics

1. Instead of writing the commands line by line, we will structure our code in a way that will be centered around objects. 
2. These objects will exchange messages. 
3. And object will respond to these messages by performing actions. 
4. Ojbects also has its own states and set attribtues.
5. Ojbects has: State and Behavior
6. They are not mutually exclusive - you can combine them in actual project. 

#### paradigm
A Programming paradigm (approach used to solve problem with code) that organizes software design around objects.

- paradigm: declaritive, imperative, functional, logic

#### Advantage

1. Modularity
2. Extendsibility
3. Reusability 


### Class

A blueprint of creating objects

Two parts:
1. Class Header:
1st line of a class definition.

2. Class Body

```
class Backpack:
	pass

```
Elements:
1. class attributes
2. __init__()
3. Methods

Object ~ Abstract.
Instance ~ Concrete. Attributes can have unique value for instances

#### __init__

Special method to define the initial state of an object

```
class House:
	def __init__(self, price):
		self (the instance that is being created).price (the attribute of the instance) = price (the value we are assigning)

```

```
class BlackPack:
	def __init__(self, height, size):
		self.item = []
		self.height = height
		self.size = size
		self.color = "Blue"
```

#### self
- self is a generic way of referring to the current instance of the class

- always use self for the 1st argument to instance methods

- The __init__() method is called automatically when an instance of the class is created in the program.

We Skip Self When We Create an Instance:
```
class Circle:
	def __init__(self, radius, color):
		self.radius = radius
		self.color = color

my_circle = Circle(3, 'Red')
```
Comparing None to anything will always return False except when we compare it to None itself.

#### Access instance attributes

inside the class: self.<attribute>

```
class Backpack:
	def __init__(self):
		self.items = []
		print(self.items)
my_backpack = Backpack()
```

outside the class: <object>.<attribute>

```
class Backpack:
	def __init__(self):
		self.items = []
my_backpack = Backpack()
print(my_backpack.items)
```

#### Default arguments
Don't use spaces around the = sign when used to indicate a keyword argument or default value for an unannotated function aparameter.

ex: def complex(real, imag=0.0)    ===> not "image = 0.0"

```
class Circle:
	def __init__(self, radius=5):
		self.radius = radius
my_circle = Circle(8)     ===> can overwrite
```

Note: Default arguments must be the last parameter in the list of parameters

Otherwise: "SyntaxError: non-default argument follows default argument"

#### Modify instance attributes
Outside class:
<object>.<attributed> = <new_value>

Inside class:
self.<attributed> = <new_value>