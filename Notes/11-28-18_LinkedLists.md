# Linked Lists #
Linked lists are dynamic sequential data structures that are commonly used to store browser histories, lists of names, etc. As opposed to arrays, Linked lists allow elements to be inserted or removed from the list without reallocating memory.

Linked Lists are composed of nodes and each node is a variable of struct or class type that is dynamically allocated using the ``new`` operator. Nodes contain the data member stored by the node as well as a pointer to the next node.

## Node Structure ##

    struct node{
      int node_content; // The data member stored in the node
      node *next;       // The next node in the list, null if this is the last element of the list
    };
    
## Adding Nodes ##
The process for adding a node to the top of an empty list is as follows:
    
    node* ptr = new node();
    head = ptr; // set the head to point to the new node
    
Or, if there is already a node in the list:

    node* ptr = new node();
    ptr->next = head;
    head = ptr;
    
To add a node to the end of the list:
    
    node* ptr = new node();
    node* temp = head;
    
    while(temp->next != nullptr)
      temp = temp->next;
      
    temp->next = ptr;
    
## Removing Nodes ##
To remove the first node from the list:
 
    node *ptr = head;
    head = ptr->next;
    delete ptr;
    
To remove the last node:
    
    node* temp = head;
    node* prev = head;
    
    while(temp->next != nullptr){
        prev = temp;
        temp->next = next;
    }
    
    delete temp;
    prev->next = nullptr;

But if there is only one element:

    head == nullptr;
    head->next == nullptr;
