# AirBnB_clone - Console


Description of the project
This is the first part of the project that simulates an airbnb application in which we are creating a way to control the modules that our web page is going to use by intervening a database in json format. Here we apply object oriented programming, python data translation and command interpreted logic to deliver a local database that can be modified by commands.

General concepts in review
As you navigate this code base, it is great to note the following concepts, while completing this project.

How to create a Python package
How to create a command interpreter in Python using the cmd module
What is Unit testing and how to implement it in a large project
How to serialize and deserialize a Class
How to write and read a JSON file
How to manage datetime
What is an UUID
What is *args and how to use it
What is **kwargs and how to use it
How to handle named arguments in a function
Files and Directories
models directory will contain all classes used for the entire project. A class, called “model” in a OOP project is the representation of an object/instance.
tests directory will contain all unit tests.
console.py file is the entry point of our command interpreter.
models/base_model.py file is the base class of all our models. It contains common elements:
attributes: id, created_at and updated_at
methods: save() and to_json()
models/engine directory will contain all storage classes (using the same prototype). For the moment I will have only one: file_storage.py.
Description of the command interpreter
Commands	Description
quit	Quits the console
Ctrl+D	Quits the console
help or help <command>	Displays all commands or Displays instructions for a specific command
create <class>	Creates an object of type , saves it to a JSON file, and prints the objects ID
show <class> <ID>	Shows string representation of an object
destroy <class> <ID>	Deletes an objects
all or all <class>	Prints all string representations of all objects or Prints all string representations of all objects of a specific class
update <class> <id> <attribute name> "<attribute value>"	Updates an object with a certain attribute (new or existing)
<class>.all()	Same as all <class>
<class>.count()	Retrieves the number of objects of a certain class
<class>.show(<ID>)	Same as show <class> <ID>
<class>.destroy(<ID>)	Same as destroy <class> <ID>
<class>.update(<ID>, <attribute name>, <attribute value>	Same as update <class> <ID> <attribute name> <attribute value>
<class>.update(<ID>, <dictionary representation>)	Updates an objects based on a dictionary representation of attribute names and values
Features
The Console
Web static
MySQL Storage
Web framework
RESTFul API
Web dynamic
Tech Stack
HTML5
CSS3
Python
MySQL
Flask
General Execution
Your shell should work like this in interactive mode:

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
(hbnb) 
(hbnb) quit
$
But also in non-interactive mode: (like the Shell project in C)

$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
