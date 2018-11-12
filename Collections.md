
# Class Collections

This class consists exclusively of static methods that operate on or return collections. It contains polymorphic algorithms that operate on collections, "wrappers", which return a new collection backed by a specified collection, and a few other odds and ends. 


## addAll(Collection<? super T> c, T... elements)
Adds all of the specified elements to the specified collection.
```
List<Integer> theNumbers = new LinkedList<Integer>();
Collections.addAll(theNumbers, 4, 8, 15, 16, 23, 42);'
```
is similar to
```
List<Integer> theNumbers = new LinkedList<Integer>(Arrays.asList(4, 8, 15, 16, 23, 42));
```
or
```
import static java.util.Arrays.*;
List<Integer> theNumbers = new LinkedList<Integer>(asList(4, 8, 15, 16, 23, 42));
```

## binarySearch()
- binarySearch(List<? extends Comparable<? super T>> list, T key)
- binarySearch(List<? extends T> list, T key, Comparator<? super T> c)
```
int index = Collections.binarySearch(al, 10)
```


```
class Binarysearch { 
    public static void main(String[] args) { 
        // Create a list 
        List<Domain> l = new ArrayList<Domain>(); 
        l.add(new Domain(10, "quiz.geeksforgeeks.org")); 
        l.add(new Domain(20, "practice.geeksforgeeks.org")); 
        l.add(new Domain(30, "code.geeksforgeeks.org")); 
        l.add(new Domain(40, "www.geeksforgeeks.org")); 

        Comparator<Domain> c = new Comparator<Domain>() 
        { 
            public int compare(Domain u1, Domain u2) 
            { 
                return u1.getId().compareTo(u2.getId()); 
            } 
        }; 

        // Searching a domain with key value 10. To search 
        // we create an object of domain with key 10. 
        int index = Collections.binarySearch(l, 
        new Domain(10, null), c); 
        System.out.println("Found at index  " + index); 

        // Searching an item with key 5 
        index = Collections.binarySearch(l, 
        new Domain(5, null), c); 
        System.out.println(index); 
    } 
} 

// A user-defined class to store domains with id and url 
class Domain 
{ 
    private int id; 
    private String url; 

    // Constructor 
    public Domain(int id, String url) 
    { 
        this.id = id; 
        this.url = url; 
    } 

    public Integer getId() 
    { 
        return Integer.valueOf(id); 
    } 
} 

```
```
public class NameComparator implements Comparator<User> {
    @Override
    public int compare(User u1, User u2) {
        return u1.getName().compareTo(u2.getName());
    }
}

NameComparator nameComparator = new NameComparator();
Collections.sort(users, nameComparator);
int idx = Collections.binarySearch(users, new User("Daenerys"), nameComparator);
```

## max
max(Collection<? extends T> coll)
max(Collection<? extends T> coll, Comparator<? super T> comp)
```
Collections.max(list));  
```
```
Comparator<String> cmp = new Comparator<String>() {
    @Override
    public int compare(String o1, String o2) {
        return Integer.valueOf(o1).compareTo(Integer.valueOf(o2));
    }
};
System.out.println("max : " + Collections.max(dirNo, cmp));
```
## min 
min(Collection<? extends T> coll)
min(Collection<? extends T> coll, Comparator<? super T> comp)

## reverse()
reverse(List<?> list)



## emptyList()
Returns the empty list (immutable).
emptyIterator()

## copy()
copy(List<? super T> dest, List<? extends T> src)
Copies all of the elements from one list into another.

## fill
fill(List<? super T> list, T obj)

## frequency(Collection<?> c, Object o)
Returns the number of elements in the specified collection equal to the specified object.


## indexOfSubList(List<?> source, List<?> target)
Returns the starting position of the first occurrence of the specified target list within the specified source list, or -1 if there is no such occurrence.

## replaceAll(List<T> list, T oldVal, T newVal)

## sort
sort(List<T> list)
static <T> void     sort(List<T> list, Comparator<? super T> c)


## swap(List<?> list, int i, int j)
Swaps the elements at the specified positions in the specified list.
