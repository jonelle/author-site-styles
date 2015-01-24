# ReadMe for COMP 15 HW1 
## Dynamic Arrays

This program models a standard deck of playing cards and provides a method for
dealing hands.

### List of files
**card.h**
Interface for the Card class.

**card.cpp**
Defines a playing card by assigning a suit and rank. Includes functions to 
create, set, and get cards; print them to screen; compare cards; copy cards; 
and convert a card to an integer value.

**hand.h**
Interface for the Hand class.

**hand.cpp**
Stores cards in a list. Includes functions to create a full 52 card deck; read 
a deck from input; randomly re-order a hand; add and remove a card from a hand;
and deal cards (move them to another hand) from the bottom or top of a hand.

**List_dynamic_array.h**
Interface for the List_Dynamic_Array class.

**List_dynamic_array.cpp**
Defines the list which forms the backbone of the Hand class. Includes functions
to create and copy lists; print lists as readable cards and as integers; 
determine whether a list is empty; makes a list empty; insert and remove
cards at the beginning, end, or a specific index of the list; and remove a
specific card.

**main.cpp**
Demonstrates the Card and Hand classes by creating a deck, shuffling it, 
dealing two hands, and displaying the results. 

### How to compile
Use the included Makefile.

### Data structure
Instances of the Card class are stored in a dynamic array. When necessary, the 
array expands by doubling the current capacity. The number of cards in the 
array and the array's capacity are each tracked in as ints (cards_held and 
hand_capacity), which safeguards against accessing unallocated memory. 
cards_held also provides an easy way to access a card in a specific position 
in the hand (first, second, last, etc.). 

### Algorithm
Hands (lists of cards) are largely manipulated by functions in the 
List_Dynamic_Array class. Those functions use a series of simple loops to 
move cards around. 
