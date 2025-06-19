# Insertion Sort

`Insertion Sort` works like how you sort playing cards in your hand.

You take one number at a time and insert it into the correct position among the numbers that are already sorted (on the left side).

```
Write a function called `insertionSort` that takes an array of numbers and sorts it in ascending order using the insertion sort method.
```

## Solutions

<details>
  <summary>Click For Solution</summary>

```JS
let arr = [5, 2, 9, 1, 3];

function insertionSort(arr) {
    let n = arr.length

    for(let i = 1; i < n; i++){
        let curr = a[i]
        let prev = i - 1
        while(a[prev] > curr && p >=0){
            a[prev + 1] = a[prev]
            prev--
        }
        a[prev + 1] = curr
    }
    return arr
}

const result = insertionSort(arr);
console.log(result);
```

</details>
