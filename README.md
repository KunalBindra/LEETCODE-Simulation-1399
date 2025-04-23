# LEETCODE-Simulation-1399
---

# Count Largest Digit Sum Group

This repository contains a Java implementation that solves the problem of counting the number of groups with the largest size based on the sum of digits of integers from `1` to `n`.

## 🧠 Problem Description

Given a number `n`, group all the integers from `1` to `n` based on the **sum of their digits**. Then, return the **number of groups that have the largest size**.

### Example:

For `n = 13`, the digit sums are:
```
1 → 1  
2 → 2  
3 → 3  
...  
10 → 1  
11 → 2  
12 → 3  
13 → 4  
```

Groups:
- Sum 1: [1, 10]
- Sum 2: [2, 11]
- Sum 3: [3, 12]
- Sum 4: [4, 13]
- Sum 5: [5]
- Sum 6: [6]
- Sum 7: [7]
- Sum 8: [8]
- Sum 9: [9]

Here, the group with digit sum 1, 2, and 3 each have size 2 (the maximum), so the result is `3`.

---

## 💡 Approach

- Create a helper method `gds(int num)` to calculate the **sum of digits** of a number.
- Use a `HashMap` to map each digit sum to its frequency (number of integers having that sum).
- Track the **maximum group size** and count how many groups have that size.

---

## 🔍 Class & Methods

### `public int gds(int num)`
Calculates the sum of digits of `num`.

### `public int countLargestGroup(int n)`
Returns the number of groups that have the largest size.

---

## 🛠️ How to Run

1. Copy the `Solution` class into your Java project.
2. Call `countLargestGroup(n)` with a desired integer `n`.
3. Observe the result which is the number of largest-sized groups based on digit sum.

### Example usage:
```java
Solution sol = new Solution();
System.out.println(sol.countLargestGroup(13)); // Output: 3
```

---

## 🧮 Time Complexity

- `gds(num)` runs in O(d), where `d` is the number of digits in `num`.
- The main loop runs from `1` to `n`, so total time complexity is **O(n × d)**.

---
