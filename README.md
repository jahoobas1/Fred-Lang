# FredLang

Made for Rewindblox, Fred is a language developed in the Roblox engine, specifically catered toward developers wishing to include a feature within their experiences where players can create their own games. This is meant to be a language which is sandboxed, so players can't delete important things or backdoor their game (allowing for exploiting).

Made by jahoobas.

Game is uncopylocked so people can view the code. <br>
TEST BETA VERSIONS HERE: https://www.roblox.com/games/17616460384/J-testing-place

# HOW IT WORKS
Fred works by taking the code sent in as a string and splitting it up into seperate strings in an array. <br>
It further splits those up into commands and arguments. <br>
It uses those to run a function with arguments to do things within the game. <br>

It prevents players from changing things within services like ReplicatedStorage and ServerScriptService, preventing them from removing critical scripts.

If you try to access a forbidden service, it will return a warning stating that you are not allowed to change anything there.

# SYNTAX
Although it is up to you to provide documentation for the language, you should know all the syntax in order for you to provide said documentation.

Syntax is always open to change at any time.


about - Provides a small about section in the Output.<br>
newInst, Class, Parent, Name - Creates a new instance.<br>
editInst, Service, Parent, Name, Property, Value, IsVariable - Edits an existing instance.<br>
waitTime, time - Waits the provided time.<br>
removeInst, Service, Parent, Name, IsVariable - Removes an instance from the game.<br>
printMessage, message - Allows the player to print a string into the output.<br>
newVariable, name, value, datatype - Make a variable.<br>
editVariable, name,newValue - Edit an existing variable.<br>
arithmetic, number,number,outputVariable,operation - Do math on 2 numbers and output the result to an existing variable.<br>
randomNumber, minimum, maximum, outputVariable - Picks a random number between the minimum and the maximum and outputs the result to an existing variable.<br>

# HOW TO PROVIDE ARGUMENTS
In order to provide arguments, you would want to do the following:
command;arg

Example:
editInst;Workspace;GameParts;Part;BrickColor;BrickColor.new('Bright_red'),false

# USING STRINGS
Using strings in Fred is different from Luau; since spaces are removed when running the command, all spaces are removed from a string as well.
In order to have spaces in a string, you need to replace the spaces with underscores (_). <br>

String: "Hello world!" Output: "Helloworld!" <br>

Fixed String: "Hello_world!" Output: "Hello world!" <br>

# USING OTHER DATATYPES
When using other datatypes, you should use the Luau way of typing them out. <br>

For example, when changing BrickColor, you should do the following: <br>
BrickColor.new("Color") <br>

instead of <br>
Color <br>

Please note, when changing BrickColor, you should use the string format when stating the name of said BrickColor. <br>

Another example for Vector3: <br>
Vector3.new(50,10,2) <br>


When using these, be sure to include them as an argument for the command you are running. <br>

# USING MORE THAN ONE COMMAND IN A SINGLE SCRIPT
When using Fred, you must keep in mind that if you do not mark the end of a command correctly, your script will not work. <br>
To mark the end of a command, you need to put a | at the end of it, otherwise the language will interpret the next command as an argument for the previous. <br>
