# Doubly Linked List in C

This project demonstrates how to create and manage a **Doubly Linked List (DLL)** using the C programming language. A doubly linked list is a data structure where each node points to both its previous and next node, allowing traversal in both directions.

## What is a Doubly Linked List?

In a Doubly Linked List:
- Each node contains **three fields**: 
  - `data`
  - `prev` (pointer to the previous node)
  - `next` (pointer to the next node)
- It allows moving **forward and backward** through the list.

## How to Establish Connections

When inserting a new node:

1. Create a new node using `malloc`.
2. Set the `data` field.
3. Set the `prev` and `next` pointers properly:
   - `newNode->prev = currentNode`
   - `newNode->next = currentNode->next`
4. Update surrounding nodes:
   - `currentNode->next->prev = newNode` (if the next node exists)
   - `currentNode->next = newNode`

**Basic Connection Diagram:**
NULL <- [data|prev|next] <-> [data|prev|next] <-> [data|prev|next] -> NULL

## Features

- Create a new list
- Insert nodes at the beginning, end, or between nodes
- Traverse list forward and backward
- Delete nodes

## Technologies Used

- **Language**: C
- **Compiler**: GCC or any standard C compiler
- **Libraries**: `stdio.h`, `stdlib.h`
