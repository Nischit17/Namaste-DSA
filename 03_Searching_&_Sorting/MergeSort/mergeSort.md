# Merge Sort

`Merge Sort` is a fast way to sort a list by using `divide and conquer`.

It splits the list into halves until each piece has one item, then merges them back together in sorted order.

```
Write a function called `mergeSort` that takes an array of numbers and sorts it in ascending order using the merge sort algorithm.
```

## Solutions

<details>
  <summary>Click For Solution</summary>

```JS
let arr = [5, 2, 9, 1, 3];

function mergeSort(arr) {
    if (arr.length <= 1) {
        return arr;
    }

    const mid = Math.floor(arr.length / 2);
    const left = mergeSort(arr.slice(0, mid));
    const right = mergeSort(arr.slice(mid));

    return merge(left, right);
}

function merge(left, right) {
    let result = [];
    let i = 0;
    let j = 0;

    // Merge both arrays in sorted order
    while (i < left.length && j < right.length) {
        if (left[i] < right[j]) {
            result.push(left[i]);
            i++;
        } else {
            result.push(right[j]);
            j++;
        }
    }

    // Add remaining elements (if any)
    return result.concat(left.slice(i)).concat(right.slice(j));
}

const result = mergeSort(arr);
console.log(result); // Output: [1, 2, 3, 5, 9]
```

</details>
