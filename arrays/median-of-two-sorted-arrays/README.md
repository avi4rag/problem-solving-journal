# Median of Two Sorted Arrays (LeetCode #4)

## Problem Summary

Given two sorted arrays nums1 and nums2, return the median of the two sorted arrays.

The overall run time complexity should be O(log(min(n, m))), but this implementation uses a simpler merge-style approach.

---

## My Initial Thought

Since both arrays are already sorted, I realized I don’t need to fully merge them.

I only need to iterate until reaching the middle element.

So I used two pointers to simulate the merge process, but stopped at the median position.

---

## Approach Used

1. Calculate total length = n + m.
2. Use two pointers (i and j) to traverse both arrays.
3. Track:
   - `curr` → current element
   - `prev` → previous element (needed for even case)
4. Iterate until total/2.
5. If total length is:
   - Even → return average of prev and curr.
   - Odd → return curr.

---

## Why This Works

The arrays are already sorted.

By simulating the merge process, the elements are accessed in sorted order without building a new array.

Since we stop at the median index, we avoid unnecessary work.

---

## Time & Space Complexity

Time Complexity: O(n + m)  
Space Complexity: O(1)

---

## Mistakes I Made Initially

- Forgot to track the previous element for even case.
- Confused index boundary conditions.
- Initially tried fully merging arrays (unnecessary).

---

## What I Learned

- I don’t always need to construct the full merged array.
- Tracking only required values reduces space.
- Edge case handling is important (empty arrays).

---

## Can I Re-Solve Without Looking?

(Will update after second attempt)