Classes are defined with the "class" keyword, and should always start with a capital letter, ex:

->  class User:
        pass
  
Create an **object** or an **instance** of a class, by calling the class name with parentheses:

->  user1 = User()

There is no limit to the number of objects that can be made from a class.

Data attached to an object is called a **field**, do not capitilise the name of fields, use underscores to seperate words:

->  user1.first_name = "Blah"
->  user1.last_naem = "Bleh"

Different objects from the same class can have varying amounts of unique fields assigned to it. If a field is called for an object that does not have that field assigned to it, an Attribute Error is given

To access the data/field in the object of the class User, type the same way it was assigned:

->  print(user1.first_name)...

A separate variable can have exact same name is the field assigned to an object, but will contain a different value if called as part of the object field. Ex:

->  first_name = "Bloo" #will contain "Bloo"
->  user.first_name #will contain "Blah" as assigned above

Classes have the following additional features (over dicts for example):
    - Methods - a function inside a class is called a method
    - Initialization
    - Help text

The init method is a feature that can be added to python classes (init methods in other languages are sometimes called "constructors")

->  class User:
->      def __init__(_self_,full_name, birthday):

The init method is called everytime a new instance/object of the class is created. The first argument in the method is "_self_", which is a reference to the new object that has been created

First thing to do in init method is store argument values to a field in the newly created object:

->  class User:
->      def __init__(_self_,full_name, birthday):
->          _self_.name = full_name
->          _self_.birthday = birthday #"birthday is the value of the argument passed throught the method, "_self_.birthday" is the field that stores the value 

