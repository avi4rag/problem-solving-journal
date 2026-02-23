# Longest Common Prefix (LeetCode #14)

## Problem Summary

Given an array of strings, find the longest common prefix string among them.

If there is no common prefix, return an empty string "".

---

## My Initial Thought

Compare characters one by one across all strings.

Since we are looking for a prefix, we can compare character at index `i` for every string.

If mismatch occurs at any position:
- Return substring from 0 to i.

---

## Approach Used (Vertical Scanning)

1. Take the first string as reference.
2. Loop through each character index `i`.
3. Compare that character with the same index in other strings.
4. If:
   - Index exceeds length of another string
   - Characters don’t match
   → Return prefix until that index.
5. If loop completes, return first string.

---

## Why This Works

A prefix must match character-by-character from the start.

As soon as mismatch happens, prefix ends.

---

## Time & Space Complexity

Time Complexity: O(S)

Where S = total number of characters in all strings.

Space Complexity: O(1)

---

## Mistakes I Made Initially

- Didn’t handle empty array case.
- Forgot to check index bounds for shorter strings.
- Initially tried sorting-based approach (unnecessary).

---

## What I Learned

- Vertical scanning is straightforward and clean.
- Always handle edge cases (empty input).
- Prefix problems are about early termination.

---

## Can I Re-Solve Without Looking?

(To update after second attempt)