# Interface Collection<E>

Superinterfaces: Iterable<E>


All Known Subinterfaces:
BeanContext, BeanContextServices, BlockingDeque<E>, BlockingQueue<E>, **Deque<E>**, **List<E>**, NavigableSet<E>, **Queue<E>**, **Set<E>**, **SortedSet<E>**, TransferQueue<E>

All Known Implementing Classes:
AbstractCollection, AbstractList, AbstractQueue, AbstractSequentialList, AbstractSet, ArrayBlockingQueue, ArrayDeque, **ArrayList**, AttributeList, BeanContextServicesSupport, BeanContextSupport, ConcurrentLinkedDeque, ConcurrentLinkedQueue, ConcurrentSkipListSet, CopyOnWriteArrayList, CopyOnWriteArraySet, DelayQueue, EnumSet, **HashSet**, JobStateReasons, LinkedBlockingDeque, LinkedBlockingQueue, **LinkedHashSet**, **LinkedList**, LinkedTransferQueue, PriorityBlockingQueue, PriorityQueue, RoleList, RoleUnresolvedList, **Stack**, SynchronousQueue, **TreeSet**, **Vector**


    
## add(E e)
- boolean 
Ensures that this collection contains the specified element (optional operation).
    
## addAll(Collection<? extends E> c)
- boolean 
Adds all of the elements in the specified collection to this collection (optional operation).

## clear()
Removes all of the elements from this collection (optional operation).

## contains(Object o)
- boolean 
Returns true if this collection contains the specified element.

## containsAll(Collection<?> c)
- boolean 
Returns true if this collection contains all of the elements in the specified collection.

## isEmpty()
- boolean 
Returns true if this collection contains no elements.


## iterator()
- Iterator<E>  
Returns an iterator over the elements in this collection.

## remove(Object o)
- boolean 
Removes a single instance of the specified element from this collection, if it is present (optional operation).

## removeAll(Collection<?> c)
- boolean 
Removes all of this collection's elements that are also contained in the specified collection (optional operation).
## retainAll(Collection<?> c)
- boolean 
Retains only the elements in this collection that are contained in the specified collection (optional operation).

## size()
- int
Returns the number of elements in this collection.

## toArray()
- Object[]    
Returns an array containing all of the elements in this collection.
```
ArrayList<Integer> list = new ArrayList<>();
list.add(5);
list.toArray();
```


## toArray(T[] a)
- <T> T[] 
Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array.
```
Integer[] myArray = new Integer[myList.size()];
myList.toArray(myArray);
```
or
```
Integer[] myArray = myList.toArray(new Integer[myList.size()]);
```
or
```
Integer[] myArray = myList.toArray(new Integer[0]);
```


---

# Interface List<E>

All Superinterfaces:
Collection<E>, Iterable<E>

All Known Implementing Classes:
AbstractList, AbstractSequentialList, **ArrayList**, AttributeList, CopyOnWriteArrayList, **LinkedList**, RoleList, RoleUnresolvedList, **Stack**, **Vector**

## add(int index, E element)
Inserts the specified element at the specified position in this list (optional operation).

## get(int index)
- E
Returns the element at the specified position in this list.

## indexOf(Object o)
- int
Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element.

## lastIndexOf(Object o)
- int
Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element.

## iterator()
Returns an iterator over the elements in this list in proper sequence. 

## listIterator()
Returns a list iterator over the elements in this list (in proper sequence).

## set(int index, E element)
Replaces the element at the specified position in this list with the specified element (optional operation).

## subList(int fromIndex, int toIndex)
- List<E>
Returns a view of the portion of this list between the specified fromIndex, inclusive, and toIndex, exclusive.

```
someList.subList(3, 7).clear();
```

## toArray()
- Object[] 
Returns an array containing all of the elements in this list in proper sequence (from first to last element).
## toArray(T[] a)
- <T> T[]   
Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array.




---

# Interface Queue<E>

boolean     
# add(E e)
- boolean  
Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning true upon success and throwing an IllegalStateException if no space is currently available.
  
# element()
- E  
Retrieves, but does not remove, the head of this queue.

# offer(E e)
- boolean  
Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions.

# peek()
- E  
Retrieves, but does not remove, the head of this queue, or returns null if this queue is empty.

# poll()
- E  
Retrieves and removes the head of this queue, or returns null if this queue is empty.
  
# remove()
- E  
Retrieves and removes the head of this queue.







---

# Class Stack<E>

## empty()

Tests if this stack is empty.
##  peek()
Looks at the object at the top of this stack without removing it from the stack.

##    pop()

Removes the object at the top of this stack and returns that object as the value of this function.
##    push(E item)
Pushes an item onto the top of this stack.

##   search(Object o)
Returns the 1-based position where an object is on this stack.
