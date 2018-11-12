# Interface Iterator<E>

- An iterator over a collection. 

- Iterator takes the place of Enumeration in the Java Collections Framework. 

- Iterators differ from enumerations in two ways:

1. Iterators allow the caller to remove elements from the underlying collection during the iteration with well-defined semantics.
2. Method names have been improved. 


## hasNext()
boolean

Returns true if the iteration has more elements.

## next()
E     

Returns the next element in the iteration.

## remove()

Removes from the underlying collection the last element returned by this iterator (optional operation). This method can be called only once per call to next(). The behavior of an iterator is unspecified if the underlying collection is modified while the iteration is in progress in any way other than by calling this method.

Throws:
UnsupportedOperationException - if the remove operation is not supported by this iterator
IllegalStateException - if the next method has not yet been called, or the remove method has already been called after the last call to the next method


# Interface ListIterator<E>

```
public class ListIteratorExample {
    public static void main(String a[]){
        ListIterator<String> litr = null;
        List<String> names = new ArrayList<String>();
        names.add("Shyam");
        names.add("Rajat");
        names.add("Paul");
        names.add("Tom");
        names.add("Kate");
        //Obtaining list iterator   
        litr=names.listIterator();

        System.out.println("Traversing the list in forward direction:");
        while(litr.hasNext()){
            System.out.println(litr.next());
        }
        System.out.println("\nTraversing the list in backward direction:");
        while(litr.hasPrevious()){
            System.out.println(litr.previous());
        }
    }
}
```
Superinterface: Iterator<E>

public interface ListIterator<E> extends Iterator<E>

An iterator for lists that allows the programmer to traverse the list in either direction, modify the list during iteration, and obtain the iterator's current position in the list. A ListIterator has no current element; its cursor position always lies between the element that would be returned by a call to previous() and the element that would be returned by a call to next(). An iterator for a list of length n has n+1 possible cursor positions, as illustrated by the carets (^) below:

     Element(0)   Element(1)   Element(2)   ... Element(n-1)

cursor positions: ^            ^            ^            ^                  ^

Note that the remove() and set(Object) methods are not defined in terms of the cursor position; they are defined to operate on the last element returned by a call to next() or previous(). 

## add(E e)
Inserts the specified element into the list (optional operation).

## hasNext()
Returns true if this list iterator has more elements when traversing the list in the forward direction.

## hasPrevious()
Returns true if this list iterator has more elements when traversing the list in the reverse direction.

## next()
- E
Returns the next element in the list and advances the cursor position.

## nextIndex()
- int
Returns the index of the element that would be returned by a subsequent call to next().

## previous()
Returns the previous element in the list and moves the cursor position backwards.
- E

## previousIndex()
Returns the index of the element that would be returned by a subsequent call to previous().
- int

## remove()
Removes from the list the last element that was returned by next() or previous() (optional operation).

## set(E e)
Replaces the last element returned by next() or previous() with the specified element (optional operation).


