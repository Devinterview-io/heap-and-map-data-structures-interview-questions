# ⚫ Heaps & Maps in Tech Interviews 2024: 10 Essential Questions & Answers

**Heaps** are specialized tree-based data structures that satisfy the heap property, ensuring efficient access to the maximum or minimum element. **Maps** are collections of key-value pairs, ensuring unique keys and facilitating fast data retrieval. In coding interviews, questions involving these structures are used to test a candidate's understanding of **priority operations** with heaps and **data organization and retrieval** with maps.

Check out our carefully selected list of **basic** and **advanced** Heaps & Maps questions and answers to be well-prepared for your tech interviews in 2024.

![Heaps & Maps Decorative Image](https://storage.googleapis.com/dev-stack-app.appspot.com/blogImg/heapsAndMaps.png?GoogleAccessId=firebase-adminsdk-bgeaf%40dev-stack-app.iam.gserviceaccount.com&Expires=1698606026&Signature=BR45PrOwWx4Zue34%2F0SpPZijcybZISGI6%2FgURnzefXk5QVyyKznFJKQj7Py7y%2B228zcLI5UU4KaLTZwH08Cb7hFf26voXcch76GPGBVVNJr5F46OLQ%2Fj9IPNKEHmyaQqgzMEpWYHsjp2q2PwlibYYvRBwr5peYxQm7M7csKXqF7Idn2LxMt8AbyQU4RnY2UVxXvX7PPhUh%2Fxs42wirjzlnllGuEM29s4LVDNx4RFN9TQiekHLO8l0ph%2FEAsGNd1z%2BEzQy60D%2FkoF6%2B0cq0tx7b4Sy7NqLjthLCwqiT1CKDQATB3PEiiWCAbDhpIYNd06f2eKJVyRgj9IoyuWlVYzgg%3D%3D)

👉🏼 You can also find all answers here: [Devinterview.io - Heaps & Maps](https://devinterview.io/data/heapsAndMaps-interview-questions)

---

## 🔹 1. What is a _Heap_?

### Answer

A **Heap** is a **tree-based** data structure that is commonly used to implement **priority queues**. There are two primary types of heaps: Min Heap and Max Heap.

In a **Min Heap**, the root node is the smallest element, and each parent node is smaller than or equal to its children. Conversely, in a **Max Heap**, the root node is the largest element, and each parent node is greater than or equal to its children.

### Key Characteristics

- **Completeness**: All levels of the tree are fully populated except for possibly the last level, which is filled from left to right.
- **Heap Order**: Each parent node adheres to the heap property, meaning it is either smaller (Min Heap) or larger (Max Heap) than or equal to its children.

### Visual Representation

![Min and Max Heap](https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/heaps%20and%20maps%2FMin-Max-Heap.png?alt=media&token=cb792085-64d2-4093-bc6f-c202463178cb)

### Common Implementation: Binary Heap

The **Binary Heap** is a popular heap implementation that is essentially a complete binary tree. The tree can represent either a Min Heap or Max Heap, with sibling nodes not being ordered relative to each other.

#### Array Representation and Index Relationships

Binary heaps are usually implemented using an array, where:

- Root: `heap[0]`
- Left Child: `heap[2 * i + 1]`
- Right Child: `heap[2 * i + 2]`
- Parent: `heap[(i - 1) // 2]`

### Core Operations

1. **Insert**: Adds an element while maintaining the heap order, generally using a "heapify-up" algorithm.
2. **Delete-Min/Delete-Max**: Removes the root and restructures the heap, typically using a "heapify-down" or "percolate-down" algorithm.
3. **Peek**: Fetches the root element without removing it.
4. **Heapify**: Builds a heap from an unordered collection.
5. **Size**: Returns the number of elements in the heap.

### Performance Metrics

- **Insert**: $O(\log n)$
- **Delete-Min/Delete-Max**: $O(\log n)$
- **Peek**: $O(1)$
- **Heapify**: $O(n)$
- **Size**: $O(1)$

### Code Example: Min Heap

Here is the Python code:

```python
# Utility functions for heapify-up and heapify-down
def heapify_up(heap, idx):
    parent = (idx - 1) // 2
    if parent >= 0 and heap[parent] > heap[idx]:
        heap[parent], heap[idx] = heap[idx], heap[parent]
        heapify_up(heap, parent)

def heapify_down(heap, idx, heap_size):
    left = 2 * idx + 1
    right = 2 * idx + 2
    smallest = idx
    if left < heap_size and heap[left] < heap[smallest]:
        smallest = left
    if right < heap_size and heap[right] < heap[smallest]:
        smallest = right
    if smallest != idx:
        heap[idx], heap[smallest] = heap[smallest], heap[idx]
        heapify_down(heap, smallest, heap_size)

# Complete MinHeap class
class MinHeap:
    def __init__(self):
        self.heap = []

    def insert(self, value):
        self.heap.append(value)
        heapify_up(self.heap, len(self.heap) - 1)

    def delete_min(self):
        if not self.heap:
            return None
        min_val = self.heap[0]
        self.heap[0] = self.heap[-1]
        self.heap.pop()
        heapify_down(self.heap, 0, len(self.heap))
        return min_val

    def peek(self):
        return self.heap[0] if self.heap else None

    def size(self):
        return len(self.heap)
```

---

## 🔹 2. What are some _Practical Applications_ of _Heaps_?

### Answer

**Heaps** find application in a variety of algorithms and data handling tasks.

### Practical Applications

- **Extreme Value Access**: The root of a min-heap provides the smallest element, while the root of a max-heap provides the largest, allowing constant-time access.
  
- **Selection Algorithms**: Heaps can efficiently find the $k^{th}$ smallest or largest element in $O(k \log k + n)$ time.

- **Priority Queue**: Using heaps, we can effectively manage a set of data wherein each element possesses a distinct priority, ensuring operations like insertion, maximum extraction, and sorting are performed efficiently.

- **Sorting**: Heaps play a pivotal role in the Heap Sort algorithm, offering $O(n \log n)$ time complexity. They're also behind utility functions in some languages like `nlargest()` and `nsmallest()`.

- **Merge Sorted Streams**: Heaps facilitate the merging of multiple pre-sorted datasets or streams into one cohesive sorted output.

- **Graph Algorithms**: Heaps, especially when implemented as priority queues, are instrumental in graph algorithms such as Dijkstra's Shortest Path and Prim's Minimum Spanning Tree, where they assist in selecting the next node to process efficiently.

---

## 🔹 3. What is a _Priority Queue_?

### Answer

A **Priority Queue** is a specialized data structure that manages elements based on their assigned priorities. In this queue, **higher-priority** elements are processed before lower-priority ones.

### Key Features

- **Dynamic Ordering**: The queue adjusts its order as elements are inserted or their priorities are updated.
- **Efficient Selection**: The queue is optimized for quick retrieval of the highest-priority element.

### Core Operations

- **Insert**: Adds an element and its associated priority.
- **Delete-Max (or Min)**: Removes the highest-priority element.
- **Peek**: Retrieves but does not remove the highest-priority element.

### Performance Metrics

- **Insert**: $O(\log n)$
- **Delete-Max (or Min)**: $O(\log n)$
- **Peek**: $O(1)$

### Common Implementations

- **Unsorted Array/List**: Quick inserts $O(1)$ but slower maximum-priority retrieval $O(n)$.
- **Sorted Array/List**: Slower inserts $O(n)$ but quick maximum-priority retrieval $O(1)$.
- **Binary Heap**: Balanced performance for both insertions and deletions.

### Code Example: Binary heap-based priority queue

Here is the Python code:

```python
import heapq

# Initialize an empty Priority Queue
priority_queue = []

# Insert elements
heapq.heappush(priority_queue, 3)
heapq.heappush(priority_queue, 1)
heapq.heappush(priority_queue, 2)

# Remove and display the highest-priority element
print(heapq.heappop(priority_queue))  # Output: 1
```

---

## 🔹 4. Name some ways to implement _Priority Queue_.

### Answer

Let's look at different ways **Priority Queues** can be implemented and the time complexities associated with each approach.

### Common Implementations

#### List-Based

- **Unordered List**:
    - Insertion: $O(1)$
    - Deletion/Find Min/Max: $O(n)$
  
- **Ordered List**:  
    - Insertion: $O(n)$
    - Deletion/Find Min/Max: $O(1)$

#### Array-Based

- **Unordered Array**:
    - Insertion: $O(1)$
    - Deletion/Find Min/Max: $O(n)$

- **Ordered Array**:  
    - Insertion: $O(n)$
    - Deletion/Find Min/Max: $O(1)$

#### Tree-Based

- **Binary Search Tree (BST)**:
    - All Operations: $O(\log n)$ (can degrade to $O(n)$ if unbalanced)

- **Balanced BST (e.g., AVL Tree)**:
    - All Operations: $O(\log n)$

- **Binary Heap**:
    - Insertion/Deletion: $O(\log n)$
    - Find Min/Max: $O(1)$

---
## 🔹 5. Compare _Heaps-Based_ vs. _Arrays-Based_ priority queue implementations.

### Answer

👉🏼 Check out all 10 answers here: [Devinterview.io - Heaps & Maps](https://devinterview.io/data/heapsAndMaps-interview-questions)

---

## 🔹 6. What are the advantages of _Heaps_ over _Sorted Arrays_?

### Answer

👉🏼 Check out all 10 answers here: [Devinterview.io - Heaps & Maps](https://devinterview.io/data/heapsAndMaps-interview-questions)

---

## 🔹 7. What is _Heap Sort_?

### Answer

👉🏼 Check out all 10 answers here: [Devinterview.io - Heaps & Maps](https://devinterview.io/data/heapsAndMaps-interview-questions)

---

## 🔹 8. What is the difference between _Heap_ and _Red-Black Tree_?

### Answer

👉🏼 Check out all 10 answers here: [Devinterview.io - Heaps & Maps](https://devinterview.io/data/heapsAndMaps-interview-questions)

---

## 🔹 9. Find _100 largest numbers_ in an _Array_ of 1 billion numbers.

### Answer

👉🏼 Check out all 10 answers here: [Devinterview.io - Heaps & Maps](https://devinterview.io/data/heapsAndMaps-interview-questions)

---

## 🔹 10. _Insert_ an item into the _Heap_. Explain your actions.

### Answer

👉🏼 Check out all 10 answers here: [Devinterview.io - Heaps & Maps](https://devinterview.io/data/heapsAndMaps-interview-questions)

---

