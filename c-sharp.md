# C Sharp (C#)

C#, pronounced as "C Sharp", is an [object oriented programming](object-orientated-programming.md) language that runs Microsoft's .NET framework. It also functional programming patterns using lambda expressions [Language Integrated Query](language-integrated-query.md) (LINQ).

## Hello World

Similar to Java which is primarily an object oriented language. the entry point of the program must be an public static method inside a class.

```cs
class HelloWorld {
    public static void Main(string[] args) {
        System.Console.WriteLine("Hello World");
    }
}
```

C# is a compiled [programming language](programming-language.md) and it can be compiled using the `csc` (C# compiler) command

```ps
csc helloworld.cs -out:helloworld.exe
```

## Documentation

Documentation for C# can be found at [Microsoft .NET (MSDN) API documentation](https://docs.microsoft.com/en-us/dotnet/api/)
