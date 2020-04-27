
# 4 PILLARS OF OOP
1. __Abstraction__ 
Abstraction is the process of showing only essential/necessary features of an entity/object to the outside world and hide the other irrelevant information. For example to open your TV we only have a power button, It is not required to understand how infra-red waves are getting generated in TV remote control.
2. __Encapsulation__
Encapsulation means wrapping up data and member function (Method) together into a single unit i.e. class. Encapsulation automatically achieve the concept of data hiding providing security to data by making the variable as private and expose the property to access the private data which would be public.
3. __Inheritance__
The ability of creating a new class from an existing class. Inheritance is when an object acquires the property of another object. Inheritance allows a class (subclass) to acquire the properties and behavior of another class (super-class). It helps to reuse, customize and enhance the existing code. So it helps to write a code accurately and reduce the development time.
4. __Polymorphism__
Polymorphism is derived from 2 Greek words: poly and morphs. The word "poly" means many and "morphs" means forms. So polymorphism means "many forms". A subclass can define its own unique behavior and still share the same functionalities or behavior of its parent/base class. A subclass can have their own behavior and share some of its behavior from its parent class not the other way around. A parent class cannot have the behavior of its subclass.

# S.O.L.I.D PRINCIPLES

1. __Single Responsibility__
A class should have one and only one reason to change, meaning that a class should have only one job. This means e.g. Method or Class should only have one task, for example if we have a method that is loading data from DB and also writing to the log this is bad as it has two reasons to change. Split this up into a LoadData and LogResult methods for example. 

2. __Open-Close Principle__
Objects and entities should be open for extension but closed for modification. This means when we update our code in the future we shouldn’t be editing all the code inside an existing method/function which could break it. We should use OOP principles to extend the classes and override the methods to add new functionality.

3. __Liskov Substitution Principle__
Every subclass/derived class should be substitutable for their base/parent class.

Example from SO (https://stackoverflow.com/questions/56860/what-is-an-example-of-the-liskov-substitution-principle):
In mathematics, a Square is a Rectangle. Indeed it is a specialization of a rectangle. The "is a" makes you want to model this with inheritance. However if in code you made Square derive from Rectangle, then a Square should be usable anywhere you expect a Rectangle. This makes for some strange behavior.
Imagine you had SetWidth and SetHeight methods on your Rectangle base class; this seems perfectly logical. However if your Rectangle reference pointed to a Square, then SetWidth and SetHeight doesn't make sense because setting one would change the other to match it. In this case Square fails the Liskov Substitution Test with Rectangle and the abstraction of having Square inherit from Rectangle is a bad one.

4. __Interface Segregation Principle__
A class should never need to implement a method it doesn’t use. The result of this is that we should use lots of small interfaces instead of a few large ones because we don’t want to be implementing methods that a class doesn’t need.
