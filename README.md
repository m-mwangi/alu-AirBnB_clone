# alu-AirBnB_clone - The Console


## How to start :

Clone the repository
$ git clone https://github.com/m-mwangi/alu-AirBnB_clone.git

Move in to the directory
$ cd AirBnB_clone

Execute the console file
/AirBnB_clone$ ./console.py

## Project Description

This project is aimed at devoloping a simplified version of the hbnb(airbnb) website. A complete web application has the following components: The console, website's frontend interface, database storage, and backend API. The project will be developed step by step with each step focusing on a specific aspect of the application.

\*\* This is the first step and it consists of a custom command line interface for data management, and the base classes for storage of data. \*\*

## Command interpreter Usage :

| **Name**  | **Description**                                                                         |
| --------- | --------------------------------------------------------------------------------------- |
| create    | Creates a new instance of the class passed by argument.                                 |
| show      | Prints the string representation of an instance.                                        |
| \*destroy | Deletes an instance that was already created.                                           |
| all       | Prints string representation of all instances or of all instances of a specified class. |
| \*update  | Updates an instance attribute if exists otherwise create it.                            |
| help      | Show all commands or display information about a specific command.                      |
| quit      | Exit the console.                                                                       |
| EOF       | Exit the console.                                                                       |

\*\*create, destroy and update commands save changes into a JSON file.\*\*

### Console usage with examples :

| Command                                       | Example                                                                                                                        |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Run the console                               | ./console.py                                                                                                                   |
| Quit the console                              | (hbnb) quit                                                                                                                    |
| Display the help for a command                | (hbnb) help <command>                                                                                                          |
| Create an object                              | (hbnb) create <class>                                                                                                          |
| Show an object                                | (hbnb) show <class> <id> or (hbnb) <class>.show(<id>)                                                                          |
| Destroy an object                             | (hbnb) destroy <class> <id> or (hbnb) <class>.destroy(<id>)                                                                    |
| Show all objects, or all instances of a class | (hbnb) all or (hbnb) all <class>                                                                                               |
| Update an attribute of an object (hbnb)       | update <class> <id> <attribute name> "<attribute value>" or (hbnb) <class>.update(<id>, <attribute name>, "<attribute value>") |

## Models Used

| **File**      | **Description**                                      | **Attributes**                                                                                                                   |
| ------------- | ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| base_model.py | BaseModel class for all the other classes            | id, created_at, updated_at                                                                                                       |
| user.py       | User class for future user information               | email, password, first_name, last_name                                                                                           |
| amenity.py    | Amenity class for future amenity information         | name                                                                                                                             |
| city.py       | City class for future location information           | state_id, name                                                                                                                   |
| state.py      | State class for future location information          | name                                                                                                                             |
| place.py      | Place class for future accomodation information      | city_id, user_id, name, description, number_rooms, number_bathrooms, max_guest, price_by_night, latitude, longitude, amenity_ids |
| review.py     | Review class for future user/host review information | place_id, user_id, text                                                                                                          |

### Tests

All the codes will be tested with the unittest module.

# General Execution
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
