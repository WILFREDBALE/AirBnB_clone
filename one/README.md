
# The AirBnB Clone Project

![](anb.png)

# Project Description
This is the first part of the AirBnB clone project where we worked on the backend of the project whiles interfacing it with a console application with the help of the cmd module in python.

Data (python objects) generated are stored in a json file and can be accessed with the help of the json module in python

# Description of the command interpreter:

The interface of the application is just like the Bash shell except that this has a limited number of accepted commands that were solely defined for the purposes of the usage of the AirBnB website.

This command line interpreter serves as the frontend of the web app where users can interact with the backend which was developed with python OOP programming.

Some of the commands available are:

show
create
update
destroy
count
And as part of the implementation of the command line interpreter coupled with the backend and file storage system, the folowing actions can be performed:

Creating new objects (ex: a new User or a new Place)
Retrieving an object from a file, a database etc…
Doing operations on objects (count, compute stats, etc…)
Updating attributes of an object
Destroying an object

# How to start it
These instructions will get you a copy of the project up and running on your local machine (Linux distro) for development and testing purposes.



# Installing
You will need to clone the repository of the project from Github. This will contain the simple shell program and all of its dependencies.
http://github.com/WILFREDBALE/AirBnB_clone.git

After cloning the repository you will have a folder called AirBnB_clone. In here there will be several files that allow the program to work.

/console.py : The main executable of the project, the command interpreter.

models/engine/file_storage.py: Class that serializes instances to a JSON file and deserializes JSON file to instances

models/__ init __.py: A unique FileStorage instance for the application

models/base_model.py: Class that defines all common attributes/methods for other classes.

models/user.py: User class that inherits from BaseModel

models/state.py: State class that inherits from BaseModel

models/city.py: City class that inherits from BaseModel

models/amenity.py: Amenity class that inherits from BaseModel

models/place.py: Place class that inherits from BaseModel

models/review.py: Review class that inherits from BaseModel

# How to use it
It can work in two different modes:

Interactive and Non-interactive.

In Interactive mode, the console will display a prompt (hbnb) indicating that the user can write and execute a command. After the command is run, the prompt will appear again a wait for a new command. This can go indefinitely as long as the user does not exit the program.

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

In Non-interactive mode, the shell will need to be run with a command input piped into its execution so that the command is run as soon as the Shell starts. In this mode no prompt will appear, and no further input will be expected from the user.

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

# Format of Command Input
In order to give commands to the console, these will need to be piped through an echo in case of Non-interactive mode.

In Interactive Mode the commands will need to be written with a keyboard when the prompt appears and will be recognized when an enter key is pressed (new line). As soon as this happens, the console will attempt to execute the command through several means or will show an error message if the command didn't run successfully. In this mode, the console can be exited using the CTRL + D combination, CTRL + C, or the command quit or EOF.

# Arguments
Most commands have several options or arguments that can be used when executing the program. In order for the Shell to recognize those parameters, the user must separate everything with spaces.




# Available commands and what they do
The recognizable commands by the interpreter are the following:
| Command                                  | Description                              |
|------------------------------------------|------------------------------------------|
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">quit or EOF</strong> | Exits the program                        |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | By itself                                |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">help</strong> | Provides a text describing how to use a command. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | By itself --or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">help &lt;command&gt;</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">create</strong> | Creates a new instance of a valid<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">Class</code>, saves it (to the JSON file) and prints the<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code>. Valid classes are: BaseModel, User, State, City, Amenity, Place, Review. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">create &lt;class name&gt;</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">show</strong> | Prints the string representation of an instance based on the class name and<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">show &lt;class name&gt; &lt;id&gt;</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.show(&lt;id&gt;)</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">destroy</strong> | Deletes an instance based on the class name and<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code><span> </span>(saves the change into a JSON file). |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">destroy &lt;class name&gt; &lt;id&gt;</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">.destroy()</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">all</strong> | Prints all string representation of all instances based or not on the class name. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | By itself or<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">all &lt;class name&gt;</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.all()</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">update</strong> | Updates an instance based on the class name and<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code><span> </span>by adding or updating attribute (saves the changes into a JSON file). |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">update &lt;class name&gt; &lt;id&gt; &lt;attribute name&gt; "&lt;attribute value&gt;"</strong><span> </span>---or---<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.update(&lt;id&gt;, &lt;attribute name&gt;, &lt;attribute value&gt;)</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.update(&lt;id&gt;, &lt;dictionary representation&gt;)</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">count</strong> | Retrieve the number of instances of a class. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.count()</strong> |


# AUTHORS
WILFRED BALE & BELLO AUGUSTINE
# The AirBnB Clone Project

![](anb.png)

# Project Description
This is the first part of the AirBnB clone project where we worked on the backend of the project whiles interfacing it with a console application with the help of the cmd module in python.

Data (python objects) generated are stored in a json file and can be accessed with the help of the json module in python

# Description of the command interpreter:

The interface of the application is just like the Bash shell except that this has a limited number of accepted commands that were solely defined for the purposes of the usage of the AirBnB website.

This command line interpreter serves as the frontend of the web app where users can interact with the backend which was developed with python OOP programming.

Some of the commands available are:

show
create
update
destroy
count
And as part of the implementation of the command line interpreter coupled with the backend and file storage system, the folowing actions can be performed:

Creating new objects (ex: a new User or a new Place)
Retrieving an object from a file, a database etc…
Doing operations on objects (count, compute stats, etc…)
Updating attributes of an object
Destroying an object

# How to start it
These instructions will get you a copy of the project up and running on your local machine (Linux distro) for development and testing purposes.



# Installing
You will need to clone the repository of the project from Github. This will contain the simple shell program and all of its dependencies.
http://github.com/WILFREDBALE/AirBnB_clone.git

After cloning the repository you will have a folder called AirBnB_clone. In here there will be several files that allow the program to work.

/console.py : The main executable of the project, the command interpreter.

models/engine/file_storage.py: Class that serializes instances to a JSON file and deserializes JSON file to instances

models/__ init __.py: A unique FileStorage instance for the application

models/base_model.py: Class that defines all common attributes/methods for other classes.

models/user.py: User class that inherits from BaseModel

models/state.py: State class that inherits from BaseModel

models/city.py: City class that inherits from BaseModel

models/amenity.py: Amenity class that inherits from BaseModel

models/place.py: Place class that inherits from BaseModel

models/review.py: Review class that inherits from BaseModel

# How to use it
It can work in two different modes:

Interactive and Non-interactive.

In Interactive mode, the console will display a prompt (hbnb) indicating that the user can write and execute a command. After the command is run, the prompt will appear again a wait for a new command. This can go indefinitely as long as the user does not exit the program.

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

In Non-interactive mode, the shell will need to be run with a command input piped into its execution so that the command is run as soon as the Shell starts. In this mode no prompt will appear, and no further input will be expected from the user.

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

# Format of Command Input
In order to give commands to the console, these will need to be piped through an echo in case of Non-interactive mode.

In Interactive Mode the commands will need to be written with a keyboard when the prompt appears and will be recognized when an enter key is pressed (new line). As soon as this happens, the console will attempt to execute the command through several means or will show an error message if the command didn't run successfully. In this mode, the console can be exited using the CTRL + D combination, CTRL + C, or the command quit or EOF.

# Arguments
Most commands have several options or arguments that can be used when executing the program. In order for the Shell to recognize those parameters, the user must separate everything with spaces.




# Available commands and what they do
The recognizable commands by the interpreter are the following:
| Command                                  | Description                              |
|------------------------------------------|------------------------------------------|
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">quit or EOF</strong> | Exits the program                        |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | By itself                                |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">help</strong> | Provides a text describing how to use a command. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | By itself --or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">help &lt;command&gt;</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">create</strong> | Creates a new instance of a valid<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">Class</code>, saves it (to the JSON file) and prints the<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code>. Valid classes are: BaseModel, User, State, City, Amenity, Place, Review. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">create &lt;class name&gt;</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">show</strong> | Prints the string representation of an instance based on the class name and<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">show &lt;class name&gt; &lt;id&gt;</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.show(&lt;id&gt;)</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">destroy</strong> | Deletes an instance based on the class name and<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code><span> </span>(saves the change into a JSON file). |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">destroy &lt;class name&gt; &lt;id&gt;</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">.destroy()</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">all</strong> | Prints all string representation of all instances based or not on the class name. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | By itself or<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">all &lt;class name&gt;</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.all()</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">update</strong> | Updates an instance based on the class name and<span> </span><code style="box-sizing: border-box; font-family: ui-monospace, SFMono-Regular, &quot;SF Mono&quot;, Menlo, Consolas, &quot;Liberation Mono&quot;, monospace; font-size: 13.6px; padding: 0.2em 0.4em; margin: 0px; white-space: break-spaces; background-color: var(--color-neutral-muted); border-radius: 6px;">id</code><span> </span>by adding or updating attribute (saves the changes into a JSON file). |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">update &lt;class name&gt; &lt;id&gt; &lt;attribute name&gt; "&lt;attribute value&gt;"</strong><span> </span>---or---<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.update(&lt;id&gt;, &lt;attribute name&gt;, &lt;attribute value&gt;)</strong><span> </span>--or--<span> </span><strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.update(&lt;id&gt;, &lt;dictionary representation&gt;)</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">-----</strong> |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">count</strong> | Retrieve the number of instances of a class. |
| <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">Usage</strong> | <strong style="box-sizing: border-box; font-weight: var(--base-text-weight-semibold, 600);">&lt;class name&gt;.count()</strong> |


# AUTHORS
WILFRED BALE & BELLO AUGUSTINE
