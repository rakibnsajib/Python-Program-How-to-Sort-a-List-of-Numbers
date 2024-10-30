# Python Program: How to Sort a List of Numbers

Sorting is the process of arranging elements in a list or sequence according to a specific order, commonly in ascending or descending order. Here, learn about different techniques to sort lists in Python, covering a variety of methods and their use cases.

### Method 1: Using the sorted() function <br>
The `sorted()` function sorts an iterable (like a list) and returns a new, sorted list. By default, it sorts in ascending order; however, setting `reverse=True` changes it to descending order.


**Syntax:** `sorted(list)`

**Example Code:**
```python
num_list = [4, 2, 7, 1, 9]
sorted_list = sorted(num_list)
print(sorted_list)  # Ascending order
print(sorted(num_list, reverse=True))  # Descending order
```

### Method 2: Using the sort() method
The `sort()` method sorts a list in place, modifying the original list rather than creating a new one. Like `sorted()`, it sorts in ascending order unless `reverse=True` is used.


**Syntax:** `list.sort()`

**Example Code:**
```python
num_list.sort()  # Ascending order
num_list.sort(reverse=True)  # Descending order
```

### Method 3: Using the [::-1] slicing technique
Slicing reverses a list's order without performing a sort, simply displaying the elements in reverse sequence.


**Syntax:** `list[::-1]`

**Example Code:**
```python
reversed_list = num_list[::-1]
```

### Method 4: Using the Lambda Function with sorted()
A custom sorting function can be applied by using the `key` parameter with a lambda function. This allows sorting based on criteria like remainder values or other custom conditions.

**Syntax:** `sorted(iterable, key=lambda x: custom_function(x))`

**Example Code:**
```python
sorted_by_remainder = sorted(num_list, key=lambda x: x % 5)
```

### Method 5: Using heapq module for large lists
The `heapq` module is efficient for sorting large lists, as it organizes data into a heap structure. This method can be memory-efficient and is particularly useful for continuously extracting the smallest element.

**Syntax:** <br>
`heapq.heapify(list)` <br>
`[heapq.heappop(list) for _ in range(len(list))]`

**Example Code:**
```python
import heapq
heapq.heapify(list)  # Converts list to a heap
sorted_list = [heapq.heappop(list) for _ in range(len(list))]
```


### Key Points

- **Mixed Types Sorting:** Python can handle lists of both integers and floats.
- **Scientific Notation:** Numbers in scientific notation sort like regular numbers.
- **Negative Numbers:** Python sorting functions include negative values correctly.
- **Custom Criteria:** Use `key` with a lambda function for custom sorting.
- **Large List Efficiency:** Use `heapq` for memory-efficient sorting on large lists.
