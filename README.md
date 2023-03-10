# AirBnB Clone - The Console

The AirBnB console will cover concepts of higher level programming aiming to eventually deploy the server as a copy of an AirBnB website.

#### Functionalities of this command interpreter:
* Create a new object (ex: a new User or a new Place)
* Retrieve an object from a file, a database etc...
* Do operations on objects 
* Update attributes of an object
* Destroy an object

## Installation
* Clone this repository: `git clone "https://github.com/alexaorrico/AirBnB_clone.git"`
* Access AirBnb directory: `cd AirBnB_clone`
* Run hbnb(interactively): `./console` and enter command
* Run hbnb(non-interactively): `echo "<command>" | ./console.py`

## File Descriptions
[console.py](console.py) - the console contains the entry point of the command interpreter. 
List of commands this console current supports:
* `EOF` - exits console 
* `quit` - exits console
* `<emptyline>` - overwrites default emptyline method and does nothing
* `create` - Creates a new instance of`BaseModel`, saves it (to the JSON file) and prints the id
* `destroy` - Deletes an instance based on the class name and id (save the change into the JSON file). 
* `show` - Prints the string representation of an instance based on the class name and id.
* `all` - Prints all string representation of all instances based or not on the class name. 
* `update` - Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file). 

#### `models/` directory contains classes used for this project:
[base_model.py](/models/base_model.py) - The BaseModel class from which future classes will be derived
* `def __init__(self, *args, **kwargs)` - Initialization of the base model
* `def __str__(self)` - String representation of the BaseModel class
* `def save(self)` - Updates the attribute `updated_at` with the current datetime
* `def to_dict(self)` - returns a dictionary containing all keys/values of the instance

Classes inherited from Base Model:
* [amenity.py](/models/amenity.py)
* [city.py](/models/city.py)
* [place.py](/models/place.py)
* [review.py](/models/review.py)
* [state.py](/models/state.py)
* [user.py](/models/user.py)

Tests
* [/tests](/tests)

## Examples of use
```
vagrant@ubuntu-focal:~/alx/python/AirBnB_clone$./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  create  destroy  help  quit  show  update

(hbnb) all MyModel
** class doesn't exist **
(hbnb) create BaseModel
74c07270-6f56-4a19-b258-98ae1eedbe15
(hbnb) all BaseModel
["[BaseModel] (74c07270-6f56-4a19-b258-98ae1eedbe15) {'id': '74c07270-6f56-4a19-b258-98ae1eedbe15', 'created_at': datetime.datetime(2023, 3, 7, 15, 41, 33, 761398), 'updated_at': datetime.datetime(2023, 3, 7, 15, 41, 33, 761414)}"]
(hbnb) show BaseModel 74c07270-6f56-4a19-b258-98ae1eedbe15
[BaseModel] (74c07270-6f56-4a19-b258-98ae1eedbe15) {'id': '74c07270-6f56-4a19-b258-98ae1eedbe15', 'created_at': datetime.datetime(2023, 3, 7, 15, 41, 33, 761398), 'updated_at': datetime.datetime(2023, 3, 7, 15, 41, 33, 761414)}
(hbnb) destroy BaseModel 74c07270-6f56-4a19-b258-98ae1eedbe15
(hbnb) show BaseModel 74c07270-6f56-4a19-b258-98ae1eedbe15
** no instance found **
(hbnb) quit
```

## Bugs
No known bugs at this time. 

## Authors
*Ruven Pillay*

## License
Public Domain. No copy write protection. 
