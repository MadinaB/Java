# Class Object

- Class Object is the root of the class hierarchy. 
- Every class has Object as a superclass. 
- All objects, including arrays, implement the methods of this class.

# Often used:

- toString()
- equals(Object obj)
- hashCode()

##  toString()
### String

Returns a string representation of the object.

## equals(Object obj)
### boolean

Indicates whether some other object is "equal to" this one.

If you want to compare strings (to see if they contain the same characters), you need to compare the strings using `equals`.
`==` compares object references, it checks to see if the two operands point to the same object (not equivalent objects, the same object).

Example:
```
String home ="home";
String house = "ho";
house = house+"me";
```
```
System.out.println((home==house));
```
false
```
System.out.println(home.equals(house));
```
true

## hashCode()
### int

Returns a hash code value for the object.

Joshua Bloch says on Effective Java

You must override hashCode() in every class that overrides equals(). Failure to do so will result in a violation of the general contract for Object.hashCode(), which will prevent your class from functioning properly in conjunction with all hash-based collections, including HashMap, HashSet, and Hashtable.

from [stackoverflow](https://stackoverflow.com/questions/2265503/why-do-i-need-to-override-the-equals-and-hashcode-methods-in-java):
If only equals is overriden... So, although they are equal, as they don't hash to the same bucket, the map can't realize it and both of them stay in the map.

Collections such as HashMap and HashSet use a hashcode value of an object to determine how it should be stored inside a collection, and the hashcode is used again in order to locate the object in its collection.

Hashing retrieval is a two-step process:

Find the right bucket (using hashCode())
Search the bucket for the right element (using equals() )

Here is a small example on why we should overrride equals() and hashcode().

Consider an Employee class which has two fields: age and name.
```
public class Employee {

String name;
int age;

public Employee(String name, int age) {
this.name = name;
this.age = age;
}

public String getName() {
return name;
}

public void setName(String name) {
this.name = name;
}

public int getAge() {
return age;
}

public void setAge(int age) {
this.age = age;
}

@Override
public boolean equals(Object obj) {
if (obj == this)
return true;
if (!(obj instanceof Employee))
return false;
Employee employee = (Employee) obj;
return employee.getAge() == this.getAge()
&& employee.getName() == this.getName();
}

// commented    
/*  @Override
public int hashCode() {
int result=17;
result=31*result+age;
result=31*result+(name!=null ? name.hashCode():0);
return result;
}
*/
}
```
Now create a class, insert Employee object into a HashSet and test whether that object is present or not.
```
public class ClientTest {
public static void main(String[] args) {
Employee employee = new Employee("rajeev", 24);
Employee employee1 = new Employee("rajeev", 25);
Employee employee2 = new Employee("rajeev", 24);

HashSet<Employee> employees = new HashSet<Employee>();
employees.add(employee);
System.out.println(employees.contains(employee2));
System.out.println("employee.hashCode():  " + employee.hashCode()
+ "  employee2.hashCode():" + employee2.hashCode());
}
}
```

It will print the following:

false
employee.hashCode():  321755204  employee2.hashCode():375890482

Now uncomment hashcode() method , execute the same and the output would be:

true
employee.hashCode():  -938387308  employee2.hashCode():-938387308

Now can you see why if two objects are considered equal, their hashcodes must also be equal? Otherwise, you'd never be able to find the object since the default hashcode method in class Object virtually always comes up with a unique number for each object, even if the equals() method is overridden in such a way that two or more objects are considered equal. It doesn't matter how equal the objects are if their hashcodes don't reflect that. So one more time: If two objects are equal, their hashcodes must be equal as well.


## clone()

Creates and returns a copy of this object.

It is a `protected Object` so should be overriden before use. Running `home.clone()` will throw `The method clone() from the type Object is not visible`

## finalize()
Called by the garbage collector on an object when garbage collection determines that there are no more references to the object.

## notify()
### void
Wakes up a single thread that is waiting on this object's monitor.

## notifyAll()
###  void
Wakes up all threads that are waiting on this object's monitor.

## wait(long timeout, int nanos)
###  void
Causes the current thread to wait until another thread invokes the notify() method or the notifyAll() method for this object, or some other thread interrupts the current thread, or a certain amount of real time has elapsed.


