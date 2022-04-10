# Binary Search

Binary search is an efficient [recursive](recursion.md) algorithm for finding a certain element in a sorted list. It is similar to the way you search a dictionary wherein rather than finding the word 1 page at a time you 2 'split' the dictionary in half and determine wether you have overshot it then search the first half otherwise search the later half.

## Recursive Implementation (JS)

```js
function binarySearch(arr, start, end, target) {
  const mid = (start + end) / 2;

  if (start > end) return -1; // target not found
  if (arr[mid] == target) return mid;
  if (arr[mid] < target) return binarySearch(arr, mid + 1, end, target);
  if (arr[mid] > target) return binarySearch(arr, start, mid - 1, target);
}
```

## Iterative Implementation (JS)

```js
function binarySearch(arr, target) {
  let low = 0;
  let high = arr.length - 1;

  while (low <= high) {
    const mid = (low + high) / 2;

    if (arr[mid] == target) return mid;
    else if (arr[mid] < target) low = mid + 1;
    else if (arr[mid] > target) high = mid - 1;
  }

  return -1; // Target not found
}
```
