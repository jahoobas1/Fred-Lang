# JPlusLang
J+ is a language developed in the Roblox engine, specifically catered toward developers wishing to include a feature within their experiences where players can create their own games. This is meant to be a language which is sandboxed, so players can't delete important things or backdoor their game (allowing for exploiting).

Made by jahoobas.
Thanks to Justafunnyknight for the name of the language.

TEST BETA VERSIONS HERE: https://www.roblox.com/games/17616460384/J-testing-place

# HOW IT WORKS
J+ works by taking the code sent in as a string and splitting it up into seperate strings in an array.
It further splits those up into commands and arguments.
It uses those to run a function with arguments to do things within the game.

It prevents players from changing things within services like ReplicatedStorage and ServerScriptService, preventing them from removing critical scripts.

If you try to access a forbidden service, it will return a warning stating that you are not allowed to change anything there.

# SYNTAX
Although it is up to you to provide documentation for the language, you should know all the syntax in order for you to provide said documentation.

Syntax is always open to change at any time.

about - Provides a small about section in the Output.
newInst - Creates a new instance.
editInst - Edits an existing instance.
waitTime - Waits the provided time.
removeInst - Removes an instance from the game.
printMessage - Allows the player to print a string into the output.

# HOW TO PROVIDE ARGUMENTS
In order to provide arguments, you would want to do the following:
command,arg

Example:
editInst,Workspace,GameParts,Part,BrickColor,BrickColor.new('Bright_red')

# USING STRINGS
Using strings in J+ is different from Luau; since spaces are removed when running the command, all spaces are removed from a string as well.
In order to have spaces in a string, you need to replace the spaces with underscores (_).

String: "Hello world!" Output: "Helloworld!"

Fixed String: "Hello_world!" Output: "Hello world!"

# USING OTHER DATATYPES
When using other datatypes, you should use the Luau way of typing them out.

For example, when changing BrickColor, you should do the following:
BrickColor.new("Color")

instead of
Color

Please note, when changing BrickColor, you should use the string format when stating the name of said BrickColor.

Another example for Vector3:
Vector3.new(50,10,2)


When using these, be sure to include them as an argument for the command you are running.

# USING MORE THAN ONE COMMAND IN A SINGLE SCRIPT
When using J+, you must keep in mind that if you do not mark the end of a command correctly, your script will not work.
To mark the end of a command, you need to put a | at the end of it, otherwise the language will interpret the next command as an argument for the previous.
