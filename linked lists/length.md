# Length

## Prerequisites
Pointers; Loops; Functions; Structures

## Problem
Write a function that returns the length of a singly linked list. Expected output:
```c
jharvard@run.cs50.net (~): ./a.out
Making sure the list length is indeed 10...
good!
```

## Distribution Code
```c
#include <assert.h>
#include <stdbool.h>
#include <stdio.h>
#include <stdlib.h>

#define SIZE 10

typedef struct node
{
    // the value to store in this node
    int n;

    // the link to the next node in the list
    struct node* next;
}
node;

node* head = NULL;

int length(void)
{
	// TODO
}

int main(void)
{
    // create linked list
    for (int i = 0; i < SIZE; i++)
    {
        node* new = malloc(sizeof(node));
        // check to see if memory was indeed allocated
        if (new == NULL)
        {
            exit(1);
        }
        new->n = i;
        new->next = head;
        head = new;
    }

    printf("Making sure that list length is indeed %i...\n", SIZE);

    // test length function
    assert(length() == SIZE);
    printf("good!\n");
}
```