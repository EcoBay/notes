# Functions

Functions are [one-to-one](relation.md#one-to-one) or [many-to-one](relation.md#many-to-one) [relations](relation.md) that map [set](set.md) $X$ to set $Y$. Set $X$ is also called the **domain** of the function while set $Y$ is its **range**. Functions can also reference it self in a process called [recursion](recursion.md).

## Computer Science

A functions in [computer science](computer_science.md) is also quite similar to a mathematical functions. There are some difference such as functions may not return an output and unlike math functions where in with same input you would get the same output. This functions are designed to the some **side effects** meaning it change other state outside the scope of the function.

For [object oriented](object-oriented-programming.md) language, functions are included as functionality of an object and are known as **methods**. Some times programming functions are similar to that of mathematical function as they do not have side effects. this type of functions are called **pure functions** and in [functional programming](functional-programming) are the only type of functions that you could use.

The input to the function are called the **parameters** of the functions while **arguments** are the actual value passed to the functions and the output of the function is called **return value**. A function parameter could either be a value **value type** or and **reference type**. With changing the value of value type doesn't change the value of the argument as it's effect is limited to the scope while for reference type changes inside the function are reflected to the passed argument. languages like [C#](c-sharp.md) also offers a variant of reference type which are **out** type which allows for an initialized variable to be passed indicating that it would be initialized inside the function.
