# Container With Most Water (LeetCode #11)

## Problem Summary

Given an array `height` where each element represents the height of a vertical line, find two lines that together with the x-axis form a container that holds the most water.

Return the maximum area.

---

## My Initial Thought

Brute force approach:
Try every pair of lines and compute area.

That would be O(n²), which is too slow for large inputs.

---

## Optimized Approach (Two Pointers)

1. Place one pointer at the start (left).
2. Place one pointer at the end (right).
3. Compute area:
   - width = right - left
   - height = min(height[left], height[right])
4. Update maximum area.
5. Move the pointer pointing to the smaller height inward.

Repeat until left < right.

---

## Why Moving the Smaller Pointer Works

The area is limited by the shorter line.

If we move the taller line inward:
- Width decreases
- Height stays limited by shorter one
- Area can only decrease

So we move the smaller one, hoping to find a taller line.

---

## Time & Space Complexity

Time Complexity: O(n)  
Space Complexity: O(1)

---

## Mistakes I Made Initially

- Tried brute force first.
- Didn’t understand why moving the smaller pointer is correct.
- Forgot to update maxArea properly.

---

## What I Learned

- Two-pointer technique reduces O(n²) to O(n).
- Greedy reasoning can drastically optimize brute-force logic.
- Understanding WHY pointer moves is more important than memorizing it.

---

## Can I Re-Solve Without Looking?

(Will update after second attempt)