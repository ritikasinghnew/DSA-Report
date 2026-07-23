# DSA End-Term Learning Report

## Introduction

During the completion of this Data Structures and Algorithms (DSA) project, I solved a wide range of LeetCode problems covering Arrays, Hashing, Prefix Sums, Sliding Window, Binary Search, Stacks, Queues, Trees, Binary Search Trees, Greedy Algorithms, Heaps, Recursion, Backtracking, Dynamic Programming, and several advanced problem-solving techniques.

Compared to the mid-term stage, my focus shifted from simply finding correct solutions to understanding algorithmic patterns, optimizing time and space complexity, and selecting the most appropriate data structure for each problem.

Throughout this project, I learned that many difficult-looking problems are variations of a few fundamental concepts. Recognizing these patterns before writing code has become the biggest improvement in my problem-solving journey.

---

# Arrays, Hashing and Basic Simulation

## Problems Solved

- Two Sum
- Majority Element
- Contains Duplicate
- Max Consecutive Ones
- Maximum Subarray
- Best Time to Buy and Sell Stock
- Rearrange Array Elements by Sign
- Sort Colors
- Set Matrix Zeroes
- 3 Sum
- 4 Sum

## What I Learned

Arrays formed the foundation of my DSA learning journey. Initially, I solved most problems using nested loops, but gradually I learned how hashing, sorting, and two-pointer techniques could significantly improve efficiency.

Simulation-based problems also taught me the importance of handling edge cases and writing clean implementations.

### Important Learnings

#### Two Sum

Using a HashMap allows storing previously visited elements and directly finding the required complement, reducing the complexity from **O(n²)** to **O(n)**.

#### Maximum Subarray

Kadane's Algorithm showed that carrying a negative running sum can never contribute to a larger future subarray.

#### Set Matrix Zeroes

This problem introduced space optimization by using the first row and first column as markers instead of extra memory.

#### 3 Sum & 4 Sum

These problems improved my understanding of sorting, duplicate handling, and efficient use of two pointers.

### Complexity

| Problem | Optimized Complexity |
|----------|----------------------|
| Two Sum | O(n) |
| Majority Element | O(n) |
| Contains Duplicate | O(n) |
| Maximum Subarray | O(n) |
| Best Time to Buy and Sell Stock | O(n) |
| Sort Colors | O(n) |
| Set Matrix Zeroes | O(m × n) |
| 3 Sum | O(n²) |
| 4 Sum | O(n³) |

### Challenges Faced

- Understanding when hashing is useful
- Avoiding duplicate answers
- Learning in-place optimizations
- Choosing between brute-force and optimized solutions

---

# Prefix Sums

## What I Learned

Prefix sums completely changed the way I approached subarray problems. Instead of calculating sums repeatedly, I learned to preprocess cumulative sums and answer range queries efficiently.

Combining prefix sums with hashing helped solve several difficult subarray problems in linear time.

### Key Observation

```cpp
prefix[i] = prefix[i - 1] + arr[i];
```

Range Sum:

```cpp
sum(L, R) = prefix[R] - prefix[L - 1];
```

This technique appears in many optimization problems.

### Challenges Faced

- Managing prefix indices
- Avoiding off-by-one errors
- Correctly applying modulo arithmetic

---

# Sliding Window & Two Pointers

## What I Learned

Sliding Window became one of my favorite techniques because it transforms many quadratic solutions into linear ones.

The biggest learning was maintaining a valid window while expanding and shrinking pointers according to the problem constraints.

### Important Observation

Each element enters and leaves the window at most once.

Therefore, most sliding window algorithms run in:

```text
O(n)
```

### Biggest Learning

Instead of recalculating values repeatedly, maintain only the information required for the current window.

### Challenges Faced

- Maintaining valid window conditions
- Updating frequency maps
- Deciding when to shrink the window

---

# Binary Search

## What I Learned

One of the biggest improvements during this project was understanding **Binary Search on Answers**.

Earlier, I believed binary search worked only on sorted arrays. Now I understand that it can also optimize search spaces whenever a monotonic condition exists.

### Important Insight

If a condition changes like:

```text
False False False True True True
```

Binary Search can efficiently locate the first valid answer.

This concept is used in problems like:

- Koko Eating Bananas
- Capacity To Ship Packages
- Split Array Largest Sum

### Challenges Faced

- Choosing search boundaries
- Avoiding infinite loops
- Identifying monotonic properties

---

# Stacks, Queues & Monotonic Structures

## What I Learned

Monotonic stacks introduced a completely different way of solving nearest greater/smaller element problems.

Instead of comparing every pair of elements, maintaining stack order allows efficient solutions.

### Most Challenging Problem

**Largest Rectangle in Histogram**

Understanding Previous Smaller Element (PSE) and Next Smaller Element (NSE) significantly improved my understanding of monotonic stacks.

### Important Observation

Each element is pushed and popped only once.

Overall complexity:

```text
O(n)
```

### Challenges Faced

- Visualizing stack operations
- Maintaining monotonic order
- Finding nearest greater/smaller elements

---

# Trees & Binary Search Trees

## What I Learned

Tree problems improved my recursive thinking and traversal techniques.

Binary Search Trees taught me how ordering properties simplify searching and insertion.

### Important BST Property

```text
Left Subtree < Root < Right Subtree
```

### Biggest Learning

Validate BST taught me that checking only parent-child relationships is insufficient.

The valid range must be maintained throughout recursion.

### Challenges Faced

- Recursive traversal
- Maintaining subtree constraints
- Understanding BST properties

---

# Recursion & Backtracking

## What I Learned

Backtracking taught me how to systematically explore every possibility while pruning invalid paths.

General process:

1. Make a choice
2. Explore recursively
3. Undo the choice
4. Explore remaining possibilities

### Most Challenging Problem

**Sudoku Solver**

This problem improved my understanding of recursion trees, pruning, and recursive state management.

### Challenges Faced

- Writing correct base cases
- Managing recursive state
- Understanding recursion flow

---

# Greedy Algorithms & Heaps

## What I Learned

Greedy algorithms taught me that selecting a locally optimal solution requires mathematical reasoning to prove global correctness.

Priority Queues (Heaps) became one of the most useful data structures for repeatedly accessing minimum or maximum elements.

### Heap Complexity

| Operation | Complexity |
|-----------|------------|
| Insert | O(log n) |
| Delete | O(log n) |
| Top Element | O(1) |

### Most Interesting Problem

**IPO**

This problem demonstrated how heaps and greedy strategies work together to solve optimization problems efficiently.

### Challenges Faced

- Understanding greedy correctness
- Choosing heap type
- Combining multiple concepts

---

# Dynamic Programming

## What I Learned

Dynamic Programming became one of the most rewarding topics because it transforms exponential recursive solutions into efficient polynomial-time algorithms.

### General DP Approach

1. Define the state
2. Find the recurrence
3. Store computed results
4. Build the final solution

Example:

```cpp
dp[i] = dp[i - 1] + dp[i - 2];
```

Used in **Climbing Stairs**.

### Most Challenging Problem

**Decode Ways**

This problem helped me understand state transitions and handling edge cases involving zeros.

### Challenges Faced

- Defining DP states
- Finding recurrence relations
- Handling base cases

---

# Key Takeaways

The biggest lessons I learned throughout this project are:

- Hashing eliminates unnecessary searching.
- Prefix sums simplify many subarray problems.
- Sliding windows convert quadratic solutions into linear solutions.
- Binary Search can be applied to answer spaces, not just sorted arrays.
- Monotonic stacks efficiently solve nearest greater/smaller problems.
- Backtracking systematically explores constrained search spaces.
- BST properties simplify searching and ordering operations.
- Greedy algorithms require proof of correctness.
- Dynamic Programming avoids repeated computation through memoization and tabulation.
- Choosing the right data structure is often more important than writing complex code.

---

# Conclusion

Completing this DSA project has significantly improved my analytical thinking and problem-solving approach.

Initially, I relied heavily on brute-force methods, but over time I learned how to recognize algorithmic patterns, analyze constraints, and develop optimized solutions using appropriate data structures and algorithms.

The most valuable outcome of this project is not just the number of problems solved, but the ability to recognize recurring patterns and apply suitable techniques efficiently.

Among all the topics covered, **Binary Search on Answers**, **Monotonic Stacks**, **Backtracking**, and **Dynamic Programming** were the most challenging but also the most rewarding to master.

Going forward, I plan to strengthen my understanding of:

- Graph Algorithms
- Advanced Dynamic Programming
- Segment Trees
- Tries
- Union-Find (Disjoint Set Union)
- Advanced Data Structures

while continuing regular LeetCode practice to improve consistency, coding speed, and interview readiness.
