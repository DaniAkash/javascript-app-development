1. Find if a linked list is circular
    Define dual pointers A and B with a common starting point. Allow pointer A to move 2 steps and pointer B to move 1 step each time. 
2. Delete the Nth element from linked list.
    * Linear Search and delete
    * Dual Pointers - First pointer A moves N steps, until which pointer B waits. After this for every move by pointer A, pointer B will also move. When pointer A reaches NULL, the pointer B can delete the element it stands on.