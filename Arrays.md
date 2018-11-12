# Class Arrays
public class Arrays
extends Object

- This class contains various methods for manipulating arrays (such as sorting and searching). 
- This class also contains a static factory that allows arrays to be viewed as lists.
- The methods in this class all throw a NullPointerException, if the specified array reference is null, except where noted. 


## asList()
static <T> List<T> 

asList(T... a)

```
List list1 = Arrays.asList(a);
```
## binarySearch()
- binarySearch(int[] a, int fromIndex, int toIndex, int key)
- binarySearch(int[] a, int key)
```
Arrays.binarySearch(intArr,intKey))
```

## copyOf()
- copyOf(int[] original, int newLength)

Integer[] newIntList = Arrays.copyOf(intList, 5);


## copyOfRange()
- copyOfRange(int[] original, int from, int to)

Copies the specified range of the specified array into a new array.

## deepEquals()
deep means that you compare contents of your objects recursively until all you need to compare is primitive fields.
static boolean     

- deepEquals(Object[] a1, Object[] a2)

Returns true if the two specified arrays are deeply equal to one another.

## equals()
static boolean   

equals(Object[] a, Object[] a2)

Returns true if the two specified arrays of Objects are equal to one another.

## fill()
- fill(int[] a, int val)
Assigns the specified int value to each element of the specified array of ints.
- fill(int[] a, int fromIndex, int toIndex, int val)
Assigns the specified int value to each element of the specified range of the specified array of ints.

## hashCode()
- hashCode(Object[] a)
Returns a hash code based on the contents of the specified array.

## sort()
- sort(int[] a)
Sorts the specified array into ascending numerical order.

- static void     sort(int[] a, int fromIndex, int toIndex)
Sorts the specified range of the array into ascending order.

```
Arrays.sort(intArr); 
```





Integer[] intList = new Integer[5];
Arrays.fill(intList, 10);
printArray(intList);
System.out.println(Arrays.asList(intList).toString());

public static <E> void printArray(E[] inputArray) {
    // Display array elements
    for (E element : inputArray) {
        System.out.printf("%s ", element);
    }
    System.out.println();
}


