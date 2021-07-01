# Development Documentation v.1



### Introduction
Mensarius is a budget management tool, that helps you to track the record of incomes and expenses, as well as analyze that data.
Software runs and stores everything locally, for simplicity and safety of user's data, at least for the first version.
The program is provided with simple, proficient and easy-to-use CLI interface, which allows to vastly simplify it as for the user, as well as for the development.

### Usage process
The software provides user with books, every book contains different expense and income records, that are tagged with appropriate types, as well as overall statistics.

Example:
> **Personal:** <br>
> \-600 Went to the shop  \[#food #shopping] <br>
> \-500 Bought clothes  \[#clothing #shopping] <br>
> \-1200 Went to the bar  \[#drinking #social] <br>
> \+400  Debt for the bar  \[#drinking #social] <br>
> **Spendings** - 2300 <br>
> **Incomes** - 400 <br>
> **Difference** - 1900 <br>

When entering the data into specific book user can mark if record is an expense or an income, leave description and tags.
Later, user can select the data and sort it via types and tags to display only the information he wants and export it in the desirable way. 

### Data storage
For data storage, SQLite database is used, it stores everything locally, which allows to access, insert and store information easily, without spending a lot of resources, as well as being flexible for the changes.

### Parser
This is one of the key components, this module will parse all the data from database and transform them to the correct data types for further usage.
The important aspect is that the parser has to be reliable, so user's data won't be lost while reading, transforming or writing.
Also, it should be pretty fast, because loading the data is probably one of the most resource consuming tasks.

### Interface
This is the frontend of the whole program, this module will display the information, that has been carefully selected by Parser, as well as taking user input and calling backend functions.
Because the interface is not really minimalistic, the best way to build it is not the "one-line" approach, like in cat or grep, but a full interactive interface, that you can enter, do some stuff in it and then exit, like htop and vim.
This interface should be fast, simple and easy to use, because simplicity and usability are the key components.

### Utilities
A module, that contains all the pieces of code, that are being called from time to time and can be shortened in simple functions.

### Tech stack
For better and easier start, Python3 is the main technology we will be using.
Remember, that you are not alone, code should be slick and beautiful.

### The development itself
It's not easy to develop something in a team, that's why all the tasks and plans will be described together, all the questions will be answered and all the concerns will be resolved.
The point is to create something usefull and cool, get your portion of joy from the process and learn something new.
Before contributing, please check out the style guide in STYLE.md of this branch.

### Development structure
The project consists of the main executable file, that executes other modules.
+ Interface - module has an event loop, in which all information is displayed and user input is being taken, the proper map of all the functions is described in the INTERFACE.md and displayed as a chart in the INTERFACE.png.
+ Parser - module is responsible for creating and maintaining the database schema and of course of quering or inerting the information into the database, the proper map of all the functions is described in the PARSER.md and displayed as a chart in the PARSER.png.
+ Utilities - module with small, utility functions, they can be added in the development process, when needed.

The main directory also has a requirements.txt file, which has all the possible dependencies.
All the development is being done in the dev branch and it's sub branches.
