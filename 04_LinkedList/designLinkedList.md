# Design Linked List

### 1) Node - Creating Nodes In Linked List

```js
function Node(val) {
  this.val = val;
  this.next = null;
}
```

### 2) Linked List

```js
function MyLinkedList() {
  this.head = null;
  this.size = 0;
}
```

### 3) Add At Head

```js
MyLinkedList.prototype.addAtHead = function (val) {
  const newNode = new Node(val);
  newNode.next = this.head;
  this.head = newNode;
  this.size++;
};
```
