# ArrayList (C#)

ArrayList is a dynamic and non-generic [array](array.md) of objects. It implements the [IList](https://docs.microsoft.com/en-us/dotnet/api/system.collections.ilist) and [ICloneable](https://docs.microsoft.com/en-us/dotnet/api/system.icloneable) [interfaces](interfaces.md) and is located at the `System.Collections` [namespace](namespace.md)

## Differences with an Array

- Its elements are of always of the typ `System.Object` as it is non-generic
- Its is dynamic meaning it can change size automatically
- Its is include in the `System.Collections` [namespace](namespace.md) as oppose to array which are included in the `System` namespace.
- There is no such thing as [Multidimensional](array.md#dimensions-of-array) ArrayList.
- ArrayList can accept `null` value

## Constructor

ArrayList have three constructor:

- `ArrayList()` - initialize an empty ArrayList with the default initial capacity of 4.
- `ArrayList(Int32)` - initialize an empty ArrayList with the specified initial capacity. Throw an `ArgumentOutOfRangeException` whet the argument is less than 0
- `ArrayList(ICollection)` - initialize an ArrayList with the same elements as the collection passed and also have it capacity as the number of elements of the the collection.

```c#
ArrayList a0 = new ArrayList();     // Creates an empty ArrayList with a capacity of 4
ArrayList a1 = new ArrayList(8);    // Create an empty ArrayList with a capacity of 8

// Creates an array list for an ICollection instance
int[] a = {1,2,3};
ArrayList a2 = new ArrayList(a);    // Creates an array with same element as array a and a capacity of 3

// Shorthand of the previous which also allows multiple types and Null
ArrayList a3 = new ArrayList {1,true,null);
```

## Properties

- `Int32 Capacity` - gets or sets the "maximum" number of elements the ArrayList. As specified earlier ArrayList are dynamic thus when you add element at a max capacity, its capacity would double. Setting its capacity less than the number of elements would throw an `ArgumentOutOfRangeException` or an `OutOfMemoryException` when there is not enough memory.

- `int Count` - gets the number of elements actually contaioned in the ArrayList
- `object? Item[int index]` - gets or sets the element of the ArrayList at the zero based `index`. Throws an `IndexOutOfRangeException` if `index` is less than 0 or greater that or equal to `Count`.

## Methods

- `void ArrayList.Add(object? value)` adds `value` to the end of the array list. `value` can be null. If the ArrayList is already at max capacity it would double its capacity.
- `void ArrayList.AddRange(ICollection c)` similar to `ArrayList.Add` but add multiple elements from collection `c` instead.
- `void ArrayList.Clear()` removes all elements from an ArrayList.
- `bool ArrayList.Contains(object? value)` returns `true` when `value` is in the ArrayList, otherwise false. `value` can be `null`.
- `void ArrayList.Insert(int index, object? value)` inserts `value` at the specified `index`. `value` can be `null`. Throws `ArgumentOutOfRangeException` when `index` is less than 0 or greater than or equal to to `Count`.
- `void InsertRange(int index, ICollection c)` insert all elements of collection `c` at the specified `index`. Throws similar exception as `ArrayList.Insert`.
- `int ArrayList.IndexOf(object? value)` returns the zero-based index of the first occurrence of `value` in the ArrayList or `-1` otherwise the element doesn't exist in the ArrayList. It has an $O(n)$ [time complexity](computational-complexity.md#time).
- `void ArrayList.Remove(object? value)` removes the first occurrence of value in the ArrayList. `value` can be null.
- `void ArrayList.RemoveAt(int index)` removes the elements at the specified index. Throws an `ArgumentOutOfRangeException` if `index` is less than 0 or greater than or equal to `Count`.
- `void ArrayList.RemoveRange(int index, int count)` is similar to `ArrayList.RemoveAt` but remove `count` elements starting from `index`. It also throws an `ArgumentException` if the number of the elements starting from index to end or the ArrayList is less than `count`
- `void ArrayList.Reverse()` reverses the elements of the array.
- `void ArrayList.Sort()` sorts the elements of the array.
- `int ArrayList.BinarySearch(object? value)`[$^{[1]}$](binary-search.md) is similar to `ArrayList.IndexOf` but requires its elements to be sorted and also have the same data typed with an advantage of $O(\log n)$ time complexity. Returns the [bitwise complement](bitwise-operator.md#bitwise-complement) of the last searched location or the placed where if you inserted it the list is still sorted.
- `object ArrayList.Clone()` creates a swallow copy of the ArrayList as an object, must be cast as an `ArrayList` to be useful.
- `ArrayList.ToArray` converts ArrayList to an array. This posed some problems due to the non-generic nature of ArrayList compared to array.
  - `object?[] ArrayList.ToArray()` returns an array of nullable object.
  - `Array ArrayList.ToArray(Type t)` return an array of element of type `t`. To be a generic array it is necessary to cast it to `(t[])`. Throws an `ArgumentNullException` if argument `t` is `null` and throws `InvalidCastException` if at least one element of the ArrayList cannot be cast to `t`. _Note: having an element of `null` doesn't mean it would throw an error as `null` can sometimes be cast to some types such as `string`_
- `void ArrayList.CopyTo` copies an ArrayList or a portion of it into an array. Throws an `InvalidCastException` when the element inside the ArrayList cannot be automatically cast into the type of the array and an `ArgumentException` when the destination is multidimensional or cannot contains the element to be copied.
  - `void ArrayList.CopyTo(Array array)` copies the whole ArrayList into `array`, starting from the beginning of the `array`.
  - `void ArrayList.CopyTo(Array array, int arrayIndex)` copies the whole ArrayList into `array`, starting from `arrayIndex`. Throws an `ArgumentOutOfRangeException` when `arrayIndex` is less than 0.
  - `void ArrayList.CopyTo(int index, Array array, int arrayIndex, int count)` copies `count` elements from the ArrayList, starting from `index`, into `array`, starting form `arrayIndex`. Throws an `ArgumentOutOfRangeException` when `index` is less than 0, `arrayIndex` is less than 0, or `count` is less than 0.

## Documentation

A more exhaustive list of methods and its description could be found at [MSDN documentation of ArrayList](https://docs.microsoft.com/en-us/dotnet/api/system.collections.arraylist)
