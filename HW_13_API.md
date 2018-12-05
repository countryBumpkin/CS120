# Homework #13 #

Write code for a linked list that stores a name and user id. The program should add a total of four people to the linked list and print debugging statements to prove functionality is implemented.

## _**Class Node:**_ ##

Private Variables:

| Data Type | Variable Name | Purpose |
|-----------|---------------|-------- |
| string    | name          | Stores the name of the person that matches the id |
| int       | ID            | Stores the id number of the person |
| node*     | next1         | Points to the list item following the current node

| Function | Return Type | Purpose |
| -------- | ----------- | ------- |
| set(string name, int id, node* ptr) | void | Sets the values of the node |
| print    |  void       | Recursively prints the name and id of all nodes in the linked list|
| search(int id)   |  string     | Recursively search all the nodes for an ID that matches ``id`` and return the name of the person with the matching id
| queue(string name, int id) | void | Add a new node with ``name`` and ``id`` to the end of the queue, should be recursive


## Main Function ##
The main function should do the following:

1. Add the following nodes to the list using the ``new`` operator:
    * "Alice", 123
    * "Bob", 234
    * "Charlie", 678
    * "Dave", 789

2. Test whether the print function works by printing the current list.
3. Test whether the search function works by:
    * searching for a node that _**is**_ in the list
    * searching for a node that _**is not**_ in the list
    
4. Add a new node to the list using the ``queue(string, int)`` function.
    
