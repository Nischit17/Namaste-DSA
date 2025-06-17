# Bubble Sort

`Bubble Sort` is a simple way to sort a list. You compare two numbers next to each other and swap them if they are in the wrong order. You keep doing this until the list is fully sorted — like bubbles rising to the top!

```
Write a function called `bubbleSort` that takes an array of numbers and sorts it in `ascending order` using the bubble sort method.
```

## Solutions

<details>
  <summary>Click For Solution</summary>

```JS
let arr = [5, 2, 9, 1, 3];

function bubbleSort(arr) {
    let n = arr.length;

    for (let i = 0; i < n - 1; i++) {
        // Go through the array
        for (let j = 0; j < n - 1 - i; j++) {
            // Compare each pair
            if (arr[j] > arr[j + 1]) {
                // Swap if in wrong order
                let temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }

    return arr;
}

const result = bubbleSort(arr);
console.log(result); // Output: [1, 2, 3, 5, 9]
```

</details>
