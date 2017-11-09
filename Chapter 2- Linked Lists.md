# Chapter 2: Linked Lists
## By Rachael Pai 11/10/2017

---

## Chapter Outline
+ What is Linked List ?
+ Creating Linked List
    + Issue and solution to creating a node in Java
+ Deleting a Node from Single Linked List
+ The Runner Technique
+ ~~Resurcive Problems~~

---

## What i have expected from my study ?

+ Fundamental 
+ Content of the chapter
+ What left behind the topic ? 
+ What is the difference between first-read and now ?
+ Questions to practice

---

## What is linked list ?
+ Node
    + Data
    + Reference to next node
+ Head: reference to first node

![](https://i.imgur.com/riwNuU5.jpg)

----

## Type of linked list

+ Single linked list
+ Double linked list
![](https://i.imgur.com/X7b5aZv.jpg)
+ Circular linked list

---

## Linked List Operations (1)
+ AddFirst
![](https://i.imgur.com/0oqFQEB.jpg)

+ Travesering
![](https://i.imgur.com/jl1hDvn.jpg)

----

## Linked List Operations (2)

+ AddLast
![](https://i.imgur.com/szOdYyY.jpg)

+ Inserting "after"
![](https://i.imgur.com/IvWdSZi.jpg)

----

## Linked List Operations (3)

+ Inserting "before"
![](https://i.imgur.com/1ZHlWb1.jpg)

+ Deletion
![](https://i.imgur.com/D17PUdk.jpg)

---

## Iterator / Cursor

The whole idea of the iterator is to provide an access to a private aggregated data and at the same moment hiding the underlying representation

----

## Functions of Iterator
+ AnyType next() - returns the next element in the container
+ boolean hasNext() - checks if there is a next element
+ void remove() - (optional operation).removes the element returned by next()

---

## Creating Linked List

+ wrap this with head

---

## Deleting a Node from Single Linked List
+ Check null pointer
+ Upadte Head / Tail pointer

---

# The Runner Technique
+ Detecting a circular linked list
+ One fast and one slow, eventually they will be in the same node sometimes

----

![](https://i.imgur.com/rJ1QXu6.jpg)


---

## Extra: Linkedlist vs Array

+ Fix Size (Array) vs Dynamic (Link)
+ Easier Insertion and Deletion (Link)
+ Random Access(Array) vs Access Sequentially (Link)
+ More Memory (Link)
+ Better Cache locality (Array)


---

## Reference

+ [www.cs.cmu.edu Linked Lists](https://www.cs.cmu.edu/~adamchik/15-121/lectures/Linked%20Lists/linked%20lists.html)

+ [Linked Lists By Gayle Laakmann ](https://www.youtube.com/watch?v=njTh_OwMljA)

+ [Cycles in a Linked List](https://www.youtube.com/watch?v=MFOAbpfrJ8g)

+ [linked-list-vs-array](https://www.youtube.com/watch?time_continue=344&v=QRpbNTKH6XY)
+ [My Go Implement LinkedList](https://github.com/pieceofr/linkedList)

###### tags: `wwc` `cracking the code` `linked lists`