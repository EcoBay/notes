# String (C#)

In C#, [string](string.md) is an immutable collection of 16bits unicode characters which is an instance of the `System.String` class. String have a limit of 2GB or about 1 billion characters (2Bytes).

## Initialization

### Create a String from a literal

A string from literal is the most common way to create a string. String literal in C# are similar to string literal in many language wherein it is enclosed between double quotes with special characters such as `\` an `"` or control characters such as newline an tab are escaped using C#.

```c#
string str = "\t\"hello\"\nworld!"; // \t means tab, while \n mean newline
/* Represents:

    "Hello"
world!

*/
```

### Create a string using a Constructor

There are a lot of [overloads] for the String constructor in C# but the two most common ones are:

- `String(char[]? chars)` creates an string from array of `chars`. Unlike C/C++ where strings are null character `\0` terminated, C# allow for null characters anywhere in the string. `chars` can also be `null` but note that an empty string is the same as an empty string.
- `String(char c, int count` creates an string of the character `c` repeated `count` times. Throws an `ArgumentOutOfRangeException` when count is less than 0.

### Create a string using a property or a method

Strings can be created using a property or a method such as getting user input using the `Console.ReadLine` method or even from a string method like the `String.Substring` method.

## Properties

- `int Length` gets the number of characters in string.
- `char Chars[int index]` get the character at the specified `index`. Throws an `IndexOutOfRangeException` when `index` is less than 0, or greater than or equal to `Length`.

## Most Common Methods

- `int String.Compare(string str1, string str2)` - returns the integer that indicates their relative lexicographical ordering.
  - $0$ - if `str1` and `str2` are the same
  - $>0$ - i if `str2` is ordered first that `str1`
  - $<0$ - i if `str1` is ordered first that `str2`
- `string String.Concat(string str1, string str2)` - returns new string with the value of `str1` appended with the value of `str2`.
- `string String.Copy(string str)` - return a new string with the same value as `str`.
- `bool String.Equals(string str1, string str2)` - returns `true` if the value of `str1` is the same as the value of `str2`, otherwise returns `false`.
- `int String.IndexOf` - returns the zero-based index of the first occurrence a character or a substring in the string. return `-1` if in is not present in the string.
  - `int String.IndexOf(char c)` - returns the index of the first occurrence of character `c` from the start of string.
  - `int String.IndexOf(string s)` - returns the index of the first occurrence of substring `s` from the start of string. returns `0` if `s` is empty.
  - `int String.IndexOf(char c, int startIndex)` - returns the first occurrence of character `c` from the specified `startIndex` of the string. Throws an `ArgumentOutOfRangeException` if `startIndex` is less than 0 or greater than the `Length` of the string.
  - `int String.IndexOf(string s, int startIndex)` - returns the index of the first occurrence of substring `s` from the specified `startIndex` of the string. returns `0` if `s` is empty. Throws an `ArgumentOutOfRangeException` if `startIndex` is less than 0 or greater than the `Length` of the string.
- `int String.IndexOfAny` - returns the zero-based index of the first occurrence of any character from an array of character inside the string. Returns `-1` if none of the characters were found or if the array of character is empty.
  - `int String.IndexOfAny(char[] chars)` - return the index of the first occurrence of any character from `char` starting from the start of string.
  - `int String.IndexOfAny(char[] chars, int StartIndex)` - return the index of the first occurrence of any character from `char` starting the specified `startIndex`. Throws an `ArgumentOutOfRangeException` if `startIndex` is less than 0 or greater than the `Length` of the string.
