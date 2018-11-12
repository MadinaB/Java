# Class String

String str = "abc";

char data[] = {'a', 'b', 'c'};
String str = new String(data);

System.out.printf(String.valueOf(new Integer(5000)));

## length()

## charAt(int index)
Returns the char value at the specified index.


##  concat(String str)
Concatenates the specified string to the end of this string.

##  contains(CharSequence s)
Returns true if and only if this string contains the specified sequence of char values.

## contentEquals(CharSequence cs)
Compares this string to the specified CharSequence.

## copyValueOf(char[] data, int offset, int count)
Returns a String that represents the character sequence in the array specified.

## endsWith(String suffix)
Tests if this string ends with the specified suffix.


## hashCode()
Returns a hash code for this string.

## indexOf(int ch)
indexOf(String str, int fromIndex)
indexOf(String str)

Returns the index within this string of the first occurrence of the specified character.

## lastIndexOf(int ch)
lastIndexOf(int ch, int fromIndex)
Returns the index within this string of the last occurrence of the specified character.

## matches(String regex)
Tells whether or not this string matches the given regular expression.


## replaceAll(String regex, String replacement)
replace()
replaceFirst()

Replaces each substring of this string that matches the given regular expression with the given replacement.

String replaceString=s1.replaceAll("is","was")

String replaceString=s1.replaceAll("\\s",""); 

str = str.replaceAll("<b>([^<]*)</b>", "$1");

str = str.replaceAll("USD", "\\$");


## split(String regex)
- String[]
Splits this string around matches of the given regular expression.


## substring(int beginIndex, int endIndex)
Returns a new string that is a substring of this string.


## toCharArray()
Converts this string to a new character array.

## toLowerCase()
Converts all of the characters in this String to lower case using the rules of the default locale.


## trim()
Returns a copy of the string, with leading and trailing whitespace omitted.
