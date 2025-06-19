# Linear Search

`Linear Search` is a simple way to find an item in a list. You check each item one by one from the beginning until you find what you're looking for or reach the end.

```
Write a function called linearSearch that takes an array and a target value as input.

The function should search for the target in the array using the linear search method.

If the target is found, return the index of the first occurrence.

If not found, return -1.
```

## Solutions

<details>
  <summary>Click For Solution</summary>

```JS
let arr = [4, 9, 1, 0, 2]

function linearSearch(arr, target) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === target) {
            return i
        }
    }
    return -1
}

const result = linearSearch(arr, 0)
console.log(result)
```

</details>
