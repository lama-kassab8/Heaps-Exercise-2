# Kth Smallest Element Using Min-Heap

This project solves the problem of finding the kth smallest element in an unsorted array using a **min-heap** data structure.

## Problem Statement

Given an unsorted array `A` and an integer `k` (1-indexed), find the kth smallest element in the array.

## Approach

We use a **min-heap** to efficiently extract the smallest elements:

1. Build a min-heap from the input array in O(n) time.
2. Pop (remove) the smallest element from the heap `k-1` times.
3. The next popped element is the kth smallest element.

This approach ensures efficient retrieval with an overall time complexity of approximately O(n + k log n).

## Implementation Details

- The `MinHeap` class implements a min-heap with essential operations such as `push`, `pop`, `heapify_up`, and `heapify_down`.
- The method `kth_smallest` in the `MinHeap` class returns the kth smallest element by popping elements `k-1` times and returning the next one.

## Example Usage

```python
A = [7, 10, 4, 3, 20, 15]
k = 3

heap = MinHeap(A)
print(f"{k}th smallest element is:", heap.kth_smallest(k))
