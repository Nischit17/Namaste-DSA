# Selection Sort

`Selection Sort` finds the smallest number in the list and puts it at the beginning.

Then it finds the next smallest and puts it in the second place, and so on.

It keeps selecting the smallest number from the unsorted part of the list.

```
Write a function called `selectionSort` that takes an array of numbers and sorts it in ascending order using the selection sort method.
```

## Solutions

<details>
  <summary>Click For Solution</summary>

```JS
let arr = [5, 2, 9, 1, 3];

function selectionSort(arr) {
    let n = arr.length;

    for (let i = 0; i < n - 1; i++) {
        let minIndex = i;

        // Find the index of the smallest number in the rest of the array
        for (let j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIndex]) {
                minIndex = j;
            }
        }

        // Swap the found minimum with the first number of unsorted part
        if (minIndex !== i) {
            let temp = arr[i];
            arr[i] = arr[minIndex];
            arr[minIndex] = temp;
        }
    }

    return arr;
}

const result = selectionSort(arr);
console.log(result); // Output: [1, 2, 3, 5, 9]
```

</details>
