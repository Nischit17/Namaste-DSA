# Linked List

### What is a Linked List?

A `Linked List` is a `linear data structure` where elements (called `Nodes`) are stored in a sequence but not in contiguous memory blocks like arrays. Instead, each node points to the next node in the sequence.

### What Does a Node Look Like?

Each `Node` typically contains:

- `Data`: The `value` or `content` stored.

- `Next Pointer`: A reference (or pointer) to the next node in the list.

## Class Node

```js
class Node {
  constructor(data) {
    this.data = data;
    this.next = null;
  }
}
```

### Key Terms

- `HEAD`: The `first node` in the `linked list`.

- `TAIL`: The `last node` in the `linked list` (its next is `null`).

- `NULL`: A special value used to indicate the end of the list (no further nodes).

```js
HEAD -> [data|next] -> [data|next] -> [data|null] <- TAIL
```

### Types of Linked Lists

1. Singly Linked List - Each node points to the next node.

2. Doubly Linked List - Each node has two pointers: one for the `next node` and one for the `previous node`.

3. Circular Linked List - The last node points back to the `first node`, forming a circle.
