# DSA Mid-Term Learning Report

## Introduction

Over the first half of this DSA prohect, I solved problems from various topics including Arrays, Prefix Sums, Sliding Window, Binary Search, Stacks, Queues, Trees, BSTs, Greedy Algorithms, Heaps, Recursion, Backtracking, and Dynamic Programming on LeetCode.

The main objective was not just solving problems but understanding the intuition behind the algorithms, why they work, and how to optimize brute-force solutions. While solving these problems, I learned that many seemingly different questions actually follow common patterns, and identifying those patterns is often more important than coding itself.

---

# Arrays and Hashing

### Problems Solved

- Two Sum
- Majority Element
- Contains Duplicate
- Maximum Subarray
- Best Time to Buy and Sell Stock
- Sort Colors
- 3 Sum
- 4 Sum

## What I Learned

Initially, most array problems looked like brute-force problems. My first instinct was often to use nested loops, but after solving more questions, I started noticing patterns involving hashing and frequency counting.

### Important Observations

#### Two Sum

The biggest learning from this problem was understanding how a HashMap can reduce a solution from O(n²) to O(n).

Instead of checking every pair, we store previously seen elements and directly look for the required complement.

#### Majority Element

This problem introduced me to the Boyer-Moore Voting Algorithm. It was surprising that the majority element can be found using only constant extra space.

#### Maximum Subarray

This was my introduction to Kadane's Algorithm.

The key observation is that carrying a negative sum forward can never help in creating a larger subarray sum later.

### Complexity Discussion

| Problem | Optimized Complexity |
|----------|--------------------|
| Two Sum | O(n) |
| Majority Element | O(n) |
| Contains Duplicate | O(n) |
| Maximum Subarray | O(n) |
| Best Time to Buy and Sell Stock | O(n) |

### Beginner Difficulties

- Understanding when to use hashing
- Identifying patterns instead of brute force
- Handling duplicate values correctly

---

# Prefix Sum Technique

### Problems Solved

- Range Sum Query
- Range Sum Query 2D
- Subarray Sums Divisible by K
- Count Number of Nice Subarrays
- Continuous Subarray Sum

## What I Learned

Prefix sums completely changed the way I approached subarray problems.

Before learning this technique, I usually recalculated sums repeatedly, leading to inefficient solutions.

### Important Observation

If prefix sums are precomputed, any range sum can be calculated in constant time.

For an array:

```text
prefix[i] = prefix[i-1] + arr[i]
```

Range sum from L to R:

```text
sum(L,R) = prefix[R] - prefix[L-1]
```

This idea becomes even more powerful when combined with hashing.

### Most Interesting Problem

#### Subarray Sums Divisible by K

This problem taught me how modular arithmetic can be combined with prefix sums.

Understanding why equal remainders indicate a valid subarray was one of the most important mathematical insights I learned during the course.

### Beginner Difficulties

- Understanding prefix indices
- Avoiding off-by-one errors
- Applying modulo operations correctly

---

# Sliding Window and Two Pointers

### Problems Solved

- Longest Substring Without Repeating Characters
- Maximum Points You Can Obtain from Cards
- Longest Repeating Character Replacement
- Binary Subarrays With Sum
- Number of Substrings Containing All Three Characters
- Subarrays With K Different Integers

## What I Learned

Initially, I struggled with deciding when to expand the window and when to shrink it.

After solving multiple problems, I realized that sliding window problems are mostly about maintaining a valid condition while moving two pointers.

### Important Observation

Every element enters and leaves the window at most once.

Therefore most sliding window solutions run in O(n).

### Most Challenging Problem

#### Longest Repeating Character Replacement

The logic behind maintaining the window while allowing replacements was difficult initially, but it helped me understand how flexible sliding windows work.

### Beginner Difficulties

- Maintaining the window condition
- Updating frequency counts correctly
- Knowing when to shrink the window

---

# Binary Search

### Problems Solved

- Search Insert Position
- Search in Rotated Sorted Array
- Find Peak Element
- Search a 2D Matrix
- Koko Eating Bananas
- Capacity To Ship Packages Within D Days
- Split Array Largest Sum

## What I Learned

Before this course, I thought binary search could only be used on sorted arrays.

The most important lesson was learning Binary Search on Answers.

### Most Interesting Problem

#### Koko Eating Bananas

This problem taught me how to binary search over possible answers instead of array indices.

Once I understood the monotonic property, many other optimization problems became easier to recognize.

### Why Binary Search Works

If a condition becomes true at some point and remains true afterwards:

```text
False False False True True True
```

Binary search can efficiently find the first valid answer.

### Beginner Difficulties

- Choosing search boundaries
- Avoiding infinite loops
- Identifying monotonic conditions

---

# Stacks, Queues and Monotonic Structures

### Problems Solved

- Valid Parentheses
- Daily Temperatures
- Next Greater Element
- Asteroid Collision
- Sliding Window Maximum
- Largest Rectangle in Histogram
- Sum of Subarray Minimums

## What I Learned

Stacks initially seemed simple, but monotonic stacks introduced a completely different way of solving problems.

### Most Challenging Problem

#### Largest Rectangle in Histogram

This was one of the hardest problems I solved.

The difficulty was understanding how previous smaller and next smaller elements help determine the maximum rectangle area.

### Important Observation

Each element is pushed and popped only once.

This is why many monotonic stack solutions run in O(n).

### Beginner Difficulties

- Understanding stack state
- Visualizing monotonic stacks
- Finding nearest greater/smaller elements

---

# Recursion and Backtracking

### Problems Solved

- Generate Parentheses
- Subsets
- Combination Sum
- Letter Combinations of a Phone Number
- N Queens
- Sudoku Solver
- Palindrome Partitioning

## What I Learned

Backtracking taught me how to systematically explore all possible choices while eliminating invalid paths early.

### Most Challenging Problem

#### Sudoku Solver

This problem helped me understand recursive state exploration and pruning.

### General Backtracking Process

1. Make a choice
2. Explore recursively
3. Undo the choice
4. Explore remaining possibilities

### Beginner Difficulties

- Writing correct base cases
- Managing recursive state
- Understanding recursion trees

---

# Trees and Binary Search Trees

### Problems Solved

#### Binary Trees

- Preorder Traversal
- Inorder Traversal
- Postorder Traversal
- Maximum Depth
- Level Order Traversal
- Lowest Common Ancestor

#### Binary Search Trees

- Search in BST
- Insert into BST
- Validate BST
- Kth Smallest Element
- BST Iterator

## What I Learned

Tree problems significantly improved my recursive thinking.

### Important Observation

For every BST:

```text
Left Subtree < Root < Right Subtree
```

Understanding this property makes many BST problems easier.

### Most Interesting Problem

#### Validate BST

This problem taught me that checking only parent-child relationships is not sufficient.

The entire valid range must be maintained during recursion.

### Beginner Difficulties

- Recursive traversal logic
- Understanding BST properties
- Managing subtree constraints

---

# Greedy Algorithms and Heaps

### Problems Solved

- Assign Cookies
- Task Scheduler
- Top K Frequent Elements
- IPO
- Minimum Refueling Stops
- Merge K Sorted Lists

## What I Learned

The hardest part of greedy algorithms is proving that a locally optimal choice leads to a globally optimal solution.

### Most Interesting Problem

#### IPO

This problem combined heaps and greedy strategy and showed how multiple concepts can work together.

### Important Observation

Heaps are extremely useful whenever repeated access to the maximum or minimum element is required.

### Complexity

| Operation | Complexity |
|------------|------------|
| Insert | O(log n) |
| Delete | O(log n) |
| Top Element | O(1) |

---

# Dynamic Programming

### Problems Solved

- Climbing Stairs
- Min Cost Climbing Stairs
- House Robber
- House Robber II
- Decode Ways
- Unique Paths
- Minimum Path Sum
- Triangle
- Minimum Falling Path Sum

## What I Learned

Dynamic Programming was one of the most rewarding topics because it converts exponential solutions into efficient polynomial-time solutions.

### Most Challenging Problem

#### Decode Ways

The challenge was identifying the correct state transition and handling edge cases involving zeros.

### General DP Approach

1. Define the state
2. Find the recurrence relation
3. Store previous results
4. Build the final answer

### Example

```text
dp[i] = dp[i-1] + dp[i-2]
```

This recurrence is used in the Climbing Stairs problem.

### Beginner Difficulties

- Defining states
- Finding transitions
- Handling base cases

---

# Some Important notes I made

Some of the biggest lessons I learned from this course are:

- Hashing can eliminate unnecessary searching.
- Prefix sums simplify many subarray problems.
- Sliding windows reduce quadratic solutions to linear solutions.
- Binary search can be applied beyond sorted arrays.
- Monotonic stacks solve many nearest greater/smaller problems efficiently.
- Backtracking is useful for constraint satisfaction problems.
- BST properties simplify searching and ordering operations.
- Greedy solutions require correctness reasoning.
- Dynamic Programming avoids repeated computation.

---

# Conclusion

This project has significantly improved my problem-solving approach. Instead of directly thinking about implementation, I now first look for patterns, invariants, and possible optimizations.

The transition from brute-force thinking to recognizing standard DSA techniques has been the biggest improvement in my learning journey so far.

Among all topics covered, Binary Search on Answers, Monotonic Stacks, and Dynamic Programming were the most challenging but also the most rewarding to learn. Going forward, I aim to strengthen my understanding of advanced DP, graph algorithms, and more complex data structures.
