# Breadth First Traversal (BFS)

Breadth First Traversal is a queue based traversal wherein it traverse nodes of same _level_ before moving to further levels.

## Implementation ([JS](javascript.md))

```js
bfs(graph, node) {
    let visited = [];
    let queue = [node];

    while (queue.length > 0) {
        const node = queue.shift();
        visited.push(node);
        for (const neighbor of graph(node)) {
            if (visited.find(neighbor) === undefined)
                queue.push(neighbor);
        }
    }
}
```

Implementation for trees can be done much simpler as you could ignore storing and checking for visited nodes as trees guarantee that there would be no loops.
