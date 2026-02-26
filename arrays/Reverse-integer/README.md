# Reverse Integer (LeetCode #7)

## Problem Summary

Given a signed 32-bit integer `x`, return the integer with its digits reversed.

If reversing `x` causes it to go outside the 32-bit signed integer range:

[-2147483648, 2147483647]

Return 0.

---

## My Initial Approach

I extracted digits one by one:

- Take last digit using `x % 10`
- Remove last digit using `x / 10`
- Build reversed number using:

    reversed = reversed * 10 + digit

This worked for normal inputs like:

123 → 321  
-123 → -321  
120 → 21  

But failed for very large values.

---

## The Real Issue — Overflow

Java does not throw an error on integer overflow.

It silently wraps the value.

For example:

Input:
1534236469

Reversed value exceeds 32-bit limit.

Expected output:
0

But without overflow check, Java produces a wrapped incorrect number.

---

## Correct Logic

Before multiplying reversed by 10, we must check:

If reversed > Integer.MAX_VALUE / 10  
or reversed < Integer.MIN_VALUE / 10  

Then overflow will happen.

Return 0 immediately.

---

Time & Space Complexity

Time Complexity: O(log₁₀(n))
Space Complexity: O(1)

What I Learned

Math-based digit extraction is simple and efficient.

Overflow must be checked before multiplication.

Java silently overflows — it does not warn you.

Edge cases are often the real test in interviews.