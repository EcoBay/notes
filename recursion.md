# Recursion

The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. It provide a way to solve a big problem by splitting the problem into smaller problem.

## Parts of Recursive function

There are two parts of a recursive function. The first part is the **recursive case** where it calls the same function and lastly the **base case** or the part where it stop recursing anymore.

## Example (Fibonacci Sequence)

The [Fibonacci Sequence](fibonacci-sequence.md) is a recursive sequence define by $Fib(n) = Fib(n - 1) + Fib(n - 2)$, where $Fib(0) = 0$ and $Fib(1) = 1$. The beauty of recursion is how declarative the implementation would be.

```js
function Fib(n) {
  // Base Cases
  if (n == 0) return 0;
  if (n == 1) return 1;

  // Recursive case
  return Fib(n - 1) + Fib(n - 2);
}
```
