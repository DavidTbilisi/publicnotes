---
tags:
  - it/ProgrammingLanguages
---
[Corey Schafer](https://www.youtube.com/playlist?list=PL-osiE80TeTsqhIuOqKhwlXsIBIdSeYtc)



```python

e1 = Emp("David", "Chincharashvili")

e1.fullname()
Emp.fullname(e1) # e1 is self in this case
```

## Class variables
Shared among all instances
In other programming languages `static` variable is similar concept
```python
class Emp:
	raise_amount = 1.04  # class variable
	number_of_employees = 0
	def __init__ (self, first, last, pay):
		self.first = first
		self.last = last
		self.pay = pay
		Emp.number_of_employees += 1 # Static variable example
	
	def fullname(self):
		return f'{self.first} {self.last}'

	def apply_rise(self):
		self.pay = int(self.pay * self.raise_amout) # gives us flexibility to use both Class or Instance !!!
		self.pay = int(self.pay * Emp.raise_amout) # gives us only Class accesability
		

e1 = Employee("David", "Chincharashvili", 100)
e2 = Employee("Mia", "Chincharashvili", 50)


Employee.raise_amount = 1.05 # changes to all (Class & instances)
e1.raise_amount = 1.05 # changes to one instance only

print(Employee.raise_amount)
print(e1.raise_amount)
print(e2.raise_amount)

```


## Class methods & Static Methods
```python

# Class methods 
class Emp:
	raise_amount = 1.04  # class variable
	number_of_employees = 0
	def __init__ (self, first, last, pay):
		self.first = first
		self.last = last
		self.pay = pay
		Emp.number_of_employees += 1 # Static variable example
	
	def fullname(self):
		return f'{self.first} {self.last}'

	def apply_rise(self):
		self.pay = int(self.pay * self.raise_amout) # gives us flexibility to use both Class or Instance !!!
		self.pay = int(self.pay * Emp.raise_amout) # gives us only Class accesability

	@classmethod
	def set_raise_amt(cls, amount):
		cls.raise_amount = amount

e1 = Employee("David", "Chincharashvili", 100)
e2 = Employee("Mia", "Chincharashvili", 50)

Employee.set_raise_amount(1.05) # same as Emplyee.raise_amount = 1.05

print(Employee.raise_amount)
print(e1.raise_amount)
print(e2.raise_amount)
```


### Alternative constructors
```python
class Emp:
	def __init__ (self, first, last, pay):
		self.first = first
		self.last = last
		self.pay = pay

employee1 = "David_chincharashvili_100" # We have a lot of data in this format
```

We can create alternative constructor exactly for the given string or format

```python
class Emp:
	def __init__ (self, first, last, pay):
		self.first = first
		self.last = last
		self.pay = pay

	@classmethod
	def from_string(cls, string):
		first, last, pay = string.split("_")
		return cls(first, last, pay)


employee1 = "David_chincharashvili_100" # We have a lot of data in this format


emp1 = Emp.from_string(employee1)
```

### Static class
Regular function but logically connected to class
```python
class Emp:
	def __init__ (self, first, last, pay):
		self.first = first
		self.last = last
		self.pay = pay
		
	@staticmethod
	def is_workday(day):
		if day.weekday() == 5 or day.weekday() == 6:
			return False
		return True

	

import datetime
print( Emp.is_workday(datetime.date(2024,7,11)) )
```

## [Inheritance](https://youtu.be/RSl87lqOXDE?si=Kvalc9BeW35ywSUE)

### Method Resolution Order
```python
print(help(Classname))
```

## Magic/Dunder methods

## Property Decorators - Getters, Setters, and Deleters