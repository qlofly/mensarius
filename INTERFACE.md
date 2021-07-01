# Interface module



### Event loop
The main part of this module, that is basically an endless loop, inside of which all other interactions are made, refreshments are done, when needed.


### Functional
+ **Hello message** - a message, that is displayed, when user starts the program.
+ **Books menu** - a function, that displays all the books and lets the user to choose one or to create a new one.
+ **Book menu** - a function, that displays brief book information.
+ **New record** - an option inside the Book menu, starts the process of creating a new record.
+ **List records** - an option inside the Book menu, lists all the records inside the book.
+ **Sort the output** - an option of List records, which sort the data by parameters, given by user.
+ **Export** - exports the result of the list, or sort functions.
+ **Delete record** - a function for choosing and deleting a specific record

These functions should be mixed up and accessible from different positions, for example, delete all records from the sort result.
This aspect should be talked over in which individual situation.



Please, separate all the functions in different files, so they don't mix up and get too complicated, remember about the style guide.
