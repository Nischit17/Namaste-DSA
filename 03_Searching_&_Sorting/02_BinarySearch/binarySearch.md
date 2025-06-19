# Binary Search

`Binary Search` is a fast way to find something in a `sorted list`.

You keep cutting the list in half and check if the middle number is what you're looking for.

If not, you look in the left or right half — depending on whether the number is smaller or bigger.

```
Write a function called `binarySearch` that takes a `sorted array` and a `target` number.
Use binary search to find the index of the target.

If found, return the index.
If not, return `-1`.
```

## Solutions

<details>
  <summary>Click For Solution</summary>

```JS
let arr = [1, 2, 4, 7, 9]; // sorted array
let target = 7;

function binarySearch(arr, target) {
    let left = 0;
    let right = arr.length - 1;

    while (left <= right) {
        let mid = Math.floor((left + right) / 2);

        if (arr[mid] === target) {
            return mid;
        } else if (arr[mid] < target) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }

    return -1;
}

const result = binarySearch(arr, target);
console.log(result); // Output: 3
```

</details>
