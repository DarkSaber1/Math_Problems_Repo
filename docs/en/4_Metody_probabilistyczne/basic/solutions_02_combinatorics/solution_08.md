# Task 8 — Sequences with Repetition

In this task we work with **5-digit PIN codes**.

A PIN code is an ordered sequence of digits.  
This means:

- **order matters**, because for example \(12345 \neq 54321\),
- digits are chosen from \(0\) to \(9\),
- repetition is allowed unless stated otherwise.

So the natural counting model here is a **sequence with repetition**.

For a sequence of length \(k\) built from \(n\) possible symbols, the number of sequences is

$$
n^k
$$

Here:

- \(n=10\) possible digits \((0,1,2,\dots,9)\),
- \(k=5\) positions.

We now solve each part carefully.

---

## 1. How many 5-digit PIN codes are possible if digits may repeat?

Each of the 5 positions can contain any of the 10 digits.

So:

- 10 choices for the first digit,
- 10 choices for the second digit,
- 10 choices for the third digit,
- 10 choices for the fourth digit,
- 10 choices for the fifth digit.

By the product rule, the total number of PIN codes is

$$
10 \cdot 10 \cdot 10 \cdot 10 \cdot 10 = 10^5
$$

Thus,

$$
10^5 = 100000
$$

### Answer:
$$
100000
$$

---

## 2. How many such codes contain **at least one repeated digit**?

Now we want the number of 5-digit PIN codes that contain **at least one repetition**.

The easiest way is to use the **complement method**:

So we need two quantities:

1. total number of PIN codes,
2. number of PIN codes with all digits distinct.

### Step 1: Count all PIN codes

From part 1:

$$
10^5 = 100000
$$

### Step 2: Count codes with all digits different

Now repetition is not allowed.

We must fill 5 positions using distinct digits from the 10 available digits.

Since order matters, this is an ordered selection without repetition:

- 10 choices for the first digit,
- 9 for the second,
- 8 for the third,
- 7 for the fourth,
- 6 for the fifth.

So the number is

$$
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6
$$

Compute:

$$
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30240
$$

### Step 3: Subtract

Therefore, the number of codes containing at least one repeated digit is

$$
100000 - 30240 = 69760
$$

### Answer:
$$
69760
$$

---

## 3. How many such codes have **all digits different**?

This is exactly the quantity computed in part 2, step 2.

We want 5-digit PIN codes with no repeated digits.

That means:

- 10 choices for the first position,
- 9 choices for the second,
- 8 choices for the third,
- 7 choices for the fourth,
- 6 choices for the fifth.

So the number is

$$
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30240
$$

Equivalently, this can be written as the k-permutation

$$
P(10,5)=\frac{10!}{5!}=30240
$$

### Answer:
$$
30240
$$

---

# Final Answers

1. Number of 5-digit PIN codes with repetition allowed:

$$
10^5 = 100000
$$

2. Number of such codes containing at least one repeated digit:

$$
10^5 - (10 \cdot 9 \cdot 8 \cdot 7 \cdot 6)=100000-30240=69760
$$

3. Number of such codes with all digits different:

$$
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30240
$$
