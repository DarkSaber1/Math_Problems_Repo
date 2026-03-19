# Task 7 — k-Permutations (Ordered Selections Without Repetition)

In this task we use **k-permutations**, also called **ordered selections without repetition**.

This model applies when:

- we choose only **some** of the objects,
- **order matters**,
- repetition is **not allowed**.

The general formula is

$$
P(n,k)=\frac{n!}{(n-k)!}
$$

We now solve each problem step by step.

---

## 1. In how many ways can the first three places be assigned among 12 runners?

We are assigning:

- 1st place,
- 2nd place,
- 3rd place

among 12 runners.

Only **3 runners** are selected from 12, and the order matters because:

- first place is different from second place,
- second place is different from third place.

Also, one runner cannot occupy more than one place, so repetition is not allowed.

Therefore, this is a **k-permutation** with:

- \(n=12\)
- \(k=3\)

So the number of ways is

$$
P(12,3)=\frac{12!}{(12-3)!}=\frac{12!}{9!}
$$

Simplify:

$$
P(12,3)=12\cdot 11\cdot 10=1320
$$

### Answer:
$$
1320
$$

---

## 2. How many 4-digit numbers with distinct digits can be formed from the digits 1–9?

We want to form 4-digit numbers using the digits:

$$
\{1,2,3,4,5,6,7,8,9\}
$$

The digits must be **distinct**, so no repetition is allowed.

Since we are forming a number, **order matters**.  
For example:

$$
1234 \neq 4321
$$

We are choosing 4 digits from 9, in order, without repetition.  
So this is again a **k-permutation** with:

- \(n=9\)
- \(k=4\)

Thus,

$$
P(9,4)=\frac{9!}{(9-4)!}=\frac{9!}{5!}
$$

Simplify:

$$
P(9,4)=9\cdot 8\cdot 7\cdot 6=3024
$$

### Answer:
$$
3024
$$

---

## 3. How many of these numbers are divisible by 5?

We are still forming 4-digit numbers from the digits 1–9, with all digits distinct.

Now we add the extra condition: the number must be divisible by 5.

A number is divisible by 5 if its last digit is either:

- 0, or
- 5

But in this problem the available digits are only \(1\) to \(9\), so the only possible last digit is

$$
5
$$

So the last position is fixed as 5.

Now we must choose the first 3 digits from the remaining 8 digits:

$$
\{1,2,3,4,6,7,8,9\}
$$

These 3 digits must be distinct, and order matters.

So we are arranging 3 digits chosen from 8 distinct digits:

$$
P(8,3)=\frac{8!}{(8-3)!}=\frac{8!}{5!}
$$

Simplify:

$$
P(8,3)=8\cdot 7\cdot 6=336
$$

### Answer:
$$
336
$$

---

# Final Answers

1. Number of ways to assign first, second, and third place among 12 runners:

$$
P(12,3)=12\cdot 11\cdot 10=1320
$$

2. Number of 4-digit numbers with distinct digits formed from 1–9:

$$
P(9,4)=9\cdot 8\cdot 7\cdot 6=3024
$$

3. Number of such numbers divisible by 5:

$$
P(8,3)=8\cdot 7\cdot 6=336
$$