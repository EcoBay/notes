# Namespace

Namespaces are way of providing a scope where you could use an identifier such as functions, class, variables, or even other namespaces.

## Example (C#)

You could access identifier inside a namespaces using (`.`) operator in [C#](c-sharp.md) which is quite confusing because members of class are also access the same way. Rather that specifying the namespaces every time you could bring the whole namespace to scope using the `using` keyword.

```cs
using System;   // Bring all identifier from the 'System' namespace to scope

class Namespaces {
    static void Main(string[] args) {
        // Note: 'Console' Here is not a namespace but rather a class
        System.Console.WriteLine("Hello World");    // We are accessing the 'Console' class from the 'System` namespace

        Console.WriteLine("Hello World");           // Because we are using the 'System' namespace, it is possible to omit the namespace
    }
}
```
