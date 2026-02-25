# Merge Two Sorted Lists (LeetCode #21)

## Problem Summary

You are given the heads of two sorted linked lists.

Merge the two lists into one sorted list and return its head.

---

## My Initial Thought

Since both lists are already sorted:

Compare nodes one by one.
Always attach the smaller node to the result list.

Repeat until one list becomes null.

Then attach remaining nodes.

---

## Approach Used (Iterative with Dummy Node)

1. Create a dummy node.
2. Use a pointer `current` to build the new list.
3. Compare `list1.val` and `list2.val`.
4. Attach smaller node to `current.next`.
5. Move that list forward.
6. Move `current` forward.
7. After loop, attach remaining nodes.

Return `dummy.next`.

---

## Why Dummy Node Helps

The dummy node avoids:

- Special handling for the head.
- Extra conditional checks.

It simplifies pointer logic.

---

## Time & Space Complexity

Time Complexity: O(n + m)

Where n and m are lengths of the two lists.

Space Complexity: O(1)

(No extra space used; we rearrange pointers.)

---

## Mistakes I Made Initially

- Forgot to move `current` pointer.
- Tried creating new nodes instead of reusing existing ones.
- Didn’t handle remaining nodes properly.

---

## What I Learned

- Dummy nodes simplify linked list problems.
- Pointer movement order is critical.
- Linked lists require careful null handling.

---

## Can I Re-Solve Without Looking?

(To update after second attempt)