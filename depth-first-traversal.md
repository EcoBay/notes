# Depth First Traversal (DFS)

Depth first traversal is a stack based traversal thus can be cleanly implemented with recursion wherein it continue to move to certain direction as far as possible before backtracking.

## Implementation ([JS](javascript.md))

### Recursive

```js
dfs(graph, node, visited) {
    visited.push(node);
    for (const neighbor of graph[node]) {
        if (visited.find(neighbor) === undefined)
            dfs(graph, neighbor, );
    }
}
```

### Iterative

```js
dfs(graph, node) {
    let visited = [];
    let stack = [node];

    while (stack.length > 0) {
        node = stack.pop();
        visited.push(node);
        for (const neighbor of graph[node]) {
            if (visited.find(neighbor) === undefined)
                stack.push(node);
        }
    }

}
```

Implementation for trees can be done much simpler as you could ignore storing and checking for visited nodes as trees guarantee that there would be no loops.
