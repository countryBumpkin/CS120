# Linked Lists #
Linked lists are dynamic sequential data structures that are commonly used to store browser histories, lists of names, etc. As opposed to arrays, Linked lists allow elements to be inserted or removed from the list without reallocating memory.

Linked Lists are composed of nodes and each node is a variable of struct or class type that is dynamically allocated using the ``new`` operator. Nodes contain the data member stored by the node as well as a pointer to the next node.

## Node Structure ##

    struct node{
      int node_content; // The data member stored in the node
      node *next;       // The next node in the list, null if this is the last element of the list
    };
    
## Adding Nodes ##
The process for adding a node to the top of the list is as follows:

    node new_node = new node(); // Create a new node
    node *second_node = head;   // Save the pointer to the first node in the list
    head = new_node;            // Set the head to point to the new node
    new_node.next = second_node;// Set new node to point to the second node
    
To add a node to the end of the list:
    
    node *ptr = head;
    while(ptr->next != NULL)
      ptr = ptr->next;
      
    node new_node = new node();
    ptr.next = &new_node;
    
 ## Removing Nodes ##
 To remove a node from the list:
 
    node *ptr = head;
    head = ptr->next;
    delete ptr;
